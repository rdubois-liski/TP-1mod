# packer-course-bootstrap
## Avant de commencer

- N'oublier pas de rajouter dans le repertoire l'OS de rocky necessaire au fonctionnement du TP

- Si present, veuillez retirer le dossier Build-Rocker-8

- Veuillez installer ansible-collection-ansible-posix sur la VM principal

## Kickstart 

#### Générer le mot de passe de root

```bash
openssl passwd -6
```
La suite de caractére obtenu est a spécifier de la maniére suivante :
```ks
rootpw --iscrypted <password>
```


## Debug

#### Augmenter le niveau de log de packer

Avant de lancer Packer définissez la variable d'environnement 'PACKER_LOG'.

```bash
export PACKER_LOG=1
```
#### Augmenter le niveau de log d'Ansible
Dans votre fichier PAcker, ajouter la configuration suivante au provisionner d'Ansible.

```hcl
    extra_arguments = [ "-vv" ]
```# TP-1
