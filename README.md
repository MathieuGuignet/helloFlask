# helloFlask

Le but final de ce cas d’étude est de mettre en place les bonnes pratiques de développeurs en
travaillant sur un mini projet “end-to-end” versionable, reproductible et donc plus facile à
maintenir dans le temps.

En tant que data scientist, il est intéressant d’avoir une idée de l’écosystème technique dans lequel
vous allez évoluer. 

Objectifs pédagogiques : 

- Travailler sur un projet collaboratif en utilisant les outils de versionnage Git
- Savoir créer un projet Python reproductible et maintenable dans le temps
- Connaître les bases de Docker pour pouvoir l’utiliser dans votre activité de Data Scientist
- S’organiser en groupe dans une démarche Agile

Installation et utilisation de Pyenv :

1) Installation des dépendances : 

sudo apt-get update; sudo apt-get install make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev

2) Installer Pyenv : 

curl https://pyenv.run | bash

3 ) Rajouter dans le fichier .bashrc les lignes suivantes : 

Load pyenv automatically
export PYENV_ROOT="$HOME/.pyenv"
command -v pyenv >/dev/null || export
PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"
Load pyenv-virtualenv automatically
eval "$(pyenv virtualenv-init -)"

4) Commenter le bloc conda initialize pour éviter tout conflit avec Pyenv

5) Création d'un environnement conda avec miniconda :

pyenv install --list
pyenv install miniconda3-4.7.12
pyenv versions

6) Activation de l'environnement conda :

pyenv activate miniconda3-4.7.12

7) Installation d'une version de Python :

pyenv install 3.10.4

pyenv virtualenv 3.10.4 testEnv310

8) Lister les différents environnements dispo : 

pyenv virtualenvs

9) Activé l'environnement virtuel

pyenv activate testEnv310

10) Définir la version comme interpréteur global:

pyenv global 3.10.4
python --version

11) Définir la version comme interpréteur local :

pyenv local
python --version
