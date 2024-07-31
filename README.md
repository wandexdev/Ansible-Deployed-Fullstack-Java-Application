# Ansible-Deployed-Fullstack-Java-Application

## Folder Structure
```
Ansible-Deployed-Fullstack-Java-Application/
|--- .gitignore
|--- README.md
|--- ansible.cfg
|--- group_vars
|    |--- hng.yml
|--- hosts
|--- main.yml
|--- mybeloved.yml
|--- roles
|    |--- common
|    |    |--- handlers
|    |    |    |--- main.yml
|    |    |--- tasks
|    |    |    |--- main.yml
|    |--- java_app
|    |    |--- tasks
|    |    |    |--- main.yml
|    |--- nginx
|    |    |--- tasks
|    |    |    |--- main.yml
|    |--- postgresql
|    |    |--- handlers
|    |    |    |--- main.yml
|    |    |--- tasks
|    |    |    |--- main.yml
|    |    |--- vars
|    |    |    |--- main.yml
|    |--- rabbitmq
|    |    |--- tasks
|    |    |    |--- main.yml
|    |    |--- templates
|    |    |    |--- rabbitmq.config.j2
|    |    |--- vars
|    |    |    |--- main.yml
|--- templates
|    |--- application.properties.j2
|    |--- nginx_stage_5b.conf.j2
|    |--- pom.xml.j2
|    |--- stage5b.service.j2

```

## Usage
- Create a `hosts` or `inventory` file. Can be named anything, it would contain slave hosts name or ip address and private key for ssh(if needed)
```env
# sample hosts file

[hng]
52.91.184.189

[hng:vars]
ansible_user=ubuntu
ansible_ssh_private_key_file=/home/ubuntu/ubuntu-sterling.pem
```

- Create your `ansible.cfg` file. This eliminates the ned for an appended inventory/host file in the command.
```cfg
# sample ansible.cfg file

[defaults]
inventory=./hosts
```

- Git Clone my repository to get the neccessary configuration
```shell
:-$ git clone https://github.com/wandexdev/Ansible-Deployed-Fullstack-Java-Application
```
- Kindly adjust the folder structure as shown above as some files were not pushed to version control

- Run the playbook
```shell
ansible-playbook main.yml -b
```
