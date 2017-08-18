# Pivotal Workshop

## config-server

Application which runs as config server

## greeting-config

### Deploy to CF

* Simple Deploy

```
cd greeting-config
cf create-service p-config-server standard config-server -c ./cfg-svr-config.json
cf create-service cloudamqp lemur cloud-bus
cf push
```

Note: Cloud Bus helps when you are running multiple Cloud Foundry instances and you do not have control over which instances you hit when sending the /refresh POST request due to load balancing provided by the router. It steps in and syncs all instances on refresh


* Changing spring profile

```
cf set-env greeting-config SPRING_PROFILES_ACTIVE qa
```

## fortune-service

### Deploy to CF

* Simple Deploy

```
cd fortune-service
cf create-service p-service-registry standard service-registry
cf push
```

## greeting-service

* Simple Deploy

```
cd fortune-service
cf push
```