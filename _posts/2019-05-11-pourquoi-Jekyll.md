---
layout:     post
title:      Pourquoi choisir Jekyll pour son site?
categories: [ Jekyll, tutorial ]
image: images/dribbble.gif
Author: Andry
categories: [ Developper skills, Jekyll, MVP, Startup ]
mathjax: true
module: true
---

>Il faut savoir que pour créér ce site j'ai choisi d'utiliser *Jekyll* .
Pourquoi ce choix?



Jekyll est un générateur de site statique écrit en *“Ruby”* qui gagne en popularité, de Google à Netflix en passant par Mailchimp, Mapbox ou NodeJS, ils sont partout et sont devenus le choix de la raison pour les sites de contenus **à fort trafic**. Leurs usages évoluent et de nouveaux services dédiés viennent enrichir et faciliter l’expérience utilisateur des contributeurs et des développeurs.

Cette stack permet aux différents intervenants de se concentrer sur l’essentiel. Les rédacteurs peuvent ainsi rédiger leurs articles au format Markdown, un format texte très simple et très lisible, qui facilité la portabilité.



## Pourquoi ne pas choisir un CMS comme Wordpress?


Un système de gestion de contenu (CMS) tel que "Wordpress", (*je cite ce dernier du fait de sa popularité auprès des developpeurs et des particuliers, mais il y en a  d'autres tel que Joomla, Drupal, Typo3, Magento, Prestashop*), aurait été parfait.

Le problème justement réside dans sa popularité et aussi la technologie qu'il embarque.
Wordpress est écrit en **PHP**, repose sur **une base de données MySQL** et est distribué par l'entreprise américaine [Automattic](https://automattic.com/).
Du fait de sa popularité, (*je n'ai pas les chiffres en téte mais je crois que c'est 30% des sites mondiaux, c'est énorme*), les sites Wordpress subissent des attaques incessantes.


![cms](/images/cms.jpeg)

### Autre argument de taille: la vitesse du site

Le couple **PHP & MySQL et hébergement mutualisé sur OVH**, si vous rajoutez des **plugins inutiles**, sa ne fait pas bon ménage! Et cela se fait ressentir.

Comment?

Par le temps de chargement... Votre site qui rame comme jamais et ce n’est le top!

## Jekyll, comment ça marche ?

Comme je l'ai dit plus haut Jekyll est un générateur de site statique écrit en *Ruby*, ce qui peut paraître tout à fait absurde par rapport à un CMS mais cela apporte bien des avantages et notamment le fait qu’il peut etre couplé à git et github.

Et c’est là, tout l’intérets, je m’explique:

**Github** est une architecture qui tourne autour de **Git**, un outil open source de *versionning*, c’est-à-dire que le concept de *backup* est compris dans l’outil, en plus de la possibilité de manière assez simple de venir éditer un article comme celui-ci par exemple.

Les pages sont **statiques**, il n’y a donc pas mieux en termes de vitesse et de sécurité pour les visiteurs et l'utilisateur.
Pas besoin de disposer d’un *serveur surdimensionné*, car les pages sont statiques, et les serveurs aiment bien ça, le contenu statique. En plus, [**Github pages**](http://localhost:4000/developper/skills/2019/05/05/Host-any-front-end/) est **gratuit**, oui vous avez bien lu, c'est *entièrement gratuit.*



![free](/images/free.jpeg)

---


Vous avez une copie entière de votre site sur votre ordinateur.
Vous pouvez faire tourner votre site en local avant de le lancer en production. Pour chaque version. Et c'est tout simplement génial.

Et dès que vous déployez le site, si il n’y a pas d’erreurs, il est mis en ligne automatiquement.

> Aucun paramétrage nécessaire pour indiquer à Github : “Hey, j’ai foutu un Jekyll sur ce repo, déploie-le moi dude”. Il le trouve, et il le lance. Et c'est tout!

Pour d’autres services, il est possible de les déployer aussi sur Github (ou d’autres outils tels que des Gitlabs), mais cela implique soit de passer par un outil de CI (Intégration Continue) qui va détecter les changements du dépôt Git et générer le site statique, ou de compiler soi-même lors de chaque modification.

## Conclusion

Servir du « statique » n’est pas du tout une mode destinée à rester confidentielle parmi *les hackers*, c’est une réponse simple à des problématiques complexes. Gardez en tête que **78% des sites sous Wordpress souffrent de vulnérabilités et que quand une faille de sécurité impacte Drupal, des millions de sites sont concernés.**

C’est donc une solution que vous devriez sérieusement considérer si vous souhaitez réduire vos coûts d’infrastructure sur des sites à fort trafic. Sur des sites très fréquentés le coût peut être divisé par 15 ou plus.

*Le full statique* est idéal pour des sites de contenus : *présentation produit, documentation, blog ou application web (progressive) en JavaScript, en revanche il n’est pas adapté pour des sites où le contenu est majoritairement généré par les utilisateurs.*






