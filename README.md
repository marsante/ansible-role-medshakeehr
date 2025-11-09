MedShakeEHR Role
=========

Le rôle ansible qui permet d’installer MedShakeEHR. [Documentation](https://docs.brunoy-osteopathe.fr/medshakeehr/guides/installation/ansible/).

Requirements
------------

- ansible 2.9

Role Variables
--------------

| Nom                | Valeur par défaut                                      | Description                                                                                      |
|--------------------|--------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| country_name        | FR                                                     | Nom du pays                                                                                     |
| locality_name       | Paris                                                  | Nom de la ville                                                                                 |
| organization_name   | Dr Strange                                             | Nom de l’organisation                                                                           |
| email_address      | email@domain.tld                                       | Adresse e-mail                                                                                  |
| sql_root_password    | root                                                   | Mot de passe root pour SQL                                                                      |
| sql_user     | user                                                   | Nom du compte utilisateur SQL                                                                   |
| sql_user_password    | user                                                   | Mot de passe du compte utilisateur SQL                                                          |
| sql_database          | medshakeehr                                            | Nom de la base de données SQL                                                                   |
| msehr_base_release | 8.2.3                                                  | Version de MedShakeEHR                                                                  |
| msehr_base_repo_url| https://codeload.github.com/MedShake/MedShakeEHR-base/tar.gz/refs/tags/ | URL de MedShakeEHR                                          |
| msehr_base_checksum| sha256:bb2f7496daa01fdd5028ff4e60e8b997a768971c4b48ea8f59b405650ab3b07b | Checksum  de MedShakeEHR                                        |
| msehr_dir          | /var/www/ehr                                               | Chemin d’installation de MedShakeEHR                                                            |
| timezone           | Europe/Paris                                           | Fuseau horaire                                                                                   |
| domain             | msehr.local                                            | Nom de domaine                                                                                   |
| upload_max_filesize  | upload_max_filesize = 20M                              | Taille maximale des fichiers téléversés                                                         |
| post_maxsize        | post_max_size = 20M                                    | Taille maximale des données POST                                                                |
| max_input_vars       | max_input_vars = 10000                                 | Nombre maximal de variables d’entrée                                                             |
| error_reporting     |  ‘E_ALL & ~E_DEPRECATED & ~E_STRICT’    | Niveau de rapport d’erreurs                                                                      |
| display_errors      | ‘Off’                                   | Affichage des erreurs (Off : désactivé, On : activé)                                            |
| display_startup_errors| ‘Off’                           | Affichage des erreurs de démarrage (Off : désactivé, On : activé)                               |
| msehr_packages      | [‘acl’, ‘apache2’, ‘composer’, ‘curl’, ‘ghostscript’, ‘git’, ‘imagemagick’, ‘mariadb-server’, ‘ntpsec’, ‘pdftk-java’, ‘php’, ‘php-bcmath’, ‘php-curl’, ‘php-gd’, ‘php-gnupg’, ‘php-imagick’, ‘php-intl’, ‘php-json’, ‘php-mysql’, ‘php-soap’, ‘php-xml’, ‘php-yaml’, ‘php-zip’, ‘python3-mysqldb’, ‘python3-openssl’, ‘ufw’, ‘unattended-upgrades’ ] | Liste des packages requis pour MedShakeEHR |

Example Playbook
----------------


    - hosts: medshakeehr
      roles:
         - { role: marsante.medshakeehr }

License
-------

GPL v3

Author Information
------------------

- Auteur
[![](https://github.com/marsante.png?size=50)](https://github.com/marsante)
- Contributeurs
[![](https://github.com/indelog.png?size=50)](https://github.com/indelog)
