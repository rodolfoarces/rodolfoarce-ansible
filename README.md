# Ansible

## Directorios

* **files**: Directorio, subidivididos en los servicios que corresponden, con los archivos que se copian al host
* **inventory**:Directorio que contiene la lista de hosts divididos en los diferentes invenatiorios disponibles
* **playbooks**:Directorio, subdivididos en las plataformas que corresponden, con los diferentes playbooks a ejecutar.

## Ejecución

Requiere la instalación del ejecutable ansible-playbook

```
ansible-playbook -i ~/proyectos/rodolfoarce-ansible/inventory/rodolfoarce-hosts.yml -l web00.rodolfoarce.local -u root ~/proyectos/rodolfoarce-ansible/playbooks/ubuntu/ubuntu-2204-docker.yml
```

