# Ansible

**Ubuntu**

La instalación de los paquetes de software en ubuntu es utilizando el siguiente comando

```
sudo apt install ansible
```

**CentOS/Rocky/RedHat**

La instalación de los paquetes en Red Hat y similares es utilizando el siguiente comando

```
sudo yum install ansible
```

## Directorios

* **files**: Directorio, subidivididos en los servicios que corresponden, con los archivos que se copian al host
* **inventory**:Directorio que contiene la lista de hosts divididos en los diferentes invenatiorios disponibles
* **playbooks**:Directorio, subdivididos en las plataformas que corresponden, con los diferentes playbooks a ejecutar.

## Ejecución

Requiere la instalación del ejecutable ansible-playbook

```
ansible-playbook -i ~/proyectos/rodolfoarce-ansible/inventory/rodolfoarce-hosts.yml -l web00.rodolfoarce.local -u root ~/proyectos/rodolfoarce-ansible/playbooks/ubuntu/ubuntu-2204-docker.yml
```

## Troubleshooting

La mayoría de los errores de ejecución en Ansible estan relacionados con el acceso al host remoto por SSH.

* Error de autenticación : La máquina remota no permite autenticación con contraseña, sólo con llave pública/privada.
* Error de permisos: El usuario de conexión a la máquina no tiene permisos para ejecutar los playbooks por que no puede escalar privilegios con sudo

