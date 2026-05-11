# Eglo 99099 remote blueprint

Home Assistant blueprint for the Eglo connect.z 99099 Zigbee remote using raw Zigbee2MQTT MQTT payloads (`action` + `action_group`).

## Note

The two favorite buttons (heart) cannot be used via a Zigbee network, as the remote control only sends these events directly to the light when directly paired with an EGLO light.


[![Open your Home Assistant instance and import this blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/Mattti0/Eglo-99099-remote-blueprint/main/blueprints/automation/mattti0/eglo_99099_raw_zigbee2mqtt.yaml)

Blueprint file:
- `blueprints/automation/mattti0/eglo_99099_raw_zigbee2mqtt.yaml`

## References
- Zigbee2MQTT device documentation: https://www.zigbee2mqtt.io/devices/99099.html

- Original blueprint inspiration: https://community.home-assistant.io/t/eglo-99099-remote-blueprint/858066
