---
layout: docwithnav-edge
title: Getting started with ThingsBoard Edge
description: Getting started with ThingsBoard Edge 

step1:
    0:
        image: /images/edge/getting-started/step-1-item-1.png 
        title: 'Login to your ThingsBoard <b>Edge</b> instance and open Devices page.'
    1:
        image: /images/edge/getting-started/step-1-item-2.png  
        title: 'Click on the "Add Device"("+`") icon in the top right corner of the table.'
    2:
        image: /images/edge/getting-started/step-1-item-3.png
        title: 'Input device name. For example, "My New Device". No other changes required at this time. Click "Add" to add the device.'
    3:
        image: /images/edge/getting-started/step-1-item-4.png
        title: 'Now your device should be listed first, since table sort devices using created time by default. '

step2:
    0:
        image: /images/edge/getting-started/step-2-item-1.png
        title: 'Login to your ThingsBoard <b>Community Edition</b> instance and open Devices page.'
    1:
        image: /images/edge/getting-started/step-2-item-2.png  
        title: 'Verify that "My New Device" device was created on the ThingsBoard Community Edition cloud.'
    2:
        image: /images/edge/getting-started/step-2-item-3.png
        title: 'Click on the "My New Device" device and navigate to the "Relations" tab.'
    3:
        image: /images/edge/getting-started/step-2-item-4.png
        title: 'Change direction "From" to "To" and see relation to the edge that has provisioned this device.'

step31:
    0:
        image: /images/edge/getting-started/step-1-item-1.png
        title: 'Open Device groups page in the ThingsBoard <b>Edge</b> instance.'
    1:
        image: /images/edge/getting-started/step-3-item-1.png
        title: 'Click on the device row in the table to open device details.'
    2:
        image: /images/edge/getting-started/step-3-item-2.png
        title: 'Click "Copy access token". Token will be copied to your clipboard. Save it to a safe place.'

step32:
    0:
        image: /images/edge/getting-started/step-3-item-1.png
        title: 'Click on the device row in the table to open device details.'
    1:
        image: /images/edge/getting-started/step-3-item-3.png
        title: 'Navigate to the "Latest telemetry" tab.'

step4:
    0:
        image: /images/edge/getting-started/step-4-item-1.png
        title: 'Open Rule chains page in the ThingsBoard <b>Edge</b> instance.'
    1:
        image: /images/edge/getting-started/step-4-item-2.png
        title: 'Open Edge Root Rule Chain.'
    2:
        image: /images/edge/getting-started/step-4-item-3.png
        title: '<b>Push to cloud</b> rule node pushes temperature timeseries data to the cloud once it is stored in local database.'

step51:
    0:
        image: /images/edge/getting-started/step-51-item-1.png
        title: 'Open <b>Dashboards</b> page in the ThingsBoard <b>Community Edition</b> server. Click on the "+" icon in the top right corner. Select "Create new dashboard".'
    1:
        image: /images/edge/getting-started/step-51-item-2.png
        title: 'Input dashboard name. For example, "My New Dashboard". Click "Add" to add the dashboard.'
    2:
        image: /images/edge/getting-started/step-51-item-3.png
        title: 'Now your dashboard should be listed first, since table sort dashboards using created time by default. Click on the "Open dashboard" icon.'

step52:
    0:
        image: /images/edge/getting-started/step-52-item-1.png
        title: 'Enter edit mode. Click on the pencil button in the bottom right corner.'
    1:
        image: /images/edge/getting-started/step-52-item-2.png
        title: 'Click "Entity Aliases" icon in the top right part of the screen. You will see empty list of Entity aliases.'
    2:
        image: /images/edge/getting-started/step-52-item-3.png
        title: 'Click "Add alias".'
    3:
        image: /images/edge/getting-started/step-52-item-4.png
        title: 'Input alias name, for example "MyDevice". Select "Single entity" Filter type. Select "Device" as Type and type "My New" to enable autocomplete. Choose your device from the auto-complete and click on the device.'        
    4:
        image: /images/edge/getting-started/step-52-item-5.png
        title: 'Click "Add" and then "Save".'        
    5:
        image: /images/edge/getting-started/step-52-item-6.png
        title: 'Finally, Click "Apply changes" in the dashboard editor to save the changes. Then you should enter edit mode again.'

step53:
    0:
        image: /images/edge/getting-started/step-53-item-1.png
        title: 'Enter edit mode. Click on the "Add new widget" button.'
    1:
        image: /images/edge/getting-started/step-53-item-2.png
        title: 'Select "Cards" widget bundle. Select "Latest values" tab. Click on the header of the Entities widget. The "Add Widget" window will appear.'
    2:
        image: /images/edge/getting-started/step-53-item-3.png
        title: 'Click "Add" to add the data source. Widget may have multiple data sources, but we will use only one in this case.'
    3:
        image: /images/edge/getting-started/step-53-item-4.png
        title: 'Select "MyDevice" entity alias. Then click on the input field to the right. The auto-complete with available data points will appear. Select "temperature" data point and click "Add".'        
    4:
        image: /images/edge/getting-started/step-53-item-5.png
        title: 'Resize the widget to make it a little bigger. Just drag the bottom right corner of the widget. You can also play with the advanced settings if you edit the widget.'

step54:
    0:
        image: /images/edge/getting-started/step-54-item-1.png
        title: 'Enter Edit mode.'
    1:
        image: /images/edge/getting-started/step-54-item-2.png
        title: 'Click "Add new widget" icon in the bottom right corner of the screen.'
    2:
        image: /images/edge/getting-started/step-54-item-3.png
        title: 'Click "Create new widget" icon.'
    3:
        image: /images/edge/getting-started/step-54-item-4.png
        title: 'Select "Charts" bundle. Scroll down and click on the "Timeseries - Flot" chart widget.'        
    4:
        image: /images/edge/getting-started/step-54-item-5.png
        title: 'Click "Add datasource" button.'
    5:
        image: /images/edge/getting-started/step-54-item-6.png
        title: 'Select "MyDevice" Alias. Select "temperature" key. Click "Add".'
    6:
        image: /images/edge/getting-started/step-54-item-7.png
        title: 'Drag and Drop you widget to desired space. Resize the widget. Apply changes.'
    7:
        image: /images/edge/getting-started/step-54-item-8.png
        title: 'Publish different telemetry values multiple times Step 2. Note that the widget displays only one minute of data by default.'
    8:
        image: /images/edge/getting-started/step-54-item-9.png
        title: 'Enter Edit mode. Open time selection window. Change the interval and aggregation function. Update the time window and apply changes.'

step6CE:
    0:
        image: /images/edge/getting-started/step-6-item-1.png
        title: 'Open Edge instances page in the ThingsBoard <b>Community Edition</b> server.'
    1:
        image: /images/edge/getting-started/step-6-item-2.png
        title: 'Click on the <b>Dashboards</b> button on the edge instance to open dashboards that are already assigned to this edge.'
    2:
        image: /images/edge/getting-started/step-6-item-3.png
        title: 'Click on the "+" icon and select "My New Dashboard" in the list. Now this dashboard is going to be provisioned to the edge.'

step6Edge:
    0:
        image: /images/edge/getting-started/step-6-item-5-edge.png
        title: 'Open "Dashboards" page in the ThingsBoard <b>Edge</b> UI. Open "My New Dashboard".'    
    1:
        image: /images/edge/getting-started/step-6-item-6-edge.png
        title: 'Verify that you see the same widgets that you have added on the cloud and temperature readings from the device.'

mqttWindows:
    0:
        image: /images/edge/getting-started/mqtt-windows-item-1.png
        title: 'Create new MQTT Client with the properties listed in screenshots below.'
    1:
        image: /images/edge/getting-started/mqtt-windows-item-2.png
        title: 'Populate the topic name and payload. Make sure the payload is a valid JSON document. Click "Publish" button.'

---

* TOC
{:toc}

{% assign currentThingsBoardVersion = "ThingsBoard Community Edition" %}

## Introduction

{% include templates/edge/getting-started/introduction.md %}

## Prerequisites

{% assign docsPrefix = "edge/" %}
{% include templates/edge/getting-started/prerequisites.md %}

## Step 1. Provision Device

{% include templates/edge/getting-started/step-1.md %}

## Step 2. Provision Device from ThingsBoard Edge to ThingsBoard Community Edition server (cloud)

{% include templates/edge/getting-started/step-2.md %}

## Step 3. Connect device

{% include templates/edge/getting-started/step-3.md %}

## Step 4. Push data from ThingsBoard Edge to ThingsBoard Community Edition server (cloud)

{% include templates/edge/getting-started/step-4.md %}

## Step 5. Create Dashboard

{% include templates/edge/getting-started/step-5.md %}

## Step 6. Provision Dashboard to ThingsBoard Edge

{% include templates/edge/getting-started/step-6.md %}

## Next steps

{% assign currentGuide = "GettingStartedGuide" %}
{% assign docsPrefix = "edge/" %}
{% include templates/edge/guides-banner-edge.md %}

## Your feedback

Don't hesitate to star ThingsBoard on **[github](https://github.com/thingsboard/thingsboard)** to help us spread the word.
If you have some questions about this sample - post it on the **[forum](https://groups.google.com/forum/#!forum/thingsboard)**.

