# The Qlik Core Workshop

Welcome to the Qlik Core Workshop. This repository will give a step-by-step
walkthrough of getting up and running with Qlik Core and the QIX Engine API.

This repository is sorted by branches. The `master` branch is the first step in the tutorial
and each branch is numbered to indicate where to go next. There are also pull requests in
this repo to indicate the changes that have occurred between each branch to give an easy view
of what has been implemented.

This workshop is run with Node.JS, however the QIX Engine API is a websocket API so any language
that supports websockets can talk to the QIX Engine.

## Prerequisites

In order to take full advantage of this workshop the following technologies should be installed and working on your system

- Node.js (the latest LTS version)
- npm/yarn
- Docker Desktop

## Step 1 - Running the Qlik Core docker image

1. ensure docker desktop is running.
2. run the following command from a terminal: `ACCEPT_EULA=yes docker-compose up -d`.
  - `ACCEPT_EULA=yes` indicates that you accept the end user license agreement for Qlik Core.
  - `docker-compose up -d` runs the Docker Compose CLI that reads the **docker-compose.yml**
    file and gets the docker image up and running.
3. wait a few seconds and run `docker ps` to ensure the image is running. you should see a line
   that includes `qlikcore/engine` under the IMAGE header.