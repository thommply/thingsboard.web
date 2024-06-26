X.509 Certificates are used to setup [mutual](https://en.wikipedia.org/wiki/Mutual_authentication) (two-way) authentication for MQTT over TLS.
It is similar to [access token](/docs/{{docsPrefix}}user-guide/access-token/) authentication, but uses X.509 Certificate instead of token.

Instructions below will describe how to connect MQTT client using X.509 Certificate to ThingsBoard Cloud.

#### Step 1. Prepare your server and certificate chain

ThingsBoard Team has already provisioned a valid certificate for [ThingsBoard Cloud](https://thingsboard.cloud/signup).
Follow the [MQTT over SSL](/docs/{{docsPrefix}}user-guide/mqtt-over-ssl/) guide to provision server certificate if you are hosting your own ThingsBoard instance.

Once provisioned, you should prepare a certificate chain in pem format. This chain will be used by mqtt client to validate the server certificate.
Save the chain to your working directory as "**tb-server-chain.pem**".
An example of certificate chain for *mqtt.thingsboard.cloud* is located [here](/docs/paas/user-guide/resources/mqtt-over-ssl/tb-cloud-chain.pem).

#### Step 2. Generate Client certificate

Use the following command to generate the self-signed private key and x509 certificate.
The command is based on the **openssl** tool which is most likely already installed on your workstation:

To generate the RSA based key and certificate, use:

```bash
openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -sha256 -days 365 -nodes
```
{: .copy-code}

To generate the EC based key and certificate, use:

```bash
openssl ecparam -out key.pem -name secp256r1 -genkey
openssl req -new -key key.pem -x509 -nodes -days 365 -out cert.pem 
```
{: .copy-code}

The output of the command will be a private key file *key.pem* and a public certificate *cert.pem*.
We will use them in next steps.

#### Step 3. Provision Client Public Key as Device Credentials

{% if docsPrefix == 'pe/' %}
Go to **ThingsBoard Web UI -> Device Groups -> Group "All" -> Your Device -> Device Credentials**.
{% else %}
Go to **ThingsBoard Web UI -> Devices -> Your Device -> Device Credentials**.
{% endif %}
Select **X.509 Certificate** device credentials, insert the contents of *cert.pem* file and click save.
Alternatively, the same can be done through the [REST API](/docs/{{docsPrefix}}reference/rest-api/).

#### Step 4. Test the connection

Execute the following command to upload temperature readings to ThingsBoard Cloud using secure channel:

```bash
mosquitto_pub --cafile tb-server-chain.pem -d -q 1 -h "YOUR_TB_HOST" -p "8883" \
-t "v1/devices/me/telemetry" --key key.pem --cert cert.pem -m {"temperature":25}
```
{: .copy-code}

Don't forget to replace **YOUR_TB_HOST** with the host of your ThingsBoard instance.