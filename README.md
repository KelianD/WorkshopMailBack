# Projet Workshop Mail

## Git pour les nuls
Pour utiliser Git, vous allez avoir besoin de **GitBash** sur vos pc afin de faire les commandes (vous pouvez également utiliser des terminals sur VScode ou sur vos suite Jetbrains surcôté.

Règle n°1: **ne codez jamais quelque chose si vous êtes dans la master, verifiez toujours ça coute rien**

### Les commandes de base

Pour récupérer le projet depuis GitHub, copier de préférence en SSH le projet.
Allez dans le repertoire de vôtre choix faites un *clique droit* selectionnez **GitBash Here** et entrez la commande suivante:
```
git clone cheminDuProjetSSH
```

Lorsque vous créez une branche, faites attention: à avoir fait un:
```
git pull
```
afin de récuperer les dernières modifications,

et à bien vous trouver dans la branche dev lorsque vous faites votre commande afin de ne pas tirer de branche depuis la master, **par pitié**.

**Pour créer une nouvelle branche et vous déplacer dedans**:
```
git checkout -b feature_maBranche
```

**Pour verifier l'etat de vos modifications**:
```
git status
```

**Pour ajouter les modifications et les préparer au push**:
```
git add .
```

**Pour faire un commit et préciser son contenu**:
```
git commit -m "FEAT: ma fonctionnalité"
```

**Pour push vos modifications sur GitHub**:
```
git push
```

Si votre branche n'a jamais été push auparavant GitBah vous dicteras la commande à copier coller quand vous aurez fait vôtre git push.

### Norme de nommage branche et commit
Les branches doivent toujours suivre ce schèma afin de faciliter la compréhension des branches:
```
feature_MaFonctionnaliteTropCool
```

Pour les commit, ils doivent expliquer simplement ce que vous pushez. 
Exemple, je souhaite ajouter une fonctionnalité qui permet de naviguer entre les pages du front:
je vais donc être dans ma branhce **feature_navigation** et mon commit sera:
```
git commit -m "FEAT: Ajout de la navigation entre les pages Front"
```
Le commit indique dans un premier temps le types de commit (fonctionnalités, correction, modification de la structure du code, etc...)

Voici les principaux types de commit (à écrire en majuscule):
```
FEAT : ajout d’une nouvelle fonctionnalité
FIX : correction d’un bug
HOTFIX: correction d'un bug sur la master ou la dev
PERF : amélioration des performances
REFACTOR : modification qui n’apporte ni nouvelle fonctionalité ni d’amélioration de performances
STYLE : changement qui n’apporte aucune alteration fonctionnelle ou sémantique (indentation, mise en forme, ajout d’espace, renommante d’une variable…)
DOCS : rédaction ou mise à jour de documentation
TEST : ajout ou modification de tests
```
