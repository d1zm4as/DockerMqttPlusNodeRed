# DockerMqttPlusNodeRed

Docker Compose setup for Node-RED integrated with an Eclipse Mosquitto MQTT broker.

## Services

- `nodered` (`nodered/node-red`)
  - exposed on host port `80` (container `1880`)
- `mosquitto` (`eclipse-mosquitto`)
  - MQTT: `1883`
  - WebSocket: `9001`
  - config mounted from `./mosquitto/mosquitto.conf`

## Run

```bash
docker compose up -d
```

## Notes

Both services are attached to the `mynet` bridge network.
