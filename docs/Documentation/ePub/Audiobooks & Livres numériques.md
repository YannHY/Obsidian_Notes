---
tags: [documentation, ePub, audiobook]
author: [Yann Houry]
date: 13-09-2022
---

## À lire
- [ ] [Is Listening to Audiobooks Really Reading?](https://www.wired.com/story/is-listening-to-audiobooks-really-reading/?utm_brand=wired&utm_source=twitter&utm_medium=social&utm_social-type=owned&mbid=social_twitter)

<hr />

L'objectif de ce document est de présenter les différentes manières de créer un ePub contenant des enregistrements audios.

La plupart des applications proposées sont gratuites.

## Créer ses enregistrements
Avant de créer votre livre à proprement parler, il convient de procéder aux enregistrements. Cela peut se faire de multiples façons. Tout dépend de vos besoins.

- Voice Memos (iPad, iPhone)
- GarageBand (iPad, iPhone, Mac)
- [SoundTrap](https://www.soundtrap.com/)
- [Audacity](https://www.audacityteam.org/)
- Voice Recorder (Windows)

![[reduce-noise.png | 600]]

## Comment créer vos audiobooks/livres numériques ?
### Pages & GarageBand
La méthode la plus simple, si l'on possède un Mac ou un iPad est d'utiliser Pages & GarageBand. 

Voir le document [[What is an ePub file and why you are going to love it]] ou [[Create an ePub with Pages]] ainsi que les tutoriels [[Create an Audiobook With GarageBand 1]] et [[Create an Audiobook With GarageBand 2]] pour créer vos enregistrements audios.

On peut aussi ajouter des enregistrements audios sur des PDFs ou des ePubs de multiples façons.

Par exemple, on peut facilement créer un ePub ou PDF avec Google Docs et ajouter les enregistrements audios par la suite.

### Audra
[Audra](http://www.audra.pub/index.php) est gratuit et très simple d'utilisation. Il vous faudra créer un compte (pas de SSO malheureusement). Laissez-vous guider. Vous pourrez créer différents types de livre dans lesquels il vous sera facile d'ajouter vos enregistrements.

![[Audra.png | 600]]

Vous pourrez publier ou télécharger votre oeuvre.

### Book Creator
 Voir le tutoriel expliquant comment créer un ePub avec [Book Creator](https://www.icloud.com/keynote/0ZtZYKtWuUlbJKpyAM31HwFSg) (sur iPad).

On peut aussi utiliser la [version web](https://bookcreator.com/) sur Chromebook.

Dans la version gratuite, on peut créer jusqu'à 40 livres.

![[Book-Creator-Pricing.png | 600]]

La solution la plus simple et probablement la plus complète.

Il existe d'autres applications en ligne pour créer des ePubs. Je pense entre autres à :

- [Scribaepub](https://www.scribaepub.it/)
- [ePubEditor](http://www.epubeditor.it/home/home-en/)

Mais Book Creator est de loin l'application la plus facile d'utilisation et la plus complète. De plus, ces deux sites sont en italien, mais Google Translate ou Deepl vous arrange ça en un clin d'œil.

À noter que Scribaepub possède même un enregistreur audio intégré !

![[Scribaepub.png | 600]]

On peut toutefois recourir à d'autres possibilités comme Adobe Acrobat Reader, Sigil, OneNote ou encore Glide.

### Adobe Acrobat Reader
Des applications web comme [FlippingBook](https://flippingbook.com/?utm_source=flippingbook_online_cloud) vous proposent de convertir des PDF en livres numériques, mais cela a un coût et peut être fait (à moindre coût) avec d'autres apps comme [Notability](https://notability.com/) ou [PDF Expert](https://pdfexpert.com/) (si vous avez un Mac ou un iPad). 

Sinon, très simplement - mais à condition d'avoir la [version payante d'Acrobat Reader](https://acrobat.adobe.com/proxy/pricing/us/en/rich-media.html?trackingid=KRRSY&ttid=rchmd1&DTProd=Reader&DTServLvl=SignedOut) - vous pouvez ajouter des enregistrements audios dans un PDF qu'on aura construit avec un traitement de texte.

![[Acrobat-Reader.png | 600]]

![[Acrobat-Add-Rich-Media.png | 600]]

Lire [Add audio, video, and interactive objects to PDFs](https://helpx.adobe.com/hk_en/acrobat/using/rich-media.html?trackingid=KRRSZ&DTProd=Reader&DTServLvl=SignedOut).

### Sigil
Ce n'est pas la méthode la plus simple, mais c'est pratique. Si vous êtes un peu geek ou aimez coder, Sigil est fait pour vous. 

1. Télécharger [Sigil](https://sigil-ebook.com/sigil/download/).
2. Ajouter son enregistrement (fichier.mp3)
3. Ajouter le code HTML ci-dessous

````HTML
<audio controls="" autoplay=""><source src="../../OEBPS/Audio/abel-cain.mp3" type="audio/mpeg"/></audio>
````

Pour en savoir plus, lire [The HTML `<audio>` Element](https://www.w3schools.com/html/html5_audio.asp).

#### Première étape
![[Sigil-Add-Existing-Files.png | 600]]

#### Deuxième étape
![[Sigil-Fichier-MP3.png | 600]]

#### Troisième étape
![[Sigil-HTML-Code.png | 600]]

## OneNote
Ce ne sera pas à proprement parler un livre numérique contenant des enregistrements, mais si tout ce dont vous avez besoin est d'une application permettant facilement de créer puis de partager des fichiers audios, [OneNote](https://www.onenote.com/hrd?wdorigin=ondcauth2&wdorigin=ondcnotebooks) est à considérer.

![[OneNote.png | 600]]

Je l'ai utilisé quelque temps pour partager des dictées audios, mais on pourrait tout aussi bien insérer des lectures de conte ou des instructions vocales.

## Glide
Cette fois, on fera, [avec Glide](https://www.glideapps.com/), une véritable application (aucune connaissance en matière de code n'est requise).

Comme pour OneNote, j'ai beaucoup utilisé Glide pour partager des enregistrements audios, ce que vous pouvez voir [en cliquant sur ce lien](https://dictees.glideapp.io/).

![[Glide.png | 600]]

Le principe est très simple. Sur une feuille de calcul (Google Sheets par exemple), on construit un tableau contenant toutes les données dont on a besoin (par exemple un titre, un lien, une image...). Glide se chargera de donner une jolie apparence à tout cela.

![[Google-Sheets.png | 600]]

