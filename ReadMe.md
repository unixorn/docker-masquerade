# docker-masquerade

docker-masquerade is a collection of shim scripts that run commands in docker containers instead of natively. This makes it easier to move into a new machine - install the ZSH plugin, and `docker` will automagically download the container image the first time you use a given shim script.

## Contents

| Name              | Description                          | Credits          |
| ----------------- | ------------------------------------ | ---------------- |
| `c-mosquitto_pub` | Runs `mosquitto_pub` in a container. | Mine             |
| `c-mosquitto_sub` | Runs `mosquitto_sub` in a container. | Mine             |
| `c-influxdb`      | Run `influxdb` tool in a container.  | Mine             |
