---
layout:     post
title:      Définissez des objets et leurs attributs avec des classes
date:       2019-07-07
image: images/js_tuto.png
author: Andry
categories: [ Developper skills, JavaScript, Modern, Programming, Classes, Objects ]
mathjax: true
featured: true
---

>Vous avez probablement entendu auparavant le terme **objet** dans un contexte de programmation.



Commençons par nous intéresser à quelques objets du monde réel, comme les stylos, les livres, les smartphones, les ordinateurs, etc.

![sublime](/images/objects.jpg)

Vous reconnaissez tous les stylos — à piston, à bille, feutre, gel, etc. — comme faisant partie du type d'objet : stylos. Vous pouvez écrire avec, ils utilisent de l'encre et peuvent se tenir à une main.

C'est la même chose pour les livres : ils ont une couverture, un certain nombre de pages, un titre, et un ou plusieurs auteurs.

Vous remarquez des points communs entre différents objets et vous notez ces informations pour créer une représentation mentale d'une catégorie d'objets.

Cette liste mentale d'attributs sert de **modèle** pour cet objet. En programmation, on l'appelle **une classe.** Pour créer une classe, vous pouvez choisir le nom de votre choix. C'est pour cela qu'on l'appelle un **type nommé.** Vous le verrez, les classes permettent aussi de regrouper beaucoup de détails ; c'est pourquoi elles s'appellent aussi des **types complexes.**

Avant de plonger dans les classes, observons un type JavaScript complexe : **l'objet.**

#### Découvrez les objets

Les objets JavaScript sont écrits en **JSON (JavaScript Object Notation).** Ce sont des séries de paires **clés/valeurs** séparées par **des virgules,** entre **des accolades.**

 Les objets peuvent être enregistrés dans une variable :

```javascript
let myBook = {
    title: 'Le facteur temps ne sonne jamais deux fois',
    author: 'Etienne Klein',
    numberOfPages: 250,
    isAvailable: true
};
```

Chaque clé est une chaîne (title, author, numberOfPages...), et les valeurs associées peuvent avoir tout type de données (nombre, chaîne, etc).

> Construire des objets présente un avantage essentiel : cela permet de regrouper les attributs d'une chose unique à un même emplacement, que ce soit un livre, un profil d'utilisateur ou la configuration d'une application, par exemple.

#### Accédez aux données d'un objet

Maintenant que vous savez comment créer un objet en JavaScript, voyons comment accéder aux données dans un objet avec **la notation pointée (dot notation),** expliquée ci-dessous.

Une fois qu'un objet est enregistré dans une variable, vous pouvez accéder à ses données comme dans l'exemple ci-dessous.

```javascript
let myBook = {
    title: 'Le facteur temps ne sonne jamais deux fois',
    author: 'Etienne Klein',
    numberOfPages: 250,
    isAvailable: true
};

let bookTitle = myBook.title;  // "Le facteur temps ne sonne jamais deux fois"
let bookPages = myBook.numberOfPages  // 250
```
Pour cela, utilisez le nom de la variable qui contient l'objet, un point `(  .  )`, puis le nom de la clé dont vous souhaitez récupérer la valeur.

#### Manipulez des classes

La construction d'un objet à la main, par la notation à accolades vue précédemment, convient bien à des objets simples et uniques. Mais vous aurez souvent besoin de beaucoup d'objets du même type. C'est là que les classes sont utiles.

Comme expliqué précédemment, une classe est un modèle pour un objet dans le code. Elle permet de construire plusieurs objets du même type (appelés instances de la même classe) plus facilement, rapidement et en toute fiabilité.

Voyons comment construire une classe dans le code.

Pour créer une classe dans JavaScript, utilisez le mot clé  `class`, suivi par un nom. Encadrez ensuite le code de la classe entre accolades :

```javascript
class Book {

}
```

Pour cette classe, nous souhaitons que chaque  `Book`  ait un titre, un auteur et un nombre de pages. Pour cela, vous utilisez ce qu'on appelle **un constructor**.

> NB: Le  `constructor` d'une classe est la fonction qui est appelée quand on crée une nouvelle instance de cette classe avec le mot clé `new`.

```javascript
class Book {
    constructor (title, author, pages) {

    }
  }
```

Il y a un ensemble d'instructions à suivre à l'intérieur du  constructor  pour créer une instance de la classe  `Book`. Pour attribuer le titre, l'auteur et le nombre de pages reçus à cette instance, utilisez le mot clé  `this`  et la notation `dot`.


```javascript
class Book {
    constructor (title, author, pages) {
    this.title = title;
    this.author = author;
    this.pages = pages;
    }
  }

```
Ici, le mot clé  `this`  fait référence à la nouvelle instance. Donc, il utilise la notation dot pour attribuer les valeurs reçues aux clés correspondantes.

Maintenant que la classe est terminée, vous pouvez créer des instances par le mot clé  `new`  :

```javascript
class Book {
    constructor (title, author, pages) {
    this.title = title;
    this.author = author;
    this.pages = pages;
    }
  }
let newBook = new Book('Le facteur temps ne sonne jamais deux fois, 'Etienne Klein', 250 );
```
Cette ligne crée l'objet suivant :

```javascript
{
    title: 'Le facteur temps ne sonne jamais deux fois',
    author: 'Etienne Klein',
    numberOfPages: 250,

}
```
Avec une classe  Book, vous pouvez créer facilement et rapidement de nouveaux objets ` Book`.

Voilà ! Maintenant, à vous de jouer. La meilleure façon d'apprendre les classes est d'en créer une vous-même.

#### Pour résumer

* les objets avec les paires clés/valeurs en notation JSON. Ils permettent d'enregistrer plusieurs éléments de données associés dans une même variable ;

* la notation pointée (dot) qui donne accès aux valeurs d'un objet et la possibilité de les modifier ;

* les classes, et comment l'utilisation de classes peut vous permettre de créer des objets plus facilement et de façon plus lisible.
