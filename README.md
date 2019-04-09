ansible-consul
=======================

Rôle de déploiement de l'agent du supervision consul.

Pré-requis
----------

N.A.

Variables
---------

Les options de base sont pré-remplies pour la production :

* ```consul_package_state```: les paquets sont-ils présents ou à jour ? Par défaut à "present"
* ```consul_dns_domain```: Nom de domaine utilisé quand on interroge consul en protocole DNS. Par défaut "consul"
* ```consul_datacenter```: Nom du centre de calcul. Par défaut "dc1"

Dépendances
-----------

Aucune.

Exemples
--------

Utilisation minimale :

    - hosts: servers
      roles:
         - { role: ansible-consul }
      vars:
        consul_consul_cluster: consul-cluster.si1a

Mise en place d'un serveur :

    - hosts: servers
      roles:
         - { role: ansible-consul }
      vars:
        consul_server_mode: true

License
-------

GPL-3+

Author Information
------------------

Mathieu GRZYBEK
