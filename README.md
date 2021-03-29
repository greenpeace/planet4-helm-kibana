[![Greenpeace](https://circleci.com/gh/greenpeace/planet4-helm-kibana.svg?style=shield)](https://circleci.com/gh/greenpeace/planet4-helm-kibana)

![Planet4](./p4logo.png)
# ElasticStack Kibana

Kibana is a free and open source UI that lets you visualise your ES data and
navigate the ElasticStack.  It is used to track the ES WP indexes and APM data.

<h1>Important Notes</h1>

>Ensure compatibility with:
- [Elasticsearch](https://github.com/greenpeace/planet4-helm-elasticsearch) 
- Elasticpress plugin in WP
- [ES-exporter](https://github.com/greenpeace/planet4-helm-esexporter)
- [APM-Server](https://github.com/greenpeace/planet4-helm-apm)

***
### Requirements - Internal Only
-   Access to P4 Infra [environment](https://www.notion.so/p4infra/bab9d0b1f2db4d929a59916899d531c1?v=eca7b78e1ae345c6883a9b37c6b76cac)

### Built with
- [kibana](https://github.com/elastic/helm-charts/tree/7.9/kibana) helm chart

### Deployment
This repository is deployed via [CircleCI](https://circleci.com/gh/greenpeace/planet4-traefik)

 - Commits to the develop branch trigger deployment to the development cluster.  
 - Create a PR for review to prepare for production deployment.
 - Approval and merge deploys to production.

### Usage
 - To access Kibana in develop use:
     `kibana.p4.greenpeace.org`
 - Clone the repo to access makefile commands via cli that are not executed via CircleCI
   - `make status` - <em> display status of named release </em>
   - `make value` - <em> display user values followed by all values deployed </em>
   - `make history` - <em> display deployment history of named release </em>
   - `make uninstall` - <em> delete release while retaining history, CRDs, PVs etc.</em>
   - `make destroy` - <em> destroy release including CRDs, PVs etc. </em> <strong> CAUSES DATA LOSS </strong>

 ### Infra Documentation
 - External
   - [Planet 4 Handbook](https://app.gitbook.com/@greenpeace/s/planet4/infrastructure/intro)
 - Internal use only
   - [P4 Notion](https://www.notion.so/p4infra/)

 ### Contributing
 If your interested in contributing to P4 Infrastructure code please check our our community page [here](https://github.com/greenpeace/planet4).

