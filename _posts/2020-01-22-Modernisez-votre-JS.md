---
layout:     post
title:      Bien commencer avec les Frameworks
date:       2019-07-07
summary: Vous souhaitez commencer à utiliser les super technos d'aujourd'hui comme React?
image: images/react.png
author: Andry
categories: [ Developper skills, React, ES2015, JavaScript, Modern, Programming ]
mathjax: true
featured: true
---

Tu souhaites débuter avec les super technos d'aujourd'hui comme **React**?

> Et bien , il faut te familiarisé avec les nouvelles avancées en **JavaScript**. Ces avancées sont apparues à partir de **2015**, dans la version du langage *appelée ES2015 (également connue sous le nom « ES6 »).*

Peut-être n’as tu tout simplement pas l’habitude de cette syntaxe : nous allons donc jeter un rapide coup d’œil sur les principales nouveautés que vous rencontrerez fréquemment à l’usage.

# Classes

*Les composants React* peuvent être définis sous forme de **fonctions ou de classes**. **ES2015** fournit du *« sucre syntaxique »* qui facilite considérablement la définition de classes, comparée à l’approche traditionnelle en JavaScript.

>Si tu viens d'un autre langage, POO , voir le  mot clé `Class` te fait peut-être dire, "Ah,🎟😆 JavaScript est enfin un langage orienté objet.." Détrompe-toi , il l'a toujours été , et même plus que `Java`. Bref...
Saches juste qu'en POO, on manipule des objets qui représentent des entités de notre programme (des composants, des documents, des utilisateurs…), et qu'une classe est en quelque sorte le plan de construction pour une catégorie d'objets (et l'usine qui les fabrique).

Cette syntaxe est comparable à celle trouvée dans de nombreux langages courants. Voici un exemple :

```javascript
class Account extends Component {
  constructor (props) {
    super(props)
    this.state = { loginState: 'logged-out' }

  render () {
    // …
  }
}
```

⚠ Fait bien attention aux points suivants :

* Le mot-clé  `class`  permet de définir un **corps de classe**, dont les éléments (constructeur, méthodes, etc.) n’ont pas besoin d’être séparés par des virgules, contrairement à ce qui se passe dans les littéraux objets.

* Il est facile de spécialiser une classe par héritage à l’aide du mot-clé `extends`

* Le mot-clé  `constructor`  permet de définir le constructeur de la classe ; au sein du constructeur,  `super(…)`  permet d’appeler le constructeur hérité, ce qui est d’ailleurs **obligatoire** si la classe en spécialise une autre avec `extends`  (et doit impérativement précéder toute manipulation de `this` ).

> 📑 **Note bien ceci:** si tu écrit une classe qui en spécialise une autre avec  `extends` , et que ta classe a son propre constructeur, celui-ci doit impérativement appeler le constructeur parent avec  `super(…)` , et ce avant de manipuler  `this`  de quelque façon que ce soit.
C'est juste une obligation syntaxique dans la spec : ton code JavaScript *ne devrait pas être valide sans cela*. En pratique, la plupart des moteurs JS (hors Babel, qui justement tourne « sous le capot » dans **Create React App** et dans la plupart des projets) attendront l'invocation du  `new`  pour détecter le souci, et lever une  `ReferenceError`  plutôt qu'une  `SyntaxError`. Dans tous les cas, ça ne marchera pas *in fine.*

* Les méthodes doivent être déclarées avec la nouvelle syntaxe de « méthodes concises », également disponible dans les littéraux objets :  `nom (paramètres) { … }` , contrairement à ce que l'on faisait auparavant dans les littéraux objets, comme par exemple   nom: `function (paramètres) { … } `.

Et parce que la Documentation on adore ça 😍 , c'est [par ici👉](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Classes)

# Fonctions fléchées

>Une syntaxe plus concise.

Le premier avantage des fonctions fléchées est **la concision de leur syntaxe.**

Traditionnellement, une fonction se déclare avec le mot-clé  `function`  suivi de la signature puis du bloc de fonction, au sein duquel tout  `return`  doit être explicite. Par exemple :

```javascript
const adults = [], minors = []
people.forEach(function (person) {
   if (person.age >= 10) {
      adults.push(person)
   } else {
       minors.push(person)
   })

people.map(function (person) {
   return person.firstName
})

```
Les fonctions fléchées ne nécessitent pas de mot-clé déclaratif. Lorsqu’elles sont intégralement constituées d’une expression à renvoyer, les accolades du bloc de fonction peuvent être omises,  ainsi que le mot-clé `return` .

Entre la signature et le bloc ou l’expression, on trouve une *fat arrow* (un nom bien naze!) , à savoir  `=>`

```javascript
const adults = [], minors = []
people.forEach((person) => {
  if (person.age >= 18) {
    adults.push(person)
  } else {
    minors.push(person)
  }
})

people.map((person) => person.firstName)

```
C’est une syntaxe raccourcie très pratique pour les **prédicats** (fonctions qui renvoient vrai ou faux selon leurs arguments, et qui sont par exemple passées aux méthodes `filter`, `every`  et  `some`) et les **mappers** (fonctions de transformation telles que celles passées à `map`). Dans ce deuxième cas, elles seront par exemple très utiles pour « réduire le bruit » dans les méthodes  `render` de nos composants React.

#### Oui, mais la question du `this`

Du fait qu' historiquement, JavaScript ne proposait qu’une manière de déclarer des fonctions : le mot-clé  `function`. Les fonctions ainsi déclarées avaient un comportement spécifique à JavaScript, fondé non pas sur l’endroit de leur déclaration dans le code, mais sur la syntaxe utilisée pour les appeler.  Cette syntaxe déterminait notamment, au sein de la fonction, la valeur de `this`.

Le fait de pouvoir appeler une fonction en contrôlant le rôle de `this` à l’intérieur a de nombreux avantages, mais comporte aussi un inconvénient : dans les fonctions de rappel (*callbacks*) notamment, on voulait souvent pouvoir continuer à utiliser le `this`  en vigueur « à la ligne du dessus », comme pour n’importe quel identifiant ordinaire.

```javascript
const name = 'Extérieur'

const obj = {
  name: 'Intérieur',
  runGreet () {
    // Ici, this.name est bien "Intérieur"
    setTimeout(function () {
      // Ici, this est soit l’objet global (mode laxiste de JS),
      // soit null (mode strict de JS)
    }, 0)
  }
}

obj.runGreet()
```
Les fonctions fléchées contournent ce problème en ne redéfinissant aucun identifiant lors de leur invocation (pas même  `this` ).

```javascript
const name = 'Extérieur'

const obj = {
  name: 'Intérieur',
  runGreet () {
    // Ici, this.name est bien "Intérieur"
    setTimeout(() => {
      // Ici, this n’est pas redéfini par la fonction,
      // car c’est une fonction fléchée : comme n’importe
      // quel identifiant, il est donc recherché dans les
      // portées englobantes, et trouvé au niveau de
      // runGreet, c’est donc aussi "Intérieur".
    }, 0)
  }
}

obj.runGreet()

```
Et cette capacité à ne pas interférer avec le `this`  en vigueur les rendra inestimables pour les méthodes  `render`  de nos composants React...!

# Déstructuration

La déstructuration te permet d’aller rapidement chercher plusieurs propriétés au sein d’un objet, ou plusieurs cellules au sein de n’importe quel objet itérable (comme un tableau) sans avoir à multiplier les déclarations ou affectations.

Par exemple, au lieu de faire ceci :

```javascript
// À l'ancienne
const firstName = this.props.firstName
const lastName = this.props.lastName
const onClick = this.props.onClick
```

On peut simplement faire :

```javascript
// Avec une déstructuration basée sur les noms
const { firstName, lastName, onClick } = this.props
```
Imaginons maintenant qu’on découpe un texte « prénom nom » en deux, et qu’on veuille affecter les parties à deux identifiants. Au lieu de faire :


```javascript
// À l'ancienne
const names = fullName.split(' ')
const firstName = names[0]
const lastName = names[1]
```
On peut faire :

```javascript
// Avec une déstructuration basée sur les positions
const [firstName, lastName] = fullName.split(' ')
```
Sympathique, non ? Il est possible d’aller beaucoup plus loin evidemment...

# Modules natifs, imports et exports

Pour découper notre application en **modules**, qui sont autant de **fichiers sources séparés.** Pour cela, nous aurons recours à la syntaxe officielle des **ES Modules.**
 Nous rendrons visibles les parties de nos modules que nous souhaitons à l’aide d’export  et nous irons chercher les parties qui nous intéressent dans d’autres modules à l’aide d’ import .

Voici un exemple de deux modules, le second utilisant le premier (ce sont deux fichiers différents, rassemblés ci-dessous pour plus de concision) :

```javascript

// Au sein du fichier textUtils.js

export function countWords (text) {
  return text.split(/\W+/u).filter(Boolean).length
}

export function normalizeSpacing (text) {
  return text.replace(/\s+/u, ' ').trim()
}

// Au sein d’un fichier main.js, dans le même répertoire :

import { countWords } from './textUtils'

console.log(countWords('Hello world, this is nice!'))
```

Il est également possible de déclarer un export « par défaut ». Dans ce cas nous pouvons l’importer sous le nom que l’on veut, sans avoir à recourir aux accolades :

```javascript

// Dans le module exportateur, SuperComponent.js :

export default class SuperComponent {
  // …
}

// Dans le module importateur, dans le même répertoire :

import GreatComponent from './SuperComponent'
```
Bravo 👏👏👏👏👏tu as désormais tous les éléments pour écrire vos composants React de façon moderne !



