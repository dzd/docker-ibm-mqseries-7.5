# docker-ibm-mqseries-7.5
IBM MQSeries 7.5 on Ubuntu 16.04

## Run container
```bash
docker run -d \
    --name ibm-mqseries \
    -e MQ_QMGR_NAME=QM1 \
    -p 1414:1414 \
    0dittyspace/ibm-mqseries:latest
```

## Run container with custom file
```bash
docker run -d \
    --name ibm-mqseries \
    -e MQ_QMGR_NAME=QM1 \
    -p 1414:1414 \
    -v /home/user/listener.mqsc:/etc/mqm/listener.mqsc \
    0dittyspace/ibm-mqseries:latest
```

## Run Mqsc console 
```bash
docker exec -ti ibm-mqseries /opt/mqm/bin/runmqsc
```