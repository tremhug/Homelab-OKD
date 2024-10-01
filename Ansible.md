# Installation d'Ansible sur un Serveur Ubuntu

Ce guide explique comment installer Ansible sur un serveur Ubuntu avec les étapes détaillées.

## Prérequis
- Un serveur Ubuntu avec un accès `sudo`.
- Connexion à internet pour télécharger les paquets nécessaires.

## Étapes d'installation

### 1. Mettre à jour la liste des paquets et installer les dépendances

Ouvrir un terminal et exécuter les commandes suivantes :

```bash
sudo apt update
sudo apt install -y software-properties-common
```

### 2. Ajouter le dépôt officiel d'Ansible

Ajoutez le PPA (Personal Package Archive) officiel pour obtenir la dernière version d'Ansible :

```bash
sudo add-apt-repository --yes --update ppa:ansible/ansible
```

### 3. Installer Ansible

Installez Ansible en exécutant la commande suivante :

```bash
sudo apt install -y ansible
```

### 4. Vérifier l'installation

Pour vérifier qu'Ansible est correctement installé, utilisez la commande :

```bash
ansible --version
```

Vous devriez voir les informations sur la version d'Ansible installée.

### 5. Créer un fichier d'inventaire local (facultatif)

Si vous souhaitez tester Ansible sur le serveur local, créez un fichier d'inventaire simple :

```bash
sudo vi /etc/ansible/hosts
```

Ajoutez le contenu suivant pour configurer un inventaire de base :

```
[local]
localhost ansible_connection=local
```

Enregistrez le fichier, et Ansible est maintenant prêt à être utilisé pour des tests locaux.

## Ressources supplémentaires

- [Documentation Officielle d'Ansible](https://docs.ansible.com/)
- [Guide de démarrage rapide avec Ansible](https://docs.ansible.com/ansible/latest/user_guide/intro_getting_started.html)
