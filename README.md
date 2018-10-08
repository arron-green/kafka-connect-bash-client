# KafkaConnect bash client

## Setup

This project depends on `jq` being installed and available within your `PATH`

### Install jq

```
brew install jq
```

### Update your local PATH

```bash
# add bin to path
export PATH="${PATH}:./bin"
```

## Create or Update job

```bash
kafka-connect-put-job ./jobs/s3-sink.properties "http://localhost:8083"
```

## Delete existing job

```bash
kafka-connect-rm-job "connect-s3" "http://localhost:8083"
```

## Other Operations

```bash
source ./bin/kafka-connect-ops

# get status of existing job
kafka-connect-job-status "connect-s3" "http://localhost:8083"
```
