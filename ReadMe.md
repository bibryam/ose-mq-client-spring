# Camel Spring ActiveMQ Client Demo

A Camel Spring client for ActiveMQ Broker.


### Start an ActiveMQ Broker

    oc new-project amq-demo

    oc policy add-role-to-user view system:serviceaccount:amq-demo:default

    oc process -f amq62-basic.json -v MQ_USERNAME=admin,MQ_PASSWORD=admin | oc create -f -

### Build the project

    mvn clean install -s configuration/settings.xml
    mvn -Pf8-local-deploy -s configuration/settings.xml
