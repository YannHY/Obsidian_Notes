---
tags: [Documentation, Pix]
author: [Yann Houry]
date: 07-03-2022
---

Envoi des convocations avec Google Sheets et l'extension form Mule

![[pix-certification-template.png | 600]]
![[pix-form-mule.png | 600]]
## HTML pour form Mule
```HTML
Bonjour <<Prénom>> <<Nom>>,

Voici votre convocation pour la certification Pix à la session <<Session>>.

<ul>
<li>Date : <<Date>></li>
<li>Heure : <<Heure>></li>
<li>Salle : <<Salle>></li>
</ul>

<strong>Vos informations</strong>
S'il vous plait, vérifiez que les informations ci-dessous sont correctes. Dans le cas contraire, informez-moi au plus tôt.

<ul>
<li>Date de naissance : <<Naissance>></li>
<li>Commune de naissance : <<Commune>></li>
</ul>

<strong>Munissez-vous</strong>
❏	d’une pièce d’identité en cours de validité, avec photo (carte d’identité, passeport, permis de conduire ou titre de séjour)
❏	des informations de connexion à votre compte Pix (adresse électronique et mot de passe)

<strong>Prenez vos précautions</strong>
❏	vous devrez laisser votre sac à l’entrée, y compris tout appareil électronique permettant de communiquer (smartphone, montre connectée, etc.)
❏	vous ne pourrez pas manger, mais vous pourrez boire, sauf indication contraire dans les conditions d’utilisation de la salle qui vous accueille

Retrouvez toutes les informations sur le déroulé de la certification en téléchargeant la fiche d’information au candidat disponible <a href="https://pix.fr/se-certifier">sur cette page</a>.

Si vous avez des questions, n'hésitez pas à m'écrire.

Cordialement,
Kind regards,

Yann Houry
Directeur de l'innovation & de la recherche académique

<img src="https://www.ralentirtravaux.com/images-lycee/logo.jpeg">
```
 