https://www.emqx.com/en/blog/mqtt-and-kafka




The codebase consists of 3 parts:

- The emqx folder contains EMQX-Kafka integration configurations to create rules and data bridges when launching EMQX automatically.
- The emqx-exporter, prometheus and grafana-provisioning folders include observability configurations for EMQX.
- The docker-compose.yml orchestrates multiple components to launch the project with one click.


Start MQTTX CLI, EMQX, and Kafka
Please make sure you have installed the Docker, and then run Docker Compose in the background to start the demo:

docker-compose up -d
Now, 10 Tesla vehicles simulated by MQTTX CLI will connect to EMQX and report their status to the topic mqttx/simulate/tesla/{clientid} at a frequency of once per second.


### Instalar https://mqttx.app/downloads
https://mqttx.app/docs/cli/downloading-and-installation

```
anamarcacini in CarregadorBateria2/example on  main [!?] 
➜  curl -LO https://www.emqx.com/en/downloads/MQTTX/v1.9.10/mqttx-cli-linux-x64

  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   144    0   144    0     0    151      0 --:--:-- --:--:-- --:--:--   151
100 75.5M  100 75.5M    0     0  12.3M      0  0:00:06  0:00:06 --:--:-- 15.0M
anamarcacini in CarregadorBateria2/example on  main [!?] took 6,2s 
➜  sudo install ./mqttx-cli-linux-x64 /usr/local/bin/mqttx

anamarcacini in CarregadorBateria2/example on  main [!?] 
➜  mqttx --version   
1.9.10
https://mqttx.app/changelogs/v1.9.10
```
curl -LO https://www.emqx.com/en/downloads/MQTTX/v1.9.10/mqttx-cli-linux-x64
sudo install ./mqttx-cli-linux-x64 /usr/local/bin/mqttx

https://mqttx.app/downloads