Windows users should use docker managed volume for remote integration logs. 
Create docker volume (for ex. `tb-coap-integration-logs`) before executing docker run command:
Open "Docker Quickstart Terminal". Execute the following command to create docker volume:

``` 
docker volume create tb-pe-coap-integration-logs
```
{: .copy-code}

Execute the following command to run this docker directly:

```bash
docker run -it -p 5683:5683/udp -v tb-pe-coap-integration-logs:/var/log/tb-coap-integration `
-e "RPC_HOST=thingsboard.cloud" -e "RPC_PORT=9090" `
-e "INTEGRATION_ROUTING_KEY=YOUR_ROUTING_KEY"  -e "INTEGRATION_SECRET=YOUR_SECRET" `
--name my-tb-pe-coap-integration --restart always thingsboard/tb-pe-coap-integration:{{ site.release.pe_full_ver }}
```
{: .copy-code}

Where: 
    
- `thingsboard.cloud` - is the host name of your ThingsBoard PE instance;
- `9090` - is the port of your ThingsBoard PE instance. It is configured in thingsboard.yml using INTEGRATIONS_RPC_PORT env variable;    
- `YOUR_ROUTING_KEY` - placeholder for your integration routing key obtained on [Step 3](/docs/user-guide/integrations/remote-integrations/#step-3-save-remote-integration-credentials);
- `YOUR_SECRET` - placeholder for your integration secret obtained on [Step 3](/docs/user-guide/integrations/remote-integrations/#step-3-save-remote-integration-credentials);
- `docker run`              - run this container;
- `-it`                     - attach a terminal session with current ThingsBoard process output;
- `-p 5683:5683/udp` - connect local udp port 5683 to exposed internal 5683 udp port for the integration.
- `-v tb-pe-coap-integration-logs:/var/log/tb-coap-integration`   - mounts the host's dir `~/.tb-pe-coap-integration-logs` to ThingsBoard logs directory;
- `--name tb-pe-coap-integration`             - friendly local name of this machine;
- `--restart always`        - automatically start ThingsBoard Integration in case of system reboot and restart in case of failure.;
- `thingsboard/tb-pe-coap-integration:{{ site.release.pe_full_ver }}`          - docker image.

After executing this command you can open logs which are located here `~/.tb-pe-coap-integration-logs`. 
You should see some INFO log messages with your latest Integration configuration that arrived from the server.

<br/>

You can detach from session terminal with **`Ctrl-p`**+**`Ctrl-q`** - the container will keep running in the background.

<br/>

- **Reattaching, stop and start commands**

To reattach to the terminal (to see ThingsBoard logs) run:

```
docker attach tb-pe-coap-integration
```
{: .copy-code}

To stop the container:

```
docker stop tb-pe-coap-integration
```
{: .copy-code}

To start the container:

```
docker start tb-pe-coap-integration
```
{: .copy-code}