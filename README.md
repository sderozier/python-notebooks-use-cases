# Exemples d'utilisation de Python en bioinformatique

Vous pouvez manipuler les notebooks proposés en ligne avec Binder :

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/sderozier/python-notebooks-use-cases/master?urlpath=lab)

Le répertoire `notebooks`contient 3 *notebooks* [Jupyter](https://jupyter.org/) :

* `comptage_rnaseq.ipynb` : exploration de données de comptage RNA-Seq
* `arbre_phylogenetique.ipynb` : création d'un arbre phylogénétique
* `formats.ipynb` : formats de fichiers (FASTA, FastQ, GenBank, GFF)

## Manipuler les notebooks localement (sur votre machine)

1. Installez miniconda dans un environnement de type Unix (WSL pour Windows, Mac OSX ou Linux)

2. Clonez le dépôt :
    ```
    git clone https://github.com/sderozier/python-notebooks-use-cases.git
    ```

3. Déplacez-vous dans le répertoire du dépôt :
    ```
    cd python-notebooks-use-cases
    ```

4. Créez l'environnement conda :
    ```
    conda env create -f binder/environment.yml
    ```

5. Activez l'environnement conda :
    ```
    conda activate python-notebooks-use-cases
    ```

6. Chargez les extensions Jupyter Lab :
    ```
    bash binder/postBuild
    ```

7. Lancez Jupyter Lab :
    ```
    jupyter lab
    ```

Pour des utilisations ultérieures, seules les étapes 3, 5 et 7 seront nécessaires.

## Remarques pour les utilisateurs de Windows (sans WSL)

Si vous avez installé miniconda sur Windows (mais sans WSL), vous pouvez également installer cet environnement sur votre machine. 

Dans un premier temps, installez `git` si ce n'est pas déjà fait en exécutant cette commande dans un terminal :
```
conda install -c conda-forge git
```

Réalisez ensuite les étapes 2, 3, 4 et 5. 

Pour l'étape 6, exécutez, manuellement et l'une après l'autre, les commandes contenues dans le fichier `binder/postBuild` :
```
jupyter labextension install @jupyter-widgets/jupyterlab-manager
jupyter labextension install @jupyterlab/toc
```

Cette étape peut prendre du temps.

Terminez enfin par l'étape 7.

## Licence

Le contenu de ce dépôt est sous licence libre BSD 3-clause. Pour plus d'informations, consultez le fichier [LICENSE](LICENSE.txt).
