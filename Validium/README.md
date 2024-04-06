# CDK validium on your local machine that sets up and runs the following components:

- zkEVM databases:
  - Data node
  - Event
  - Explorer L1 and L2
  - Pool
  - State
  - Bridge service

- zkEVM node components:
  - Aggregator
  - Approve service
  - Sequencer and sequence sender
  - Sync

- L1 network (mock)

- Prover

- Explorers L1, L2

- JSON RPC explorer

- L2 gas pricer

- DAC: Data availability service

- zkEVM bridge service and UI
## Prerequisites
### Hardware
- A Linux-based OS (e.g., Ubuntu Server 22.04 LTS).
- At least 16GB RAM with a 4-core CPU.
- An AMD64 architecture system.
### Software
- Docker
- Docker Compose

## 1. Clone the repo
```
sh script.sh 
```
### Create the .env file by copying the example:
```
Validium\.env
```
## 2. Launch validium locally

#### 2.1 Start your local CDK validium:
```
sudo make run
```
#### 2.2 To ensure all services are running properly, check the status of each container:
```
docker compose ps
```
#### 2.3 Investigate further using the logs:
```
sudo docker compose logs <container_name>
```
#### 2.4 Useful commands

To stop CDK validium, use:
```
sudo make stop
```
To restart all services:
```
sudo make run-resume
```
To check all running or exited services, use:
```
sudo make ps
sudo make ps-exited
```
## 3. Test validium¶

Verify the block explorer is running by navigating to localhost.

[QuickStart](https://docs.polygon.technology/cdk/get-started/quickstart-validium/)