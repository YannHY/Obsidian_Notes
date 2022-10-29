---
tags: [Blog]
---

🔗 [Lien](https://www.ralentirtravaux.com/le_blog/comment-importer-une-video-youtube-dailymotion-etc-dans-ibooks-author/)

En principe, lorsque vous souhaitez intégrer une vidéo dans votre site ou votre blog, vous copiez et collez une portion de code, et le tour est joué. Ce sont quelques lignes qui ressemblent à ça :

```
<iframe width="480" height="360" src="[https://www.youtube.com/embed/z4CLpA3Y1Kg?rel=0](https://www.youtube.com/embed/z4CLpA3Y1Kg?rel=0)" frameborder="0" allowfullscreen></iframe>
````

Il n’en va pas de même avec [iBooks Author](http://www.apple.com/fr/ibooks-author/ "iBooks Author"). Vous ne pouvez pas simplement copier et coller le code qui vous a été donné. Il faut réaliser un widget.  
Souvenez-vous, je vous avais expliqué [comment importer des exercices interactifs](http://www.ralentirtravaux.com/le_blog/?p=1930 "Comment importer des exercices interactifs ?") que vous aviez obtenus avec un exerciseur du type HotPotatoes. La méthode est sensiblement la même. Vous pourrez alors intégrer dans iBooks Author n’importe quelle vidéo, que celle-ci provienne de [YouTube](http://www.youtube.com/ "YouTube"), [DailyMotion](http://www.dailymotion.com/fr "DailyMotion"), [Vimeo](http://vimeo.com/ "Vimeo") ou l’[Ina](http://www.ina.fr/ "Ina.fr")… Évidemment, on se dira qu’on aura plus vite de recourir aux services d’un site comme [Bookry](http://bookry.com/author/widget/library/?from=classwidgets "Bookry"), mais il faut s’inscrire et la création du widget qui nous intéresse ne concerne que les seuls YouTube et Vimeo.

## Pour commencer

Tout d’abord, créez un dossier. Vous pouvez, par exemple, lui donner le nom de votre vidéo. Dans notre cas, ce sera verbe. On obtient donc un dossier intitulé verbe.

## Créer un fichier HTML

Dans ce dossier, placez un fichier HTML. Celui-ci doit impérativement s’appeler Main et porter l’extension .html. Votre fichier sera donc Main.html.  

Dans ce fichier, placez le code suivant :

```
<!DOCTYPE html>
<html>
<head>
<title></title>
</head>
<body>
</body>
</html>
```

Entre les balises title, mettez le titre de votre vidéo. Entre les balises body, placez le code obtenu sur le site de partage de vidéo. Dans notre cas, cela donnera ceci :

```
<!DOCTYPE html>

<head>
<title>Le verbe</title>
</head>
<body>
<iframe width="480" height="360" src="[http://www.youtube.com/embed/z4CLpA3Y1Kg?rel=0](http://www.youtube.com/embed/z4CLpA3Y1Kg?rel=0)" frameborder="0" allowfullscreen></iframe>
</body>
</html>
```

 ## Créer une image

À présent, créez une image de la dimension que vous voulez. Cette image va permettre d’afficher votre vidéo dans votre livre fait avec iBooks Author. Ce peut être un simple rectangle affichant le titre de votre vidéo. Vous préférerez probablement mettre une image provenant du film. Pour cela, affichez votre vidéo en plein écran et faites une capture d’écran.

Placez votre image dans le dossier verbe créé au tout début de ce tutoriel. Attention votre image doit s’appeler Default et être au format PNG. Votre image s’appellera donc Default.png.

## Créer un fichier PLIST

Dernière étape avant import dans iBooks Author, créez un fichier PLIST. Copiez ce code :

```
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "[http://www.apple.com/DTDs/PropertyList-1.0.dtd](http://www.apple.com/DTDs/PropertyList-1.0.dtd)">

<plist version="1.0">
<dict>
<key>CFBundleDevelopmentRegion</key>
<string>French</string>
<key>CFBundleDisplayName</key>
<string>Le verbe</string>
<key>CFBundleIdentifier</key>
<string>com.widget.Untitled</string>
<key>CFBundleName</key>
<string>Le verbe</string>
<key>CFBundleShortVersionString</key>
<string>1.0</string>
<key>CFBundleVersion</key>
<string>1.0</string>
<key>Height</key>
<integer>360</integer>
<key>MainHTML</key>
<string>main.html</string>
<key>Width</key>
<integer>480</integer>
</dict>
</plist>  
```

Ce code doit figurer dans un fichier intitulé Info et portant l’extension PLIST. Votre fichier sera donc Info.plist.

L’essentiel à retenir de ce fichier XML est qu’il délivre un certain nombre d’informations à propos de votre vidéo. Les plus importantes étant les dimensions de cette vidéo. Soyez sûr que ces dimensions correspondent à celles qui se trouvent dans votre fichier PLIST. Ma vidéo est de 480 par 360. Ce sont des dimensions qui m’ont été données par YouTube (naturellement, j’aurais pu en obtenir d’autres). Elles doivent donc figurer dans le fichier PLIST.

## Pour finir

Maintenant que vous avez les 3 fichiers Main.html, Default.png et Info.plist dans votre dossier verbe, il vous reste une chose à faire. Il faut ajouter l’extension WDGT à votre dossier qui sera désormais un widget intitulé verbe.wdgt. Il n’y a plus rien à faire si ce n’est glisser et déposer le widget dans iBooks Author. Branchez votre iPad. Cliquez sur Aperçu et vérifiez que votre vidéo fonctionne.

Si quelque chose ne fonctionne pas, si vous désirez modifier votre widget, il faudra faire un clic droit et choisir Afficher le contenu du paquet.