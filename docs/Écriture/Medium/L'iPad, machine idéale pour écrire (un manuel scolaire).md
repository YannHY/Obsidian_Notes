---
tags: Medium
authors: Houry
date: 20-09-2016
---

[Lien](https://medium.com/@yannhoury/lipad-machine-idéale-pour-écrire-un-manuel-scolaire-c9097e7a9b4c)

![[iPad.jpeg]]

## Splendeurs et misères d'iBooks Author
À l'époque où [iBooks Author](http://www.apple.com/fr/ibooks-author/ "iBooks Author") était un logiciel plein de promesses, je me prenais à rêver d'une version pour iPad qui n'est jamais venue. D'ailleurs, plus rien n'est jamais venu de ce logiciel dont Apple continue pourtant à faire la promotion, certainement dans le but de rentabiliser un produit possédant déjà un octet dans la tombe.

Par ailleurs, si [iBooks Author](http://www.apple.com/fr/ibooks-author/ "iBooks Author") permettait de faire de beaux manuels richement interactifs, ceux-ci ne pouvaient être lus que sur les machines arborant une pomme croquée. Or mes élèves venaient soit avec leur propre matériel (les joies du BYOD), soit avec l'ordinateur prêté par le Conseil général. Dans ces conditions, produire un manuel spécifiquement voué à être lu sur une machine pommée n'avait aucun sens dans un monde où PC et machines tournant sous Android étaient monnaie courante.

## À la recherche d'un remplaçant
Il a alors fallu trouver d'autres moyens de production d'un manuel scolaire. Je dis d'autres parce que j'en essayé une tripotée. Avant même de le faire, j'ai porté mes manuels [sur mon site](http://www.ralentirtravaux.com/ "Ralentir travaux"). Celui-ci étant responsive design et en HTML5, je me disais avoir là un moyen de toucher le plus grand nombre d'élèves. C'était oublier qu'une connexion internet peut être parfois aléatoire. Mais si, dans l'ensemble le réseau (du collège) tient la charge et ne connaît pas trop de mésaventures, j'achoppai sur un autre problème.

![[Coda.jpeg]]

Avec le temps, je délaissai mon iMac et ses 27 pouces au profit de mon iPad. La raison est relativement évidente. J'ai mon iPad à peu près tout le temps sur moi, mais pas mon 🖥. Je l'ai en cours, je l'ai quand je pars en déplacement, je l'ai quand je suis en vacances et je peux donc à tout moment travailler à l'élaboration de projets passablement longs. Mais, je trouvais que maintenir un site web sur un iPad laissait à désirer. Je n'ai peut-être pas su m'y prendre correctement, mais, même en faisant l'acquisition d'une si belle app comme [Coda](https://panic.com/coda/ "Coda"), je ne m'y retrouvais pas. Mais j'y travaille toujours... 😇

Et puis dans le même temps, j'ai découvert qu'il existait autre chose que des pommes et je suis allé voir du côté de Google Play, de Kobo et surtout d'Amazon qui a purement et simplement changé ma façon de voir les choses.[ Ça a changé ma façon de lire](https://medium.com/@yannhoury/pourquoi-lire-avec-amazon-a6aff94d25e1?source=linkShare-5c07e4d0064b-1474284452 "Pourquoi lire avec Amazon"), ça a changé ma conception du livre, ça a changé mon mode de production du livre. D'ailleurs, de mon point de vue d'enseignant, je trouve (si ça a du sens d'écrire les choses ainsi) que le livre l'a emporté sur le web ou, pour le dire un peu plus sérieusement, l'ePub l'a emporté sur la page web. 

![[Dictionnaire.jpeg]]

Bref, je me devais d'écrire des livres qui seraient lisibles sur toutes les plateformes. De plus, la liseuse étant devenue pour moi l'accès royal au texte, j'ai progressivement abandonné la débauche d'artifices interactifs promue par Apple. Et, compte tenu du développement du multitâche sur les appareils mobiles, j'en suis venu à penser qu'une tablette proposait suffisamment de ressources qui pouvaient être exploitées sans être directement intégrées dans le livre, lequel est déjà bien assez lourd comme ça avec des images qu'il faut quand même pouvoir afficher sur toutes sortes d'écrans, y compris des écrans de haute définition. Ainsi, sur l'iPad, avec [Split View](https://support.apple.com/fr-fr/HT202070 "Split View"), on peut très bien lire le texte d'un côté et, par exemple, visionner une vidéo en regard.

![[Video-Manuel.jpeg]]

J'ai donc tout d'abord longuement travaillé avec [Pages](http://www.apple.com/fr/pages/ "Pages") qui, pour peu que l'on comprenne la notion de styles, permet de produire un ePub relativement facilement. L'ensemble aboutissant à un ePub 3, on peut insérer des vidéos ou des fichiers audio, ce qui est plutôt séduisant, mais lourd. Excessivement lourd. Ajoutez 10 vidéos et votre livre pèse un poids qui frappera de terreur tous les iPad 16 Go qu'Apple a eu la bonne idée de continuer à vendre tout en proposant une app qui permettait de faire des livres de 5 Go. 😱

![[ManuelPages.jpeg]]

Et puis il faut admettre qu'un ePub fait avec Pages contient quelques attributs CSS qui n'ont été écrits que pour être lus sur l'une ou l'autre des machines conçues par Apple. Donc pas terrible. J'ai fait quelques essais avec Libre Office et les plugins idoines ([eLAIX](http://extensions.libreoffice.org/extension-center/elaix "eLAIX") ou [Writer2ePub](http://writer2epub.it/en/download/ "Writer2ePub")). C'est bien, mais inaccessible de mon iPad. J'ai alors fait des essais avec [BookCreator](https://appsto.re/fr/wDIxA.i "BookCreator"), qui est très bien pour les élèves, beaucoup moins pour le prof. Des essais avec l'horrible [Creative Book Builder](https://appsto.re/fr/uIL4A.i "Creative Book Builder") qui pourrait être excellent si son auteur découvrait le mot « ergonomie ». Bref, on peut faire des choses sympathiques pour peu que vous n'ayez pas l'idée d'aller ouvrir votre livre ailleurs que dans [iBooks](http://www.apple.com/fr/ibooks/ "iBooks").

![[BookCreator.jpeg]]

## Le Markdown, graal des enseignants
Je m'étais accommodé de Pages quand [j'ai commencé à découvrir le Markdown](http://www.ralentirtravaux.com/le_blog/?p=2939 "Et si les enseignants utilisaient le Markdown"). Ça a été une révolution (pour moi), une révolution bien tardive mais une révolution quand même. C'était l'ultime solution (jusqu'à ce que je trouve autre chose...). C'était un retour au code, si par code on veut bien entendre langage de balisage plutôt léger. J'en avais ma claque du HTML, du CSS, et de mon site à maintenir. Désespéré, j'envisageais tout de même de faire mon ePub à la main, de me retrousser les manches et de lancer [Sigil](https://sigil-ebook.com/ "Sigil") et de tout faire par moi-même. Mais quelle corvée quand on y pense ! Je ne suis que prof de français. Pas développeur. Et puis j'ai pris conscience de l'existence du Markdown. Facile à apprendre, facile à mettre en œuvre. La solution était là.

Restait à trouver l'app. THE app. 🏆J'ai d'abord utilisé [1Writer](https://appsto.re/fr/GjYJO.i "1Writer") que j'aime toujours beaucoup. Et puis j'ai découvert, ou plutôt on m'a fait découvrir [Ulysses](%20%20https://www.ulyssesapp.com/features/ "Ulysses"). Cette application mériterait à elle seule tout un article. Mais je dirai simplement que pouvoir écrire un texte formaté en Markdown et pouvoir en deux clics produire un document docx ou PDF ou HTML ou ePub, sans avoir à retravailler le même texte et donc en une seul fois, a achevé de me conquérir. On peut même dans la foulée publier sur son Wordpress et Medium. Le bonheur intégral.

Pour bien le comprendre, imaginez qu'auparavant j'écrivais sur un traitement de texte pour imprimer le document à transmettre aux élèves ; je transférais le tout dans mon application pour faire un iBooks ; je publiais un extrait sur mon Wordpress après m'être rendu sur Wordpress puis éventuellement j'allais sur Medium pour copier coller ce même extrait et à chaque fois il fallait rajouter les images, remettre en gras, remettre en italique, refaire les liens, etc. Maintenant avec Ulysses, je le fais une fois et c'est publié partout. Et tout ça à partir de mon iPad. 😍

![[iPadMachineAEcrire.jpeg]]

Si l'un d'entre vous est arrivé à la fin de ce billet, il se demandera comment je retouche les images qui parsèment mes manuels. Eh bien pour cela, comme sur le Mac, un simple navigateur suffit. Et si j'ai des choses un peu plus complexes à faire, j'ai recours à [Pixelmator](https://appsto.re/fr/lUBh3.i "Pixelmator"). Pas plus tard qu'hier, je me suis livré à un détourage effréné avec autant de facilité que son mon Mac et sa souris. Mais avec le Pencil. 🤗

![[Detourage.jpeg]]

Bref l'iPad, c'est la machine à écrire du XXIe siècle. Je lui ai quand même ajouté un clavier. J'ai choisi le [Keys-to-go de Logitech](http://www.logitech.fr/fr-fr/product/keys-to-go "Keys-to-go de Logitech"). Depuis que [iOS 9 a intégré les raccourcis avec claviers externes](http://www.igen.fr/ios/2016/02/ios-93-ameliore-spotlight-avec-les-claviers-externes-94657 "Raccourcis claviers") dignes d'un ordinateur de bureau, on gagne en productivité. Je retrouve les joies du `⌘ + ⇧` ou du `⌘ +  →`, pour ne prendre que quelques exemples, bref de [beaucoup de ces raccourcis](https://support.apple.com/fr-fr/HT201236 "Beaucoup de ces raccourcis") qui me permettent de garder les mains sur le clavier et d'éviter de les lever et de toucher l'écran. Et quand il faut vraiment le faire, on peut éviter un peu de fatigue musculaire à saisir le Pencil et à l'utiliser pour naviguer dans l'iPad.

![[RaccourcisClavier.jpeg]]

Ainsi, dans quelques mois, vous pourrez lire le premier manuel scolaire fait entièrement sur un iPad et en Markdown. 🍸🍾

![[CouvertureProvisoire.jpeg]]