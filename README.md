# Kubernetes-Projet-1

# Introduction

Ce projet a été réalisé pour permettre le déploiement d'un pod PHP et d'un pod MySQL en utilisant Kubernetes. Pour ce faire, j'ai utilisé le fichier "kustomization.yaml" pour partager le mot de passe de la base de données avec les deux pods. J'ai également créé deux services associés à chacun de ces pods pour faciliter l'accès à l'application.

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

3. Déployez les ressources Kubernetes :
```
kubectl apply -k .
```

# Fonctionnement

Lorsque vous avez déployé les ressources Kubernetes, deux pods sont créés : un pod PHP et un pod MySQL. Le fichier "kustomization.yaml" est utilisé pour partager le mot de passe de la base de données entre les deux pods.

De plus, deux services sont créés pour faciliter l'accès à l'application :

- Le service PHP permet d'accéder à l'application PHP.
- Le service MySQL permet d'accéder à la base de données MySQL.

Vous pouvez changer le mot de passe de la base de donnée en modifiant la valeur dans le fichier "kustomization.yaml" :
```
  literals:
  - password=redhat
```

# Conclusion

Félicitations ! Vous venez de déployer votre première application Kubernetes. J'espère que ce projet vous a permis de mieux comprendre le fonctionnement de Kubernetes et son utilisation pour déployer des applications.
