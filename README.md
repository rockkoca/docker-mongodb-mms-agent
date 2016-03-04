mongodb-mms-agent
---

# Why

We needed a better way to monitoring mongodb in our environment. This Docker will allow you use the MongoDB monitoring agent to make that job.

## MongoDB Monitoring Agent

The Cloud Manager Monitoring Agent is a lightweight component that runs within your infrastructure, connects to your MongoDB processes, collects data about the state of your deployment, and then sends the data to Cloud Manager, which processes and renders the data.

MongoDB Monitoring Agent need `munin-node` running in the same host to collect hardware statistics, like cpu, memory, disk.

This Docker run both `mongodb-mms-agent` and `munin-node`.

## Run this container

        docker run --name mongodb-mms-agent --env "MMS_API_KEY=YOUR_MMS_KEY" --privileged --net=host neowaylabs/mongodb-mms-agent


> Note: You need change YOUR_MMS_KEY
