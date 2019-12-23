---
layout:     post
title:      Qu'est-ce-qu'une API?
date:       2019-12-23
author: Andry
summary: Prototyper votre projet web
categories: [ JavaScript, API,beginner, introduction,Tools ]
mathjax: true
courses: true
image: images/api_dev.gif
---


Tout d'abord, nous survolerons le concept d'API — qu'est-ce que c'est, comment ça fonctionne, comment les utiliser dans votre code, et comment sont-elles structurées ? Nous verrons également quelles sont les principales APIs et leur utilisation.

## C'est quoi une API ?

Les APIs ou *Application Programming Interfaces* sont des constructions disponibles dans les langages de programmation pour permettre aux développeurs de créer plus facilement des fonctionnalités complexes. Elles s'occupent des parties de code plus complexes, fournissant au développeur une syntaxe plus facile à utiliser à la place.

>Tu n'as rien compris? C'est pourtant claire..

Plus concrètemnent, imagines des branchements électriques dans une maison, tout le monde à une maison...ou un appartement on s'en fiche; si tu souhaites utiliser un appareil dans ta maison/appartement, il te suffit de le brancher dans une prise et cela devrait normalement fonctionner(si tu as payé la facture ce mois-ci,evidemment!).

 Tu ne vas pas essayer  de le brancher directement à l'alimentation électrique — le faire serait réellement inefficace, stupide voire totalement débile et dangereux à réaliser, sauf si tu es électricien.

![plug](/images/electric_power.jpg)

## Utiliser une API:

Rien ne vaut l'exemple comcret donc :

>Imagine que tu as un ton site web, parce que tu as assité à [notre premier workshop](https://www.meetup.com/fr-FR/Apprendre-le-developpement-web/) et que tu y exposes tes oeuvres personnelles. Génial! Tu fais de la peinture et tu veux que les gens soient capables d’acheter tes créations.
Concevoir le code pour prendre en charge toutes les cartes bancaires serait incroyablement difficile,mais après avoir lu cet artlicle tu décides d’utiliser un système extérieur comme *PayPal*, et de l’intégrer à ton site.

Pour trouver *l'API de Paypal*, il te suffit de chercher “PayPal API” sur Internet. C’est une technique que tu  peux utiliser pour trouver quasiment toutes les API des sites qui en proposent. Et c'est aussi la technique qu'utilise un développeur BAC+5, pour faire n'importe quoi d'autre..Oui je balance et alors!

Soyons serieux, sur la page de [l’API elle-même](https://developer.paypal.com/docs/api), tu peux trouver la documentation dont tu auras besoin pour intégrer le code de ton site avec leur service.
C’est d’assez haut niveau et assez technique quand tu le vois pour la première fois,(c'est pour justifier le salaire) mais si  tu te detent une seconde, nous allons voir cela ensemble.

>Ce qu'il faut retenir c'est: *une API vient presque toujours avec une documentation.*

La documentation du code est un texte écrit par les développeurs qui sacrifient leur vies sociales et qui rend plus facile l’utilisation du code de cette API. On dit merci qui?

Elle explique comment le code fonctionne, pourquoi il a été écrit d’une certaine façon et pas d’une autre, comment contribuer au projet, et bien plus encore. Lire la documentation est très important même si c'est très chiant... pour bien intégrer l’API d’une autre plateforme.


## Que peuvent faire les API ?

Il y a plusieurs sortes d'API mais en tant qu'entrepreneur ceux qui vont plus nous intéresser ce sont les **APIs tièrces.**

Les API tierces sont des API qui sont fournis par des tiers, généralement des entreprises comme *Facebook, Twitter ou Google,* qui permettent d'accéder à leurs données et/ou leurs fonctionnalités grâce à JavaScript afin de les utiliser sur son site. Utiliser **une API de cartographie afin d'afficher une carte** sur une page est un exemple.

### APIs tierces courantes

Il y a une grande variété d'APIs tierces; en voici quelques unes des plus populaires que vous allez probablement utiliser tôt ou tard :

* L'[API Twitter](https://developer.twitter.com/en/docs) — vous permet, par exemple, d'afficher vos derniers tweets sur votre site Web.

* L'[API Google Maps](https://cloud.google.com/maps-platform/) — vous permet d'afficher des cartes sur vos pages web. Il s'agit à dire vrai d'une suite complète d'APIs, qui gèrent une grande variété de tâches, comme en témoigne l'{API Picker Google Maps.](https://developers.google.com/maps/documentation/api-picker)

* L'[API Facebook](https://developers.facebook.com/docs/) — vous permet d'utiliser diverses parties de l'écosystème Facebook au profit de votre application, par exemple permettre de se connecter via Facebook, accepter des paiements via l'application, déployer des campagnes publicitaires ciblées, etc.

* L'[API YouTube ](https://developers.google.com/youtube/)— vous permet d'intégrer des vidéos YouTube sur votre site, de rechercher sur YouTube, de créer des playlists, etc.

* L'[API Twilio](https://www.twilio.com/) — fournit un framework permettant de créer des fonctionnalités d'appel vocal et vidéo dans votre application, d'envoyer des SMS/MMS depuis vos applications, et plus encore.

>Note : Vous pouvez trouver des informations sur beaucoup plus d'API tierces dans [le répertoire Programmable Web API](https://www.programmableweb.com/category/all/apis).

Maintenant tu sais ce que c'est qu'une API, son utilisation. Et si tu veux en savoir plus , je t'invite à nous rejoindre sur [@Meetup](https://www.meetup.com/fr-FR/Apprendre-le-developpement-web/), cela va être le thème de nos prochains workshops. A bientôt!

