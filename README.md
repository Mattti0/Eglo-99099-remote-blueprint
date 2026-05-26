# Eglo 99099 remote blueprint
[![Open your Home Assistant instance and import this blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/Mattti0/Eglo-99099-remote-blueprint/main/blueprints/automation/mattti0/eglo_99099_raw_zigbee2mqtt.yaml)

Home Assistant blueprint for the Eglo connect.z 99099 Zigbee remote using raw Zigbee2MQTT MQTT payloads (`action` + `action_group`).

## Note

The two favorite buttons (heart) cannot be used via a Zigbee network, as the remote control only sends these events directly to the light when directly paired with an EGLO light.


## Setup

🔃 Button could be used to easily toggle between scenes

### Step 1: Create a state machine (Input Select helper)

This acts as memory for which scenario is currently active.

1. Go to Home Assistant: Settings → Devices & Services → Helpers
2. Select Create Helper and search for Dropdown (Input Select)
3. Give it a descriptive name, e.g., Living Room State
4. Add your scenario names one by one in the Options field (e.g., Normal, Movie, Reading, Dark)
5. Save

### Step 2: Automation to control the state machine (Remote button press)

This automation reacts to the "refresh" button press and moves the dropdown to the next option.

1. Go to Settings → Automations & Scenes → Create Automation
2. **Trigger**: Select State trigger and choose the helper you created in Step 1 (Living Room State). This will trigger whenever the state changes
3. **Action**: Add your desired actions based on the helper's state (e.g., control lights, activate scenes, etc.)
4. **Optional**: Use conditions to check the current state and execute different actions accordingly

Blueprint file:
- `blueprints/automation/mattti0/eglo_99099_raw_zigbee2mqtt.yaml`

## References
- Zigbee2MQTT device documentation: https://www.zigbee2mqtt.io/devices/99099.html

- Original blueprint inspiration: https://community.home-assistant.io/t/eglo-99099-remote-blueprint/858066
