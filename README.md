Role Name
=========

Creación de un servidor mediante el CLI hcloud y envío de los datos de acceso al puesto de usuario

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

Utilice sus servidores de correo para enviar cartas

    email:
      - host: smtp.gmail.com
        port: 587
        username: mail@gmail.com
        password: pass
        to: John Smith <name@domain.com>
        subject: New server was created.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    ---
    
    - hosts: localhost
      connection: local
      gather_facts: true
      become: true 
      vars_files:
        - /etc/ansible/roles/CREATE-server/defaults/main.yml
        - /etc/ansible/roles/CREATE-server/.travis.yml
    
      roles:
        - role: "/etc/ansible/roles/CREATE-server"

Agregar clave ssh al servidor
-------
Para acceder al servidor usando claves SSH, las claves generadas deben ser añadidas al servidor. Para añadir las llaves utilice el comando
```bash
hcloud ssh-key create --name [name of key] --public-key "ssh-ed25519 AAAAC3N...H6Ei0EUUKdp desarollo"
```

Author Information
------------------

Oleg Sidokhmtov
