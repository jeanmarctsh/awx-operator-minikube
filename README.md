# INSTALLATION AWX-OPERATOR AVEC CLUSTER MINIKUBE

## SOMMAIRE

- [INSTALLATION AWX-OPERATOR AVEC CLUSTER MINIKUBE](#installation-awx-operator-avec-cluster-minikube)
  - [SOMMAIRE](#sommaire)
  - [📝 INTRODUCTION](#-introduction)
  - [🛠️ OUTILS UTILISES](#️-outils-utilises)
  - [🔧 PREREQUIS](#-prerequis)
  - [🏠 DEMO: INTERFACE D'ACCEUIL ET DASHBOARD AWX](#-demo-interface-dacceuil-et-dashboard-awx)
  - [🧰 QUELQUES COMMANDES](#-quelques-commandes)



## 📝 INTRODUCTION

De nos jours, nous voyons bel et bien comment les différents équipements sont interconnectés au sein d’une infrastructure informatique. Le suivi, la maintenance de ces derniers passent par l’utilisation de bons outils. Il existe plusieurs outils qui permettent d’assurer cette tâche critique dont notamment : GLPI, awx, etc… Dans le cadre de ce projet nous allons utiliser l’outil AWXOPERATOR

---

## 🛠️ OUTILS UTILISES

- OS: LINUX.
- KUBERNETES.
- VS_CODE.
- SSH.
- HYPERVISEUR type 2 : vmware_workstation.
- GITHUB
- DOCKER.

---

## 🔧 PREREQUIS

- OS : Ubuntu 22.04 LTS
- Disque : SSD 40 ou 60 GO
- RAM : 12GO
- HYPERVISEUR DE TYPE 1 ou 2

---

## 🏠 DEMO: INTERFACE D'ACCEUIL ET DASHBOARD AWX 


![interface d'acceuil et dashboard AWX](Demo/connexion%20à%20awx%20.mp4)

---

## 🧰 QUELQUES COMMANDES

Voici quelques commandes à exécuter sur AWX déployé avec Kubernetes avec la variante kubectl:
 
- Vérification des pods : 
  
```shell 
$ kubectl get pods
```
  
- Vérification des nodes : 

```shell 
$ kubectl get nodes
```

- Accéder à un pod : 
 
```shell 
$ kubectl exec -it nom_du_pod -- /bin/bash
```

Voici quelques commandes à exécuter sur AWX déployé avec Kubernetes avec la variante minikube kubectl: 

Démarrage du cluster minikube après installation :

```shell 
$ minikube start
```

Vérification des pods : 
  
```shell 
$ minikube kubectl -- get pods -A
```
  
- Vérification des nodes : 

```shell 
$ minikube kubectl -- get nodes -n <nom du namespaces>
```

- Accéder à un pod : 
 
```shell 
$ kubectl exec -it nom_du_pod -- /bin/bash 
```
```shell 
$ minikube kubectl -- exec -it nom_du_pod -n <nom_du_namespaces> -- bash
```

- Vérifier le nom de différents namespaces:
  
```shell 
$ minikube kubectl -- get namespaces
```

---



