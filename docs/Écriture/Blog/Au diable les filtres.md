---
tags: [Blog]
---

Qui n’a jamais pesté contre un web filtré ? À en juger d’après les nombreuses réactions ou demandes de collègues, on peut penser qu’ils sont nombreux ceux à qui l’on dénie et le plein accès au web, et la capacité à décider par eux-mêmes ce qu’ils peuvent faire et ce qu’ils ne peuvent pas faire. Et de râler sans savoir quoi faire...

En ce qui me concerne, je ne comprends pas un traitre mot au discours qui m’est tenu à propos du filtrage du net : il s’agirait d’empêcher les élèves (et les enseignants) d’accéder à des sites qui n’auraient aucun intérêt pédagogique.

Ah !?

Parce qu’il y a quelqu’un, quelque part, sachant ce qui revêt un intérêt pédagogique ou pas ? Parce que moi je l’ignore (je ne parle évidemment pas de tout ce que la morale réprouve).

Peut-on même savoir quel chemin l’activité pédagogique va-t-elle emprunter ? Moi, je fais feu de tout bois : Facebook, Twitter, YouTube, un obscur blog, un improbable site, tel ou tel forum nourrissent ma réflexion et stimulent mon désir d’enseigner. En revanche, quand je tombe sur une page m’expliquant que je n’ai pas le droit d’accéder à telle page parce que quelqu’un quelque part en a décidé ainsi, cela me fait sortir de mes gonds. Je me suis déjà vu refuser l’accès à un site sur la peinture parce qu’on avait pensé que ce n’était pas pédagogique. Eh quoi ! Raphaël ou Waterhouse ne seraient pas pédagogiques (si si, ça m’est arrivé) ?

Et puis s’il fallait prouver que les filtres étaient inadaptés à l’école, rappelons qu’en dépit de leur mise en place, on trouve durant sa navigation sur le web ce qu’il ne faudrait pas, et qu’on y trouve pas ce qu’il faudrait...

Bah oui.

Pour toutes ces raisons, pour mes collègues auxquels on ne permet pas d’accéder à leur boîte mail, aux sites auxquels ils veulent accéder et qui sont pourtant d’une innocuité pédagogique et morale, voici deux solutions, qu’il ne faut évidemment pas mettre en œuvre, parce que c’est mal, et que - si je vous le dis - c’est uniquement à titre informatif (je ne saurais être tenu pour responsable de vos agissements).

Tor

La première solution consiste à installer Tor sur votre ordinateur. C’est d’une simplicité enfantine, à condition d’avoir un plein accès à votre machine, et non à un espace alloué sur un serveur avec des droits limités.
Faut-il rappeler que Tor vous permettra d’être (relativement) anonyme durant votre navigation sur le web. Récemment, j’ai pu encore le vérifier en allant sur le site de la CNIL qui prétend pister vos traces (http://www.cnil.fr/vos-libertes/vos-traces/). Avec Tor, comme on peut le voir grâce à cette capture d’écran, la CNIL pense que mon adresse IP est ... alors que ma véritable adresse est ... (je ne vais quand même pas vous donner mon adresse) , et que je viens de ... !
Je ne sais pas si je deviens parano, mais j’aime de moins en moins laisser des traces de mon parcours sur internet, notamment depuis que j’ai lu ces quelques articles : http://www.numerama.com/magazine/19103-pour-la-cnil-facebook-et-google-sont-des-big-brother-conviviaux.html, http://www.numerama.com/magazine/19067-41-pays-approuvent-le-rapport-de-l-onu-sur-la-liberte-et-internet-pas-la-france.html, etc. D’ailleurs, Tor installe pour Firefox une série de plugins destinés aux plus paranos d’entre nous : NoScript, BetterPrivacy, HTTPS-Everywhere.

Évidemment, tout cela n’est pas nouveau. Cela fait bien longtemps que l’on nous invite à la prudence. Si vous n’êtes pas convaincus, lisez cet article expliquant pourquoi chiffrer ses mails : http://www.gbronner.net/mail/cryptoMail.html (notamment la partie «Bon, d’accord. Mais qui aurait intérêt à lire mes courriels ? Je n’ai rien à cacher»).

Mais je m’éloigne du sujet...

Pour en revenir à nos filtres, il y a un autre moyen de les contourner, un moyen qui me plait beaucoup, à la fois très simple, et compliqué.

Votre administrateur réseau a bloqué Facebook. Ainsi, vous ne pouvez saisir l’URL http://www.facebook.com sans essuyer un refus. Voici comment y parvenir (j’utilise un Mac mais on peut aisément faire la même chose avec un PC).

Ouvrez le Terminal et faites un ping afin d’obtenir l’adresse IP du site que vous voulez consulter.

![[Terminal.png]]

Vous devez ensuite convertir l’adresse IP en binaire, soit convertir les quatre numéros en numéro binaire à 8 chiffres. Enfin, il ne manque plus qu’à réunir tout cela en un nombre binaire à trente-deux chiffres, puis à le convertir en un nombre décimal.

![[IP.jpg]]
![[Binaire.jpg]]
![[Décimal.jpg]]

Si vous n’avez pas eu le temps de réviser ces petites pirouettes numériques, je vous recommande le logiciel IP-Calculator (que je viens de trouver sur l’App Store).

Vous n’avez pas de Mac, vous n’aimez pas le Terminal ? Voici mieux encore : un site qui vous demande juste de rentrer l’adresse IP (quoique je vois pas comment vous allez l’obtenir sans lui) et qui fait tout le calcul : http://www.allredroster.com/iptodec.htm