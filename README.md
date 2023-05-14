# Kubernetes-Projet-1

# Introduction

Ce projet a été réalisé pour créer une page web en PHP qui affiche le contenu d'une base de données MySQL. Pour cela, j'ai utilisé Kubernetes pour déployer un pod PHP et un pod MySQL, ainsi que deux services associés pour faciliter l'accès à l'application. Le fichier "kustomization.yaml" est utilisé pour partager le mot de passe de la base de données entre les deux pods.

# Fonctionnement

Une fois que vous avez déployé les ressources Kubernetes, deux pods sont créés : un pod PHP et un pod MySQL. Le fichier "kustomization.yaml" est utilisé pour partager le mot de passe de la base de données entre les deux pods.

La page web en PHP affiche le contenu de la base de données MySQL. Sur cette page web, il y a un champ texte dans lequel vous pouvez rentrer un nom et le valider. Une fois que vous avez validé le nom, celui-ci est ajouté à la base de données et s'affiche sur la page PHP.

De plus, deux services sont créés pour faciliter l'accès à l'application :

- Le service PHP permet d'accéder à l'application PHP.
- Le service MySQL permet d'accéder à la base de données MySQL.

# Prérequis

- Kubernetes doit être installé sur votre machine ou sur un cluster Kubernetes accessible.
- Un accès à la ligne de commande Kubernetes.

# Guide d'installation

1. Clonez ce dépôt sur votre machine locale :
```
git clone https://github.com/votre-nom/kubernetes-php-mysql.git
```

2. Accédez au répertoire du projet :
```
cd kubernetes-php-mysql
```

3. Modifiez le fichier "kustomization.yaml" pour définir le mot de passe de la base de données MySQL :
```
  literals:
  - password=redhat
```
Notez que le mot de passe par défaut est "redhat".

# Déployment des ressources Kubernetes


1. Déployer le fichier de Kustomization en utilisant le fichier suivant :
```
kubectl apply -k .
```

# Conclusion

Félicitations ! Vous venez de déployer votre première application Kubernetes qui affiche le contenu d'une base de données MySQL sur une page web en PHP. J'espère que ce projet vous a permis de mieux comprendre le fonctionnement de Kubernetes et son utilisation pour déployer des applications.
