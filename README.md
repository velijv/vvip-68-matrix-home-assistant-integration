# Integrate **[WiFi panels / garlands on esp8266 by vvip-68](https://github.com/vvip-68/GyverPanelWiFi) with Home Assistant**

This integration is built on a set of automations for Home Assistant and allows you to control the matrix and configure most of the parameters.

### Appearance

![](https://github.com/tarasifua/vvip-68-matrix-home-assistant-integration/blob/main/screenshot/screenshot.png?raw=true)

### Installation

In your `configuration.yaml` file, add the lines that are in the file of the same name in the repository. If you already have `input_boolean`, `input_number`, `input_text`, `input_select`, `sensors` or `script` files included, transfer the contents of these files to your own.

Place the `matrix_automations` folder in your automations folder.

The contents of the `ui-lovelace.yaml` file are also transferred to your Lovelace settings file.

Also, to display parameter settings cards with `+` and `-` buttons, you need to install the [numberbox-card](https://github.com/htmltiger/numberbox-card) component, the easiest way to do this is through [HACS](https ://hacs.xyz/)

### Setting

For the integration to work correctly, the matrix must send messages to the MQTT server in the `WiFiPanel-0` topic, and the batch mode for passing parameters in the matrix firmware must be disabled (file `a_def_soft.h`, variable `bool mqttstatepacket = false;)`