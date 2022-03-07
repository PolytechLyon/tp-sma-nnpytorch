# TP1 Réseaux de neurones & PyTorch

Vous trouverez dans ce dépôt :
* Les slides du CM1
* Les notebooks associés au CM: CM1-1DeepRL.ipynb et CM1-2DeepRL.ipynb
* Le notebook à compléter pour ce TP: TP1/TP1-Tuto.ipynb

## 1. Récupération du projet sur GitHubClassroom


1. Les 2 étudiants du binôme (nom1 et nom2) doivent avoir un compte github. Si ce n’est pas le cas, créer un compte sur [github](https://github.com).
2. Un seul des 2 étudiants du binôme (nom1) clique sur le lien de l’assignment des TPs donné en cours.

3. Avec ce lien, l’étudiant nom1 accepte l’invitation et **crée une team** nommée `nom1-nom2`. Le nom du dépôt sera alors : `tpsma-nn-pytorch-nom1-nom2`. 
4. Le second étudiant nom2 du binôme doit alors:
* Le plus simple:  cliquer sur l’assignment. Il choisit alors de joindre la team existante : `nom1-nom2`.
* Soit l’étudiant nom1 ajoute `nom2` à la team `nom1-nom2`. L'étudiant `nom2`  recoit alors une invitation. L’étudiant `nom2`  accepte l’invitation : dans github, l’étudiant `nom2`  voit la team, et peut modifier le dépôt. L’étudiant `nom2`  ne voit le dépôt que lorsqu’il a fait une modification.

## 2. Installation

[Conda](https://docs.conda.io/en/latest/) est un système de gestion de package permettant l'installation de multiples versions de logiciels au travers d'un mécanisme d'**environnements virtuels**. Vous pouvez ainsi isoler vos différents projets Python dans des environnements virtuels différents. Chaque environnement virtuel utilisera la version souhaitée de Python et des packages associés pour votre projet.

> Conda is an open source package management system and environment management system 
for installing multiple versions of software packages and their dependencies and 
switching easily between them. It works on Linux, OS X and Windows, and was created 
for Python programs but can package and distribute any software.



### 2.1. Installation d'Anaconda ou de miniconda

Vous pouvez au choix installer [Anaconda](https://www.anaconda.com/products/individual), qui contient le gestionnaire de paquet Conda, plus les bibliothèques scientifiques, un environnement de développement … ou uniquement le gestionnaire de paquet Conda appelé [Miniconda](https://docs.conda.io/en/latest/miniconda.html).

Pour Anaconda, suivez les consignes sur leur site. Pour Miniconda, suivez les consignes ci-dessous:

> [Miniconda](https://docs.conda.io/en/latest/miniconda.html) is a free minimal installer for conda. 

**Télécharger** la denrière version de`miniconda` correspondant à votre système.

|        | Linux | Mac | Windows | 
|--------|-------|-----|---------|
| 64-bit | [64-bit (bash installer)][lin64] | [64-bit (bash installer)][mac64] | [64-bit (exe installer)][win64]
| 32-bit | [32-bit (bash installer)][lin32] |  | [32-bit (exe installer)][win32]

[win64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe
[win32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86.exe
[mac64]: https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
[lin64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
[lin32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86.sh

**Installer** [miniconda](http://conda.pydata.org/miniconda.html) sur votre machine:

- **Linux:** https://conda.io/projects/conda/en/latest/user-guide/install/linux.html
- **Mac:** https://conda.io/projects/conda/en/latest/user-guide/install/macos.html#install-macos-silent
- **Windows:** https://conda.io/projects/conda/en/latest/user-guide/install/windows.html

### 2.2. Creation et activation d'un environnement

Dans la suite, 
* pour Mac et Linux, les commandes sont à faire dans un terminal classique. 
* Pour Windows, il faut utiliser **Anaconda prompt** et pas un terminal de commande classique (taper "Anaconda Prompt" dans la barre de recherche Windows). 

Pour tous les OS:

1. Créer (et activer) un nouvel environnement, appelé `nnPyTorch` avec Python 3.6. 

```
conda create --name nnPyTorch python=3.6
conda activate nnPyTorch
```

A ce niveau, votre ligne de commande doit ressembler à : `(nnPyTorch) <User>: `. `(nnPyTorch)` indique que l'environnement créé est actif, et vous pouvez maintenant installer des packages dans l'environnement.

Vous pouvez lister les environnements installés :
```
conda env list
```
2. Installation de PyTorch et torchvision:

-  __Mac__ or __Windows__: 
```
conda install pytorch==1.6.0 torchvision==0.7.0 -c pytorch
```
- __Linux__ : 
```
conda install pytorch==1.6.0 -c pytorch
pip install torchvision
```

3. Installer le package permettant d'utiliser les commandes Linux dans Anaconda Prompt:
```
conda install m2-base
```

4. Git

Dans la suite il est supposé que `git` est installé sur votre machine. Si ce n'est pas le cas, vous pouvez utiliser `conda`pour l'installer:
```
conda install git
```

5. Cloner le dépôt créé *via* githubclassroom (partie 1) et aller dans le dossier du dépôt:
```
git clone https://github.com/tpsma-nn-pytorch-nom1-nom2.git
cd tpsma-nn-pytorch-nom1-nom2
```


6. Installation des packages spécifiés dans le fichier *requirements.txt*.
```
pip install -r requirements.txt
```
Vous pouvez lister les packages installés dans l'environnement actif :
```
conda list
```
et installer d'autres packages dans votre environnement local si besoin.





## 3. TP

N'oubliez pas d'activer votre environnement avant le lancement de votre TP !

```
conda activate nnPyTorch
```

Vous pouvez maintenant lancer le notebook ([Jupyter notebook](https://jupyter.org)) du TP1 et les notebooks associés au CM en lancant la commande suivante :

```
cd tpsma-nn-pytorch-nom1-nom2
jupyter notebook
```
et compléter le TP1 `TP1-Tuto.ipynb`.

Un tutoriel sur les [Jupyter notebook](https://python.sdv.univ-paris-diderot.fr/18_jupyter/)
