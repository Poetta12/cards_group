# Card Mouse Follow - Interactive Card Group

## Description

**Card Mouse Follow** est un projet interactif développé avec **HTML**, **CSS**, et **JavaScript**. Ce projet met en avant un groupe de cartes dont les arrière-plans réagissent au mouvement de la souris. Lorsque l'utilisateur déplace le curseur, les cartes ajustent leur arrière-plan en temps réel, créant une expérience visuelle dynamique et immersive.

## Fonctionnalité principale

Le projet utilise les événements de mouvement de la souris pour modifier la position de l'arrière-plan de chaque carte. Chaque carte comprend :
- Un effet de mouvement fluide qui suit le curseur de la souris.
- Une superposition de texte informatif sur chaque carte.
- Des transitions douces pour améliorer l'expérience utilisateur.

## Détails du fonctionnement du code

### HTML

Le fichier `index.html` contient la structure de base de la page. Les éléments principaux incluent :

- **Conteneur de cartes** : Une div englobante qui contient toutes les cartes.
- **Div pour chaque carte** : Chaque carte possède une classe qui lui est propre et reçoit des événements de souris.

#### Extrait HTML principal :
```html
<div class="card-container">
    <div class="card" id="card1">
        <h3>Titre de la carte 1</h3>
        <p>Description de la carte 1.</p>
    </div>
    <div class="card" id="card2">
        <h3>Titre de la carte 2</h3>
        <p>Description de la carte 2.</p>
    </div>
    <!-- Autres cartes ici -->
</div>
```

### CSS

Le fichier `styles.css` gère l'apparence des cartes et des effets de suivi de la souris. Les éléments clés incluent :

- **Style des cartes** : Définition de la taille, de l'espacement, et des effets de survol.
- **Effets de transition** : Chaque carte utilise des transitions CSS pour rendre l'interaction plus fluide.

```css
.card {
    transition: background-position 0.3s ease;
    /* autres styles */
}
```

### JavaScript

Le fichier `script.js` est responsable de la logique qui fait réagir les cartes au mouvement de la souris. Les concepts principaux incluent :

- **Événements de mouvement de la souris** : Utilisation de `mousemove` pour capturer les coordonnées de la souris.
- **Mise à jour de la position de fond** : Calcul et mise à jour de la position d'arrière-plan des cartes en fonction des mouvements de la souris.

```javascript
document.addEventListener('mousemove', (event) => {
    const cards = document.querySelectorAll('.card');
    cards.forEach(card => {
        const rect = card.getBoundingClientRect();
        const x = (event.clientX - rect.left) / rect.width * 100;
        const y = (event.clientY - rect.top) / rect.height * 100;
        card.style.backgroundPosition = `${x}% ${y}%`;
    });
});
```

### Explication des principaux concepts utilisés

- **Événements de souris** : Les événements `mousemove` permettent de détecter la position du curseur en temps réel.
- **Positionnement d'arrière-plan dynamique** : Les cartes utilisent des styles CSS pour ajuster leur arrière-plan en fonction de la position de la souris.
- **Transitions CSS** : Les transitions douces rendent les changements d'arrière-plan plus agréables visuellement.

### Fichiers du projet

- `index.html` : Le fichier HTML principal contenant la structure des cartes.
- `styles.css` : Le fichier de style définissant l'apparence et les animations des cartes.
- `script.js` : Le fichier JavaScript gérant les interactions avec la souris.

### Guide d'utilisation

- **Interagir avec les cartes** : Déplacez la souris sur les cartes pour voir les arrière-plans réagir en temps réel.
- **Effets dynamiques** : Les cartes se déplacent et s'ajustent automatiquement en fonction de la position de la souris, offrant une expérience interactive.

### Fonctionnalités supplémentaires possibles

Pour améliorer ou enrichir ce projet, voici quelques suggestions :

- **Ajout de contenu multimédia** : Intégrer des images ou des vidéos pour enrichir le contenu des cartes.
- **Effets sonores** : Ajouter des sons lors du survol des cartes pour une expérience plus immersive.
- **Optimisation mobile** : Adapter le comportement pour les appareils tactiles, en intégrant des gestes de toucher.

### Contribution

Les contributions sont les bienvenues ! Si vous souhaitez améliorer ce projet ou ajouter de nouvelles fonctionnalités, vous pouvez :

1. Faire un fork de ce dépôt.
2. Créer une nouvelle branche (`git checkout -b feature/nouvelle-fonctionnalite`).
3. Soumettre vos modifications (`git commit -m 'Ajouter nouvelle fonctionnalité'`).
4. Pousser la branche (`git push origin feature/nouvelle-fonctionnalite`).
5. Ouvrir une Pull Request.

### Licence

Ce projet est sous licence MIT. Consultez le [fichier LICENSE](LICENSE) pour plus d'informations.

### Auteur

**Pedro Costa**  
[LinkedIn](https://linkedin.com/in/pedronfcosta/)

### Explication détaillée des sections :

1. **Description et Fonctionnalité principale** : Donne une vue d'ensemble du projet et de son objectif.
2. **Détails du code** : Explique comment le HTML, CSS, et JavaScript fonctionnent ensemble pour créer l'effet d'interaction.
3. **Concepts utilisés** : Décompose les techniques spécifiques utilisées (événements de souris, transitions CSS, etc.).
4. **Fichiers du projet** : Liste des fichiers inclus dans le projet et leur fonction.
5. **Guide d'utilisation** : Explique comment l'utilisateur peut interagir avec les cartes.
6. **Suggestions de fonctionnalités futures** : Propose des idées pour améliorer le projet, telles que l'ajout de contenu multimédia.
7. **Contribution et Licence** : Indique comment les autres peuvent contribuer et sous quelle licence le projet est partagé.
