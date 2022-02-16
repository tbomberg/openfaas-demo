# openfaas-demo

Erste Schritte mit OpenFAAS

## Install faas-cli 
```
curl -sSL https://cli.openfaas.com | sh
```
or download from `https://github.com/openfaas/faas-cli/releases`

## Setup Environment

### URL of the Gateway

```
export OPENFAAS_URL=https://gateway-openfaas.devservices.onvpc.de
```

Login to the gateway:

```
faas-cli login -u admin -p <PASSWORD>
```

### Container Registry
```
export OPENFAAS_PREFIX=harbor.csvcdev.vpc.arvato-systems.de/openfaas
```

Login to the registry

```
faas-cli registry-login --username <ACCOUNT> --password <PASSWORD>
```

## Build and install a Python based function

### Setup a new function from a standard template
```
faas-cli new --lang python3 demo-api
```

### Write your Code

### Build, Push and Deploy
```
faas-cli up -f demo-api.yml
```

## Another sample (nodejs)