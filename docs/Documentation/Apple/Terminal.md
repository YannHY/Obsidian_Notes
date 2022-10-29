---
tags: [Documentation, Mac, Apple]
---

## À lire
- [Lesson 2. Bash Commands to Manage Directories and Files](https://www.earthdatascience.org/courses/intro-to-earth-data-science/open-reproducible-science/bash/bash-commands-to-manage-directories-files/)
- [macOS Terminal commands every Mac user should know](https://www.techrepublic.com/article/macos-terminal-commands-every-mac-user-should-know/)
- [5 Useful Terminal Tricks for Mac Users](https://www.wired.com/story/5-useful-terminal-tricks-for-mac/)

- [x] [Lesson 13: Introduction to the Command-Line Interface](https://docs.jamf.com/education-services/jamf-100-course/4.1/Lesson_13__Introduction_to_the_Command-Line_Interface.html)
- [x] [Lesson 14: Navigate the File System with Terminal](https://docs.jamf.com/education-services/jamf-100-course/4.1/Lesson_14__Navigate_the_File_System_with_Terminal.html)
- [x] [Lesson 15: Use Terminal More Efficiently](https://docs.jamf.com/education-services/jamf-100-course/4.1/Lesson_15__Use_Terminal_More_Efficiently.html)
- [ ] [5 Useful Terminal Tricks for Mac Users](https://www.wired.com/story/5-useful-terminal-tricks-for-mac/)
- [ ] https://www.macworld.com/article/195806/erasefreespace.html
- [ ] [](https://www.macg.co/macos/2021/11/macos-monterey-et-ios-15-testent-la-reactivite-de-votre-connexion-internet-125369)

## cd
= Change directory

`cd ~/desktop`
ou 
`cd ..` (mais ne pas oublier l'espace)

`cd ~/Library/Mobile\ Documents/com~apple~CloudDocs/`

`cd ~/Library/Mobile\ Documents/com~apple~CloudDocs/documents`

Mais impossible de localiser précisément un fichier sur iCloud.

On peut glisser et déposer un dossier ou un fichier. On a le lien automatiquement.

## mkdir
= make directory
`mkdir Essai` (crée un dossier `Essai`)

## touch
touch test.txt
(crée un fichier `test.txt`)

## mv
`mv test.txt essai.txt`
Change le nom de `test.txt`

`mv essai.txt Essai` (déplace le fichier dans le dossier `Essai`)

On peut combiner les deux
`mv essai.txt Essai/nouveau.txt` (le fihcier essai.txt est déplacé dans le dossier Essai et est renommé nouveau.txt)

## cp
fait une copie du fichier et le place dans le dossier Essai
`cp nouvelessai.txt Essai`

## pwd
montre le chemin (absolute path) = `Users/yannhoury`

## ls
Liste le contenu d'un dossier

## rm
Delete a file `rm fichier.md` (supprime complètement le fichier qui n'est pas placé dans la corbeille. On ne peut pas annuler)

`rm nouvelessai.txt/Essai` (supprime le fichier dans le dossier Essai)

Delete a directory `rm -r dossier`

[Documentation](https://www.macworld.com/article/222596/master-the-command-line-deleting-files-and-folders.html)

## open
Ouvre le fichier (avec app par défaut)
`open IMG_2772.jpg`

Ouvre le fichier dans l'app que l'on a spécifié
`open -a Safari IMG_2772.jpg`

Ouvre une URL
open -a Safari https://www.ralentirtravaux.com

Ouvre le dossier
`open Essai`

Ouvre une app
`open System/Applications/TextEdit.app`

Appuyer sur flèche du haut répète la dernière commande

## Pandoc
"pan-" = tout en grec. -> tous les documents ("doc"). Permet de convertir tout fichier.

 `pandoc fichier.md -o fichier.odt`
 
 On commence toujours par `pandoc`
 + fichier de départ (input) 
 + `-o` (= output)
 + fichier qu'on veut obtenir (output)

À chaque fois, on indique l'extension de départ et l'extension d'arrivée.

<iframe width="560" height="315" src="https://www.youtube.com/embed/yYZiO6CVtj8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- https://www.techrepublic.com/article/how-to-access-your-local-icloud-folder-from-the-terminal/
- https://osxdaily.com/2017/11/16/access-icloud-drive-command-line-mac/
- https://michaelsoolee.com/icloud-drive-terminal/
- https://perishablepress.com/list-files-folders-recursively-terminal/

## Flush DNS
https://phoenixnap.com/kb/how-to-flush-dns-cache

---

- [How to convert RTF to Markdown on the UNIX/OSX command line similar to pandoc](https://stackoverflow.com/questions/30448176/how-to-convert-rtf-to-markdown-on-the-unix-osx-command-line-similar-to-pandoc)

## Textutil
- [Free conversion of text files with textutil](https://eclecticlight.co/2018/03/28/free-conversion-of-text-files-with-textutil/)
- [textutil](https://ss64.com/osx/textutil.html)
- [Convert TXT, RTF, DOC and DOCX files with textutil](https://www.chriswrites.com/convert-txt-rtf-doc-and-docx-files-with-textutil/)


```
textutil -stdin -convert html  -stdout | pandoc --from=html --to=markdown
```


textutil -convert html medecin.rtf

pandoc medecin.html -o medecin.md

## How to play audio files in the Terminal
https://www.macworld.com/article/194771/105audioterm.html

