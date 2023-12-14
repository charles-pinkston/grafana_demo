# Grafana Demo

## Introduction
This project is a simple demonstration of setting up a Grafana instance that can be used to provide an analytics view of system data to customers.

### Getting Started

1. Run `docker-compose up -d` to create a MySQL DB and a Grafana instance
2. Visit the Grafana instance by going to: http://127.0.0.1:3000

#### Behind the Scenes
The docker compose does a couple of things:
* MySQL
  * It volume mounts the sample DB from /data and automatically deploys it
* Grafana
  * Provisions the instance  
     * Creates the `Demo DB` Configuration to connect Grafana to the DB
       * Configuration in `/provisioning/datasources/datasource.yml`
     * Creates some sample Dashboards to display data from the Datasource
       * Configuration in `/provisioning/dashboards/dashboard.yml`

## Additional Resources:

### Grafana:
1. Provisioning: https://grafana.com/docs/grafana/latest/administration/provisioning/
2. Configuration: https://grafana.com/docs/grafana/latest/setup-grafana/configure-grafana
   3. This lists the values that can be overridden by Environment Variables

### DB Data:
Sample DB data comes from:
https://www.mysqltutorial.org/mysql-sample-database.aspx