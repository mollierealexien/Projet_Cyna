# Ansible Playbooks pour Switchs Cisco

Ce projet contient des rôles et playbooks Ansible pour automatiser la configuration, la sécurité, le SNMP et la sauvegarde des switchs Cisco (Core et Distribution).

## Structure

- `roles/core_switch` : Rôle pour la configuration des switches Core
- `roles/distrib_switch` : Rôle pour la configuration des switches de Distribution
- `playbook_core.yaml` : Playbook principal pour les switches Core
- `playbook_distrib.yaml` : Playbook principal pour les switches Distribution
- `playbook_save_config.yaml` : Sauvegarde de la configuration
- `group_vars/`, `host_vars/` : Variables globales et spécifiques
- `hosts-all.ini` : Inventaire

## Utilisation

1. Adaptez l'inventaire (`hosts-all.ini`) et les variables dans `group_vars/` et `host_vars/`.
2. Lancez un playbook selon le besoin, par exemple :

```bash
ansible-playbook -i hosts-all.ini playbook_core.yaml
ansible-playbook -i hosts-all.ini playbook_distrib.yaml
ansible-playbook -i hosts-all.ini playbook_save_config.yaml
```

## Personnalisation

- Modifiez les rôles pour ajouter ou adapter des tâches selon vos besoins.
- Les tâches sont découpées par fonction pour une meilleure lisibilité et maintenance.

## Auteurs
- Projet Cyna
- Contact : mollierealexien
