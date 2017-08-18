# Pivotal Workshop

## config-server

Application which runs as config server

## greeting-config

### Deploy to CF

```
cd greeting-config
cf create-service p-config-server standard config-server -c ./cfg-svr-config.json
cf push
```
