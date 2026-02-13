# Spin up a Chainlink Node with Docker Compose

This lab demonstrates how to run a local Chainlink node using Docker Compose.

## Prerequisites

Install Docker Desktop

Make sure Docker Desktop is running (whale icon is green)

Verify installation:

```
docker --version
docker compose version
```

Both commands must return version numbers.

## Step 1 – Clone Repository

```
git clone <YOUR_REPO_URL>
cd chainlink-node-lab
```

## Step 2 – Create Environment File

```copy .env.example .env```


Edit the following values:

```
ETH_WS_URL=
ETH_HTTP_URL=
```

Save and close the file.

## Step 3 – Start the Node


```
docker compose up -d
```

Open your browser:

http://localhost:6688

Login using the email and password defined in .env.


## Clean Up the resources

To completely remove containers and all data:

docker compose down -v --remove-orphans

Then start again:

docker compose up -d

Useful Commands

## View logs:

docker logs -f chainlink

Stop containers (keep data):

docker compose down

