# Simple Obsidian MkDocs

Un simple modèle de dépôt GitHub pour publier des notes d'Obsidian via MkDocs avec le thème Material telles que à cette adresse : <https://ericecmorlaix.github.io/simple_template_obsidian_mkdocs/>

Ce template est basé sur <https://github.com/jobindjohn/obsidian-publish-mkdocs> et s'inspire également de <https://github.com/ObsidianPublisher/obsidian-mkdocs-publisher-template>

## Mise en place

1. **Créer** un nouveau dépôt GitHub à partir de ce modèle en cliquant sur le bouton vert ci-dessus ou cliquer sur [ce lien](https://github.com/ericECmorlaix/simple_template_obsidian_mkdocs/generate) ;
![[Use_this_template.png]]
2. **Donner** un nom à votre dépôt public et **ajouter** une description. Par défaut vos notes seront publiées à l'adresse <https://votre-pseudo-github.github.io/nom-depot/> ;
 > ne copier que la branche `main` du dépôt template ;
3. **Cloner** le dépôt que vous venez de générer dans votre dossier/coffre d'Obsidian.  Soit avec le plugin Obsidian Git installé et activé dans votre coffre, ou directement en ligne de commande : 
```sh
cd votre_dossier-coffre
git clone url_du_depot`
```
4. **Glisser/déposer** les notes que vous souhaitez publier et leurs pièces jointes dans le dossier `docs` ;
5. **Commiter** puis **pousser** les changements avec Obsidian Git après avoir bien paramétré les options de ce plugin ;
6. GitHub Action va alors prendre en charge automatiquement la conversion de vos fichiers MarkDown d'Obsidian vers [MkDocs](https://www.mkdocs.org/) avec le thème [Material](https://squidfunk.github.io/mkdocs-material/) pour générer les fichiers au format HTML de votre site Web dans une branche `gh-page` ;
7. Depuis la page de votre dépôt sur GitHub, **Cliquer** sur les onglets `Settings` (1) puis `Pages` (2), **sélectionner** la branche `gh-pages` (3) enfin **cliquer** sur le bouton `Save` (4) :
![](gh-pages.png)
> Au bout d'un moment, si tout se passe bien, votre site devrait être visible sur le web à l'adresse <https://votre-pseudo-github.github.io/nom-depot/>

8. Si cela ne fonctionne vraiment pas pour vous, ouvrez une [issue](https://github.com/ericECmorlaix/simple_template_obsidian_mkdocs/issues/new/choose) et expliquez moi votre problème...

## Configuration du site

Les fichiers de configuration du site `mkdocs.yml` et `ci.yml` sont écrits en [YAML](https://fr.wikipedia.org/wiki/YAML), un langage avec une syntaxe la plus lisible possible par des humains pour représenter des données.

Obsidian ne permet pas d'éditer ces fichiers. Il vous faudra les ouvrir dans votre éditeur de texte favori ou directement les éditer dans GitHub pour les modifier afin de les personnaliser :

- Sauf à vouloir ajouter de nouvelles fonctionnalités, le fichier [`CI.yml`](https://ericecmorlaix.github.io/adn-Tutoriel_site_web/Yaml/#le-fichier-ciyml) peut rester inchangé ;
- En revanche, il est nécessaire de modifier le fichier `mkdocs.yml` en s'aidant des explications laissées en commentaires ou encore de celles ce [tutoriel de configuration d'un site web avec MkDocs](https://ericecmorlaix.github.io/adn-Tutoriel_site_web/Yaml/#le-fichier-mkdocsyml)


## Autres projets à regarder

- <https://github.com/ObsidianPublisher/obsidian-mkdocs-publisher-template>
- <https://github.com/mr-karan/notes>
- <https://github.com/Jackiexiao/foam-mkdocs-template>
- <https://github.com/foambubble/foam-template>
- <https://sarthaknarayan.tech/projects/obsidian-publish-github-action/>
- <https://github.com/mathieudutour/gatsby-digital-garden>
- <https://github.com/TuanManhCao/digital-garden>
- <https://forum.obsidian.md/t/my-obsidian-mkdocs-workflow/24424> | <https://tarekshehata.github.io/alkashi/>
 
