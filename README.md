# Cours de Bioinformatique Appliquée
Ce dépôt GitHub contient les ressources nécessaires pour suivre le cours de bioinformatique appliquée basé sur l'article `Gut microbiota of preterm infants in the neonatal intensive care unit: a study from a tertiary care center in northern India` . Le cours utilise l'outil QIIME2 pour effectuer les analyses de données.
## Installation de QIIME2
### 1. Installation Conda
 Si vous n'avez pas déjà Conda, vous pouvez l'installer en suivant les instructions sur le [site officiel](https://gist.github.com/kauffmanes/5e74916617f9993bc3479f401dfec7da).
```bash
wget https://repo.continuum.io/archive/Anaconda3-5.2.0-Linux-x86_64.sh
bash Anaconda3-5.2.0-Linux-x86_64.sh
```
puis configurer votre environnement conda

```bash
conda config --set auto_activate_base false
```

```bash
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
conda config --set channel_priority strict
```
### 2. Création de l'environnement QIIME2 
Utilisez la commande suivante pour créer un environnement QIIME2 

```bash
conda env create -n qiime2-env --file envs/qiime2-amplicon-2024.2-py38-linux-conda.yml
```
Activer l'environnement conda

```bash
conda activate qiime2-env
```

Tester l'installation

```bash
qiime --help
```
