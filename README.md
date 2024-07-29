# Ansible-Deployed-Fullstack-Java-Application

## Folder Structure
```
|--- main.yml
|--- roles
|    |--- postgresql
|    |    |--- tasks
|    |    |    |--- main.yml
|    |    |--- templates
|    |    |    |--- postgresql.conf.j2
|    |    |    |--- pg_hba.conf.j2
|    |    |--- vars
|    |    |    |--- main.yml
|    |--- rabbitmq
|    |    |--- tasks
|    |    |    |--- main.yml
|    |    |--- templates
|    |    |    |--- rabbitmq.config.j2
|    |    |--- vars
|    |    |    |--- main.yml
|    |--- java_app
|    |    |--- tasks
|    |    |    |--- main.yml
|    |    |--- templates
|    |    |    |--- application.properties.j2
|    |    |--- vars
|    |    |    |--- main.yml
```

## Usage
