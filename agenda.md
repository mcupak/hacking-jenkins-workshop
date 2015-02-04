# Agenda

## REST Export
- Read only
- Where to get help

### Flavors
- Xml
- Json
- Python

## REST
- Various URL exposed

- Task: build job

    ```curl -v http://localhost:8080/job/example_job/build```

- config.xml

- Task: Get node config.xml via REST API
    
    ```curl http://localhost:8080/computer/example_slave/config.xml > example_slave.xml```
    
- Task: Update number of executors on given node via REST API
    
    ```curl -v -X POST http://localhost:8080/computer/example_slave/config.xml -d @example_slave.xml```

## CLI

- Where to get help
- Usage: `java -jar jenkins-cli.jar -s $JENKINS_URL <command>`

- Task: Restart Jenkins instance via CLI

    ```java -jar jenkins-cli.jar -s http://localhost:8080 restart```

- Task: Get job config.xml via CLI

    ```java -jar jenkins-cli.jar -s http://localhost:8080 get-job example_job > example_job.xml```
  
- Task: Create new job from existing config

    ```java -jar jenkins-cli.jar -s http://localhost:8080 create-job new_job < example_job.xml```

- groovy, groovysh
- PKI
- https://wiki.jenkins-ci.org/display/JENKINS/Jenkins+CLI
- https://wiki.jenkins-ci.org/display/JENKINS/Jenkins+SSH
