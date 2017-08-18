# Pivotal Workshop

## config-server

Application which runs as config server

## greeting-config

### Deploy to CF

```
cf create-service p-config-server standard config-server -c ./cfg-svr-config.json
cf push
```
