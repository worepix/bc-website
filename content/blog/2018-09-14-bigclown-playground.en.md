---
date: "2018-09-14"
title: "BigClown Playground"
description: "The new multi-platform graphical application to manage all BigClown devices."
images:
    preview: "preview.png"
    main: "main.png"
author:
    name: "Martin Hubáček"
    post: "Firmware Designer"
    email: "martin.hubacek@hardwario.com"
    image: "martin.jpg"
---

We have released a new graphical application [**BigClown Playground**](https://github.com/bigclownlabs/bch-playground/releases) which contains everything you need in a one package. Create rules and flows in the Node-RED, upload new firmware to the **Core Module 2**, manage the radio paired nodes.

[**Download**](https://github.com/bigclownlabs/bch-playground/releases) and try out [**BigClown Playground**](https://github.com/bigclownlabs/bch-playground/releases) now. It's multi-platform and runs on Windows, Linux and macOS. You can have your radio network with nodes up and running in a minutes. Take a look at the [**Quick Start Guide**]({{< relref "/doc/basics/quick-start-guide.en.md">}}) where the basics are explained.

Later, for a more permanent solution, you can use the **{{<shop "BigClown Hub">}}** that is pre-programmed and comes also with {{<shop "Radio Dongle">}}. Or you can flash our [**bc-raspbian**]({{< relref "/doc/tutorials/custom-setup-on-raspberry-pi.en.md">}}) to your Raspberry Pi 3 computer.

### Playground contains:

* **Home** - help page that will guide you how to get started
* **Functions** - Node-RED flows editor where you define the rules
* **Dashboard** - Dashboard page where all your values can be visualized and controlled
* **Messages** - See all the messages that BigClown devices sends by the radio
* **Firmware** - Reprogram you Core Modules with one of many pre-programmed firmwares
<div class="container img-container">
  <div class="row">
    <div class="col-sm">
      {{< img-zoom src="dashboard.png" >}}
    </div>
    <div class="col-sm">
       {{< img-zoom src="node-red.png" >}}
    </div>
  </div>
  <div class="row">
    <div class="col-sm">
       {{< img-zoom src="devices.png" >}}
    </div>
    <div class="col-sm">
       {{< img-zoom src="flash.png" >}}
    </div>
  </div>
</div>

### More technical stuff:

BigClown Playground is using an Electron. It is basically a web application with server and web browser in a single package. The backend runs on NodeJS. The Node-RED is already written in NodeJS so it is running "natively". For MQTT we had to leave Mosquitto and use also NodeJS variant. The MQTT server runs on port 1883 but can be reached also over Websockets.

The `bcg` gateway and `bcf` flasher had to be rewritten to the NodeJS.
