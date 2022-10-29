---
tags: [Documentation, Markdown]
author: [Stéphane Bortzmeyer]
date: 23.03.2016
---

RFC 7764: Guidance on Markdown: Design Philosophies, Stability Strategies, and Select Registrations

[Lien](https://www.bortzmeyer.org/7764.html)

[Lire RFC 7764](https://www.rfc-editor.org/info/rfc7764)

## Texte brut, formats binaires et markdown
> Lorsqu'on veut stocker des textes (romans, rapports techniques, articles scientifiques, lettres d'amour, etc) sur un système informatique, on a plusieurs solutions : elles vont du **[texte brut](https://fr.wikipedia.org/wiki/texte%20brut)** à un format binaire. Le texte brut est le stockage des seuls caractères **[Unicode](https://fr.wikipedia.org/wiki/Unicode)** (cf. [RFC 6838](http://www.bortzmeyer.org/6838.html), section 4.2.1 : le texte est distribué sur l'Internet avec un type MIME`text/quelquechose`, par exemple `text/plain` pour le texte brut). Son gros avantage est qu'il est lisible et modifiable avec n'importe quel logiciel. Bon, en fait, le texte brut n'est jamais tout à fait brut. Il contient quelques caractères de contrôle comme le **[saut de ligne](https://fr.wikipedia.org/wiki/saut%20de%20ligne)** ou la **[marque d'un nouveau paragraphe](https://fr.wikipedia.org/wiki/marque%20d'un%0A%20%20%20%20nouveau%20paragraphe)**(U+2029 en **[Unicode](https://fr.wikipedia.org/wiki/Unicode)**, mais ce séparateur de paragraphe n'est que rarement géré par les logiciels).
> À l'autre extrémité se trouve les formats binaires : lisibles et modifiables uniquement par des applications spécifiques (et c'est pour cela qu'ils sont distribués avec le type MIME `application/quelquechose`).
> Entre les deux se trouvent le texte formaté ou marqué. Il s'agit à première vue de texte brut mais il inclut en fait quelques marques qui ont une signification non prévue par le jeu de caractères. Un exemple classique est la mise en évidence qui, en Markdown, se fait en encadrant le texte avec des **[étoiles](https://fr.wikipedia.org/wiki/Ast%C3%A9risque)** : « il est *très* important de comprendre que... »

## Type MIME
> Depuis le [RFC 7763](http://www.bortzmeyer.org/7763.html), il existe un **[type MIME](https://fr.wikipedia.org/wiki/type%20MIME)** [^1] pour identifier Markdown,`text/markdown`. (Une extension de nom de fichier comme `.md` ne suffit pas : tout le contenu n'est pas forcément dans des fichiers.)

La suite porte sur le problème de préservation du type MIME ("Markdown n'a pas l'équivalent du `<?xml version="1.0">` qui, au début des contenus en **[XML](https://fr.wikipedia.org/wiki/Extensible%20Markup%20Language)**, indique sans ambiguité qu'il s'agit de XML") ainsi que sur le stockage des métadonnées.

[^1]: Un type de médias (media type en anglais)1, à l'origine (et toujours communément) appelé type MIME, est un identifiant de format de données sur internet en deux parties.