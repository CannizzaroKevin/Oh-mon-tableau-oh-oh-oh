# Oh mon tableau - Oh oh oh 🎶

Embarquez dans une aventure inter-galactique 🚀🪐 pour maîtriser les tableaux et objets en JavaScript, en aidant Bob, Lucie, et leur fidèle robot domestique !

## Contexte

Dans le futur lointain, Sam doit confier la gestion de la maison à Bob, son fils, pendant une mission spatiale. Les instructions nécessaires sont enregistrées dans le robot domestique sous forme de tableaux et d'objets pour guider Bob et sa petite sœur, Lucie.

Sam laisse un message affectueux, rappelant à Bob où trouver les instructions pour mettre la table et le menu, et signale avoir laissé des notes utiles dans la mémoire du robot.

>*Bob chéri, 
> merci de t'occuper de mettre la table pendant que je suis en mission. Si tu as oublié quels couverts mettre, ou si tu veux savoir quel est le menu, demande au robot.
Je lui ai enregistré des notes pour toi! Les couverts sont enregistrés
au nom de `couverts`, et le menu au nom de `menu`. 
Je t'aime, bisous  
>P.S. : j'ai aussi noté dans la mémoire du robot la liste des jours  
>Vers l'infini et super plus loin encore <3*

## Tes missions

### Step 01 : Back to the future

Tu incarnes Sam et ton défi est de programmer le robot pour qu'il aide tes enfants pendant ton absence. Ton objectif ? Enregistrer dans la mémoire du robot :

1. La liste des couverts pour 1 personne
2. La liste des jours pour 3 jours consécutifs
3. Une liste d'entrées (3)
4. Une liste de plats de résistance (3)
5. Une liste de desserts (3)

Consignes claires, n'est-ce pas ? Mais si jamais tu te sens un peu perdu dans l'espace, voici un petit coup de pouce sous forme de code. Attention, l'exemple ci-dessous est sur un autre thème pour stimuler ta créativité !

<details>
<summary>Exemple de code (clique pour ouvrir)</summary>

Imaginons que tu veuilles créer une liste de tâches pour une journée typique sur Terre. Voici comment tu pourrais procéder en JavaScript :

```javascript
// Liste des tâches pour une journée
const taches = ["Se réveiller", "Prendre un petit-déjeuner", "Aller au travail"];

// Affichage des tâches dans la console
console.log("Mes tâches pour la journée :");
taches.forEach(tache => console.log(tache));
```

Cet exemple montre comment créer et utiliser un tableau en JavaScript. Garde en tête cette logique pour créer tes listes dans le cadre de l'atelier !

</details>

---

### Step 02 : Bob va mettre les couverts

Maintenant, c'est à toi de jouer, Bob ! Tu sais que le robot a toutes les infos dont tu as besoin. Ton but ? Lui demander de préparer la table avec les couverts pour toi et Lucie. Utilise tes connaissances pour formuler la demande. 

**Astuce :** tu auras peut-être besoin de créer la liste des enfants pour qui le robot doit préparer la table.

Ne t'inquiète pas, si tu as besoin d'un peu d'inspiration sur comment dialoguer avec le robot, jette un œil aux exemples ci-dessous. Mais souviens-toi, c'est juste pour te donner des idées. Ton vrai défi concerne les couverts !

<details>
<summary>Exemple de code (clique pour ouvrir)</summary>

Voici un exemple simple pour commencer :

```javascript
// Nom de ton animal de compagnie
const nomAnimal = "Pixel";

// Demande à l'assistant de te rappeler de nourrir ton animal
console.log(`Assistant, rappelle-moi de nourrir ${nomAnimal} ce soir.`);
```
Maintenant, imaginons que tu as deux animaux de compagnie et que tu souhaites que l'assistant te rappelle de les nourrir tous les deux :
```javascript
// Noms de tes animaux de compagnie
const animaux = ["Pixel", "Byte"];

// Boucle pour demander à l'assistant de rappeler de nourrir chaque animal
animaux.forEach(animal => {
  console.log(`Assistant, rappelle-moi de nourrir ${animal} ce soir.`);
});
```
Ce deuxième exemple illustre comment utiliser une boucle pour traiter plusieurs éléments, similaire à ce que tu pourrais faire pour préparer la table pour Bob et Lucie.

</details>

---

### Step 03 : Aïe, Lucie n'utilise pas de couteau !

Bob doit adapter les couverts pour Lucie en suivant ces étapes simples :

1. Faire une copie de la liste des couverts.
2. Retirer le couteau, car Lucie est trop petite pour l'utiliser.
3. Remplacer le verre par un gobelet, plus adapté pour Lucie.
4. Renommer les couverts restants en ajoutant " de Lucie" à la fin de chaque couvert.

<details>
<summary>Exemple de code (clique pour ouvrir)</summary>

Imaginons que nous ajustons le contenu d'une trousse pour Paul. Il a besoin de certaines fournitures pour l'école, mais nous devons les personnaliser et nous assurer qu'elles sont adaptées :

```javascript
// Liste originale des fournitures
let fournitures = ["crayon", "compas", "ciseaux", "gomme"];

// Faire une copie de la liste
let fournituresPaul = [...fournitures];

// Supprimer "ciseaux" car inappropriés pour Paul
let indexCiseaux = fournituresPaul.indexOf("ciseaux");
if (indexCiseaux !== -1) {
    fournituresPaul.splice(indexCiseaux, 1);
}

// Paul a besoin d'un taille-crayon
fournituresPaul.push("taille-crayon");

// Personnaliser chaque fourniture pour Paul avec forEach
fournituresPaul.forEach((fourniture, index, leTableau) => {
    leTableau[index] = fourniture + " de Paul";
});

console.log(fournituresPaul);
```

L'opération `indexCiseaux !== -1` est utilisée pour vérifier si l'élément "ciseaux" existe dans le tableau. Si `indexOf` renvoie `-1`, cela signifie que l'élément n'est pas dans le tableau. Sinon, l'élément est présent, et nous pouvons procéder à sa suppression avec `splice`. 

L'utilisation de `forEach` nous permet de parcourir chaque élément du tableau `fournituresPaul` et de le personnaliser en ajoutant " de Paul" à la fin de chaque nom. Cette méthode applique une action sur chaque élément du tableau, ce qui est idéal pour le renommage et la personnalisation.

</details>

---

### Step 04 : cette fois on met la table !

Avec les préparatifs des couverts adaptés pour Bob et ceux spécialement ajustés pour Lucie, Bob est prêt à mettre la table. Mais surprise ! Un copain, Bill, est venu jouer et voudrait bien manger avec eux. Bob doit maintenant préparer la table en s'assurant que chacun ait l'ensemble de couverts approprié.

Pseudo-code pour organiser la mise en place des couverts :

> Ajuster ou créer un tableau "convives" avec Bob, Lucie, et Bill.
> Pour chaque convive :
> - Si le convive est Lucie, utiliser les couverts de Lucie.
> - Sinon, placer les couverts standards.

<details>
<summary>Cliquez ici pour voir un exemple simple et un exemple avancé</summary>

Voici d'abord un exemple simple qui illustre comment différencier les actions basées sur les caractéristiques spécifiques des éléments d'un tableau :

```javascript
let animals = ["🐈", "🐟"];
const environment = ["air", "tree"];
const fishEnvironment = ["water", "plants"];

// Un nouvel animal arrive dans la famille
animals.push("🐈‍⬛");

// Pour chaque animal, il faut le bon environnement :
animals.forEach(animal => {
  if (animal === "🐟") {
    console.log(`Pour ${animal}, l'environnement nécessaire est : ${fishEnvironment.join(", ")}`);
  } else {
    console.log(`Pour ${animal}, l'environnement nécessaire est : ${environment.join(", ")}`);
  }
});
```

Maintenant, voici une version plus avancée qui utilise un objet pour associer chaque animal à son environnement spécifique. Cette méthode permet un accès direct à l'environnement de chaque animal via une clé :

```javascript
let animals = ["🐈", "🐟"];
const environment = ["air", "tree"];
const fishEnvironment = ["water", "plants"];
let home = {};

// Un nouvel animal arrive dans la famille
animals.push("🐈‍⬛");

// Associer chaque animal à son environnement dans l'objet home
animals.forEach(animal => {
  if (animal === "🐟") {
    // Associer le poisson à son environnement spécifique
    home[animal] = fishEnvironment;
  } else {
    // Associer les autres animaux à l'environnement par défaut
    home[animal] = environment;
  }
});

// Affichage de l'environnement pour le poisson
console.log(`L'environnement pour 🐟 est : ${home["🐟"].join(", ")}`);
```

Dans la version avancée, l'utilisation de l'objet `home` permet une gestion plus structurée et flexible des données, offrant une manière claire et directe de relier chaque animal à son environnement.

</details>

---

### Step 05 : Organiser le menu pour chaque jour

Après avoir préparé les listes nécessaires à l'étape 1, Bob souhaite maintenant organiser le menu de chaque jour de manière à ce que chaque repas soit bien planifié et facile à consulter pour tous les convives.

**Objectif :** Utiliser les listes d'entrées, de plats de résistance, et de desserts pour créer un menu détaillé pour chaque jour.

**Instructions :**

- Utiliser la liste des jours pour 3 jours consécutifs.
- Associer à chaque jour une entrée, un plat principal, et un dessert en utilisant les listes préparées à l'étape 1.

<details>
<summary>Exemple de code (clique pour ouvrir)</summary>

Imaginons un planning d'activités pour un camp de vacances, où chaque jour doit proposer une activité différente pour les enfants. Voici comment vous pourriez structurer cela en code, en utilisant des listes similaires à celles que vous avez créées pour les repas :

```javascript
// Listes des jours et des activités
let jours = ["Lundi", "Mardi", "Mercredi"];
let activitesMatin = ["Tir à l'arc", "Natation", "Randonnée"];
let activitesApresMidi = ["Escalade", "Canoe", "VTT"];
let activitesSoir = ["Feu de camp", "Observation des étoiles", "Jeux de société"];

// Création d'un planning pour chaque jour
let planningActivites = {};

jours.forEach((jour, index) => {
  planningActivites[jour] = {
    matin: activitesMatin[index],
    apresMidi: activitesApresMidi[index],
    soir: activitesSoir[index]
  };
});

// Affichage du planning des activités
console.log("Planning des activités du camp :");
for (let jour in planningActivites) {
  let activites = planningActivites[jour];
  console.log(`${jour} : Matin - ${activites.matin}, Après-midi - ${activites.apresMidi}, Soir - ${activites.soir}`);
}
```
Cette structure montre comment organiser et accéder à des informations structurées pour faciliter la planification et la communication, similaire à la préparation d'un menu quotidien pour le dîner.

</details>

---

### Step 06 : Gérer les intolérances alimentaires

Bob planifie d'inviter Clémentine pour le goûter, où ils mangeront des fruits.

**Objectif :** Vérifier et ajuster la liste des fruits pour s'assurer qu'elle est adaptée à tous.

**Instructions :**

- Créer la liste de fruits disponibles à la maison : (oranges, bananes, poires, fraises)
- Clémentine a une intolérance aux pépins de fraise : vérifier si la liste contient des fraises et les retirer si nécessaire.

<details>
<summary>Exemple de code (clique pour ouvrir)</summary>

Imaginons une playlist pour une soirée. Un de vos amis n'apprécie pas le genre "pop". Voici comment vous pourriez ajuster votre playlist pour s'assurer que tout le monde passe un bon moment :

```javascript
// Liste initiale de chansons pour la soirée
let playlist = [
  { titre: "Chanson 1", genre: "rock" },
  { titre: "Chanson 2", genre: "pop" },
  { titre: "Chanson 3", genre: "electro" },
  { titre: "Chanson 4", genre: "rock" }
];

// Genre de musique à éviter
let genreAEviter = "pop";

// Filtrer la playlist pour exclure les chansons d'un certain genre
let playlistAdaptee = playlist.filter(chanson => chanson.genre !== genreAEviter);

// Afficher la playlist adaptée
console.log("Playlist adaptée pour la soirée :");
playlistAdaptee.forEach(chanson => console.log(chanson.titre));
```

Cet exemple illustre comment filtrer une collection basée sur des préférences ou restrictions spécifiques, de manière similaire à l'ajustement d'une liste de fruits en prenant en compte les intolérances alimentaires.

</details>

---

Et voilà, tout est prêt ! Félicitations 🤩
