---
tags: [Blog]
---

🔗 [Lien](https://www.ralentirtravaux.com/le_blog/comment-integrer-des-exercices-du-type-hotpotatoes-dans-ibooks-author/)

Je crois bien que c’est la première fois que je réalise un tutoriel. Il y a un début à tout.
En fait, comme j’ai reçu plusieurs messages me demandant comment j’avais réalisé tel ou tel exercice pour mon manuel, je me suis dit que j’allais expliquer les choses une bonne fois pour toutes. Et je n’aurai, ensuite, plus qu’à indiquer le lien à chaque fois qu’on me posera la question. Le droit à la fainéantise mérite bien quelques efforts.

Avant de vous expliquer comment je m’y suis pris pour intégrer certains exercices réalisés avec HotPotatoes dans iBooks Author, je tiens à prendre quelques précautions d’usage. Je n’ai rien d’un spécialiste. Je bidouille, et, à force, le HTML ou le CSS me deviennent plus ou moins familiers. Quant au JavaScript, je suis une véritable quiche dont la nullité crasse ne peut qu’inviter à l’humilité. Bref, si je dis une bêtise, je vous prierai de ne pas m’en vouloir. Les intentions sont nobles, l’exactitude des renseignements subséquents non garantie.

Commençons.

![[Tutot1.mov]]

Si vous n’aimez pas les vidéos, lisez la suite. De toute façon, c’est complémentaire.

## I - Utiliser le widget HTML
![[Widget HTML.png]]

Si, dans un élan d’enthousiasme naïf, vous choisissez de créer un widget HTML, et que vous cherchez à y entrer benoîtement un peu de HTML, vous constaterez que rien ne se passe. Vous ne pouvez rien faire. Vous aurez beau cliquer sur le rectangle indiquant HTML, ce sera en vain. Stupéfait, vous découvrez ensuite que l’inspecteur vous propose de choisir un widget HTML 5. Et, en effet, vous avez la possibilité d’importer quelque chose portant l’extension .wdgt.

J’abandonne dorénavant le ton un tantinet verbeux que j’ai employé jusqu’à présent, je vous épargne la description de l’étonnement, l’agacement et le dépit que j’ai éprouvés. Je vous passe les phases d’énervement et d’abandon, et j’en viens aux résultats auxquels je suis parvenu.

## II - Créer un widget

Vous l’aurez compris. Il s’agit de créer un widget, par vous-même. Ne croyez pas ceux qui vous disent qu’il faut télécharger xCode et tout le tintouin. C’est peut-être gratuit, mais c’est très lourd et parfaitement inutile pour ce que nous allons faire.

En fait, tout ce que vous devez faire consiste à créer un dossier le plus simplement du monde. Vous créez votre dossier, vous lui donnez l’extension .wdgt, et votre dossier change d’apparence. Il devient un widget ! Un widget parfaitement vide, mais un widget.

![[wdgt.png]]

Vous faites alors un clic droit sur ledit widget et vous choisissez Afficher le contenu du paquet. Évidemment, il n’y a rien dedans. Vous allez devoir le « remplir ».

![[afficher.png]]


## III - Remplir votre widget

Que mettre dedans ? Eh bien l’exercice que vous avez réalisé avec HotPotatoes (pour ça, je ne vous explique pas comment faire ; il y a d’ailleurs une kyrielle de tutoriels sur le sujet).
Vous allez donc mettre dans votre widget, le fichier que vous avez créé avec HotPotatoes. Quel que soit le nom que vous lui avez donné au moment de sa création, vous allez devoir le renommer. Il doit impérativement porter le nom suivant : index.html. Attention, HotPotatoes crée des fichiers portant l’extension .htm, vous devrez la changer pour .html.
Ensuite, vous devez créer un fichier .plist répondant au doux nom de Info.plist dans lequel vous devez écrire les lignes ci-dessous :

```
<plist version="1.0">
<dict>
	<key>CFBundleDevelopmentRegion</key>
	<string>French</string>
	<key>CFBundleDisplayName</key>
	<string>Exercice</string>
	<key>CFBundleIdentifier</key>
	<string>com.exercice</string>
	<key>CFBundleName</key>
	<string>Exercice</string>  
	<key>CFBundleShortVersionString</key>
	<string>1.0</string>
	<key>CFBundleVersion</key>
	<string>1.0</string>
	<key>Height</key>
	<integer>768</integer>
	<key>MainHTML</key>
	<string>index.html</string>
	<key>Width</key>
	<integer>1024</integer>
</dict>
</plist>
```

Évidemment, vous voudrez peut-être modifier certaines informations, non pas ce qui est compris entre <key> et </key>, mais ce qui est entre <string> et </string> ou <integer> et </integer>. Mais, quels que soient les choix que vous ferez, il n’y a pas là de grandes difficultés.

Vous devez enfin créer une image devant être intitulé Default. Elle aura l’extension .png. Cette image est celle qui servira à iBooks Author pour afficher votre exercice. Pour ma part, j’ai cédé à la facilité et j’ai créé une image avec Pixelmator sur laquelle j’ai écrit... Exercice (ce n’est pas très original, je sais).

![[Exercice.png]]

Est-ce tout ?

Bah ! non.

## IV - Modifier le code de index.html

Une des caractéristiques de HotPotatoes est de produire des choses assez moches. Quand je réalise un exercice avec ce logiciel, je change une partie du CSS afin que ce soit le plus neutre possible. N’étant pas un maître de la feuille de style, j’essaie au moins d’aspirer à la sobriété. Je me dis que ça passera mieux.

Que faut-il faire ?

Pas grand-chose. Il faut ouvrir votre fichier index.html dans un éditeur de code. J’utilise Coda, mais il en existe de nombreux notamment TextWrangler qui est gratuit. Un véritable codeur se livrerait à un nettoyage en bonne et due forme du code, mais n’étant pas un, je me contente de modifier ce qui m’importe (cela dit, la tentation est grande...).

Pour être clair et précis, vous devez modifier ce qui se trouve entre `<style type="text/css"></style>`.

![[Style.png]]

Je ne vais pas vous faire un cours sur le CSS, mais sachez quelques petites choses.

Vous devez retirer ces lignes :

```
margin-right: 5%;
margin-left: 5%;
````

J’ai choisi aussi de retirer les bordure (mais ça, c’est un choix):

```
border-style: solid;
border-width: 1px 1px 1px 1px;
border-color: #000000;
````

J’ai changé cette ligne :

```
padding: 0.5em;
````

Par celles-ci :

```
padding-right: 6em;
padding-left: 6em;
padding-bottom: 2em;
````

Et retirer celle-là :

```
margin-bottom: 1px;
````

Vous pouvez modifier de nombreuses choses encore, des choses très simples comme changer la police à cette ligne :

```
font-family: Georgia,Baskerville,Times New Roman,Geneva,Arial,sans-serif;
````

La couleur de la police :

```
color: #000000;
````

Plus important, la dimension du corps de la page (important, parce qu’il faut que ça tienne sur l’iPad) :

```
width: 90%;
````

Personnellement, je varie la largeur (width) en fonction de l’exercice produit pour que cela tienne sur l’écran de l’iPad sans qu’il y ait à scroller (car s’il faut faire défiler la page, monter ou descendre, pour une raison ou pour une autre, ça ne marche pas).

## V - Pour finir

Pour finir, précisons que tout ne fonctionne pas. Ainsi, tel exercice réalisé (http://www.ralentirtravaux.com/lettres/exercices/sixieme/phrase/phrase-1.htm) avec HotPotatoes ne fonctionne pas. À vrai dire, cet exercice ne fonctionne ni dans iBooks Author ni dans Safari. C’est un exercice où l’on peut déplacer des portions de texte. C’est bien dommage, et si un développeur passant par là pouvait m’apporter quelques éléments de réponse, j’en serai vraiment très heureux.

En revanche, je viens d’essayer, les mots croisés fonctionnent dans iBooks Author.

Vous rencontrerez probablement un tas de petites difficultés dépendant de ce que vous cherchez à obtenir, sachez que si je peux vous aider d’une manière ou d’une autre, je n’hésiterai pas.

Dernier point. On peut très bien réaliser la même chose avec Netquiz Pro. Simplement, l’exerciseur génère de nombreux fichiers qu’il faut tous mettre dans le même dossier comportant l’extension .wdgt. Vous n’aurez pas à renommer le principal fichier puisqu’il est déjà nommé index.html. Et le CSS, si vous désirez le modifier, se trouve (comme il se doit) dans un dossier à part.
