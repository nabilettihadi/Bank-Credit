# Bank-Credit

# Simulation de Crédit Bancaire

Ce projet fournit une interface dynamique de simulation de crédit bancaire où l'utilisateur peut ajuster le montant du prêt, la durée et les mensualités de manière interactive. Le système garantit que ces champs sont interdépendants, c'est-à-dire que toute modification d'un champ met à jour automatiquement les autres en fonction d'un taux d'intérêt fixe.

## Fonctionnalités

- **Simulation dynamique de prêt** : Ajustez le montant du prêt, la durée ou les mensualités, et le système met à jour automatiquement les autres valeurs.
- **Sliders interactifs** : Utilisation de curseurs pour modifier les paramètres du prêt.
- **Formulaire multi-étapes** : Collecte des informations sur le prêt, les coordonnées et les informations personnelles sur plusieurs étapes.
- **Design réactif** : L'interface s'adapte à différentes tailles d'écran, offrant une expérience utilisateur fluide sur tous les appareils.

## Structure du projet

- **index.html** : Structure de la page avec les trois étapes du formulaire.
- **styles.scss** : Feuille de style écrite en Sass pour rendre le formulaire esthétique et responsive.
- **script.js** : Contient la logique pour la mise à jour dynamique des calculs du prêt et la validation des formulaires.

## Formules

Le calcul des mensualités est réalisé à l’aide de la formule suivante :

\[
\text{Mensualités} = \frac{\text{Montant du prêt} \times \text{Taux mensuel}}{1 - (1 + \text{Taux mensuel})^{-\text{Durée}}}
\]

Où :

- **Montant du prêt** est le capital emprunté.
- **Taux mensuel** est calculé en divisant le taux d'intérêt annuel par 12.
- **Durée** est le nombre total de mois.

Le montant du prêt peut également être calculé à partir de la mensualité et de la durée :

\[
\text{Montant du prêt} = \frac{\text{Mensualité} \times (1 - (1 + \text{Taux mensuel})^{-\text{Durée}})}{\text{Taux mensuel}}
\]

Dans ce projet, le taux d'intérêt est fixé à 4% par an, mais il peut être ajusté dans le fichier `script.js`.

## Installation

1. Cloner le dépôt :

   ```bash
   git clone https://github.com/nabilettihadi/Bank-Credit.git
   ```

2. Accédez au dossier du projet :

   ```bash
   cd Bank-Credit
   ```

3. Ouvrez `index.html` dans votre navigateur pour afficher le projet.

## Utilisation

1. **Étape 1** : Utilisez les curseurs pour ajuster le montant du prêt, la durée et les mensualités.
2. **Étape 2** : Fournissez vos informations personnelles telles que l'email et le numéro de téléphone.
3. **Étape 3** : Entrez vos informations personnelles supplémentaires et soumettez le formulaire.

### Mise à jour des champs

- **Montant du prêt et Durée** : Modifiez ces champs pour voir les mensualités mises à jour automatiquement.
- **Mensualités** : Modifiez les mensualités pour voir le montant du prêt se mettre à jour.
- Le système assure la cohérence entre les trois champs.

## Dépendances

Ce projet ne nécessite aucune bibliothèque externe ou dépendance. Il est entièrement construit avec JavaScript, HTML et CSS natifs.

## Personnalisation

- **Taux d'intérêt** : Vous pouvez ajuster le taux d'intérêt en modifiant la variable `tauxInteret` dans `script.js`.
- **Validation du formulaire** : Des validations supplémentaires peuvent être ajoutées dans les fonctions `validateStep1` et `validateStep2` dans `script.js` selon vos besoins.

## Améliorations futures

- Support pour des taux d'intérêt variables.
- Ajout d'une validation plus avancée des formulaires et des messages d'erreur détaillés.
- Amélioration des fonctionnalités de gestion de crédit en cours et des conditions d'acceptation.

## Contribution

N'hésitez pas à forker ce dépôt et à soumettre des pull requests. Nous accueillons les contributions et suggestions pour améliorer ce projet.


