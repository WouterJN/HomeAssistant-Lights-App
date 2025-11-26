
# HomeAssistant - Lights App

Custom component that allows control of lights by [Lights App](https://play.google.com/store/apps/details?id=com.novolink.lightapp&hl=en_US)

<p float="left">
  <img src="/img/img2.jpeg" width="200" />
  <img src="/img/img1.jpeg" width="200" /> 
</p>

## Installation

Copy contents of custom_components/lights_app/ to custom_components/lights_app/ in your Home Assistant config folder.

## Installation using HACS

Add this repository as custom repository.

HACS is a community store for Home Assistant. You can install [HACS](https://github.com/custom-components/hacs) and then install Lights App from the HACS store.

## Supported devices

Currently the 48m and the 5.5m variant are supported. If your device does not show up, check the available Bluetooth devices on your phone and add the name to the `SUPPORTED_BLUETOOTH_NAMES` in the `const.py` and please open PR.

## Usage

Integration allows setting brightness, controlling state and all the available modes.

<p float="left">
  <img src="/img/img3.png" width="400" />
</p>

## Recent improvements

- Coordinator refreshes now ask the controller for light and mode status only when Home Assistant is waiting on state, mode, or brightness data. This trims unnecessary BLE chatter that could cause momentary flickers during routine polling.
- When the Bluetooth link drops, state, mode, and brightness are marked as pending so the next reconnect performs a one-time resync. Entities recover their values without the rapid-fire polling writes that might trigger flashes.

## Have a comment or a suggestion?

Please [open a new issue](https://github.com/JurajNyiri/HomeAssistant-Lights-App/issues/new/choose), or discuss on [Home Assistant: Community Forum](https://community.home-assistant.io/t/custom-component-lights-app-bluetooth-outside-christmas-lights/654770).

## Thank you

<a href="https://www.buymeacoffee.com/jurajnyiri" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" alt="Buy Me A Coffee"  width="150px" ></a>
