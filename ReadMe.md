## Ansible
     -- Création d'un virtual host

     -- un script bash qui permet de lancer un playbook Ansible pour configurer des virtual hosts:

#!/bin/bash

if [ $# -eq 0 ]; then
  echo "Usage: \\$0 <file_path>"
  exit 1
fi

file_path="\$1"
ansible-playbook virtualhost_setup.yml -e "domain_names_file_path=$file_path"

     -- Configuration des hôtes virtuels sur un serveur avec Apache2

     -- virtual host template