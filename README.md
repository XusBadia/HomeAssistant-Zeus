[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs) 

# Zeus Icon Set

Zeus Icon Set for Home Assistant

![2FA](https://github.com/XusBadia/zeus-icon-set-ha/blob/master/docs/zeus-ha-main.png)

 ---
## Icon List

You can find a list of the icons in the official website: [Zeus Icon Set](https://xus.badia.me/zeus)

Here's a cheatsheet with all the icon names: [Zeus Icon Set Cheatsheet](https://badia.me/zeus/cheatsheet/)


# Install

## HACS

I recommend installing Zeus Icon Set via [Home Assistant Community Store](https://hacs.xyz)
 
 1. Add the folowing to the `frontend` section of your `configuration.yaml`

  ```yaml
frontend:
  extra_module_url:
    - /local/community/HomeAssistant-Zeus/HomeAssistant-Zeus.js
```
2. (optional) Or add the following to your lovelace configuration using the Raw Config editor under Configure UI or ui-lovelace.yaml if using YAML mode.

```yaml
resources:
  - type: js
    url:  /local/community/HomeAssistant-Zeus/HomeAssistant-Zeus.js
```

 ##  Manual Installation

To add custom repositories please follow [this guide](https://hacs.xyz/docs/faq/custom_repositories/). Set URL to `https://github.com/XusBadia/HomeAssistant-Zeus` and category to `Lovelace`.
1. Download `HomeAssistant-Zeus.js` file from the [latest release](https://github.com/XusBadia/HomeAssistant-Zeus/releases/latest).
2. Copy the `HomeAssistant-Zeus.js` file into `<config>/www/` the directory where your `configuration.yaml` resides.

3. Add the folowing to the `frontend` section of your `configuration.yaml`

```yaml
frontend:
  extra_module_url:
    - /local/HomeAssistant-Zeus.js
```

Or add the following to your lovelace configuration using the Raw Config editor under Configure UI or ui-lovelace.yaml if using YAML mode.

```yaml
resources:
  - type: js
    url: /local/HomeAssistant-Zeus.js
```

Restart home-assistant.

## Use
you can use icons by entering the prefix `zeus:`

Example of integration in the card

```yaml
entities:
  - entity: light.bathroom
    icon: 'zeus:bath'
    name: Bathroom
  - entity: light.cleaning_closet
    icon: 'zeus:broom'
    name: Cleaning Closet
show_header_toggle: false
title: Zeus icons
type: entities
```
# Customize the prefix

In case you want to create your own perfix you can edit the last line of the `HomeAssistant-Zeus.js`

```js
  window.customIconsets["yourprefix"] = getIcon;
```
# Don't see the icon?

It probably depends on the cache. Open Home assistant from an incognito window and check that the icon loads if yes then it depends on the cache, otherwise double check the installation


_Special thanks to Emanuele (https://github.com/elax46/custom-brand-icons) since I took his Custom Brand Icons for HACS repository to get this one to work._