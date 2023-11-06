---
title: "Zemismart ZM25TQ control via MQTT"
description: "Integrate your Zemismart ZM25TQ via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-04-30T08:00:58
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Zemismart ZM25TQ

|     |     |
|-----|-----|
| Model | ZM25TQ  |
| Vendor  | [Zemismart](/supported-devices/#v=Zemismart)  |
| Description | Tubular motor |
| Exposes | cover (state, position), linkquality |
| Picture | ![Zemismart ZM25TQ](https://www.zigbee2mqtt.io/images/devices/ZM25TQ.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->



## Options
*[How to use device type specific configuration](../guide/configuration/devices-groups.md#specific-device-options)*

* `invert_cover`: Inverts the cover position, false: open=100,close=0, true: open=0,close=100 (default false). The value must be `true` or `false`

## Pairing
To set the device into pairing mode, click the button on the motor 3 times. The motor will do a short shake to comfirm pairing mode.

## Exposes

### Cover 
The current state of this cover is in the published state under the `state` property (value is `OPEN` or `CLOSE`).
To control this cover publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state": "OPEN"}`, `{"state": "CLOSE"}`, `{"state": "STOP"}`.
It's not possible to read (`/get`) this value.
To change the position publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"position": VALUE}` where `VALUE` is a number between `0` and `100`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

## Setting the Limits
Please see the following post: https://community.home-assistant.io/t/zemismart-zm25-zigbee-howto-tubular-roller-blind-shade-cover-motor/474992/16
