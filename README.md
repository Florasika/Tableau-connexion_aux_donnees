# 📊 Jour 1 / 10 — Tableau : Connexion aux données & premiers graphiques

> **Série : 10 Days of Tableau** · Jour 1/10  
> Concepts : Connexion CSV · Dimensions vs Mesures · Bar Chart · Line Chart · Dashboard

---

## 📁 Fichiers du projet

```
day-01-premiers-pas/
│
├── ventes_tableau.csv    ← 188 lignes de données (5 produits, 5 vendeurs, 12 mois)
└── README.md
```

---

## 🚀 Prérequis — Télécharger Tableau

**Tableau Public (gratuit) :**
```
https://public.tableau.com/app/discover
→ Créer un compte gratuit → Télécharger Tableau Desktop Public
```
**Tableau Desktop (payant, 14 jours d'essai) :**
```
https://www.tableau.com/fr-fr/products/trial
```
Ce guide fonctionne avec les deux versions.

---

## 📊 Les données — `ventes_tableau.csv`

| Colonne | Type Tableau | Description |
|---------|-------------|-------------|
| `Date` | Dimension (date) | Date de la vente |
| `Mois` | Dimension (texte) | Format YYYY-MM |
| `Trimestre` | Dimension (texte) | T1 · T2 · T3 · T4 |
| `Vendeur` | Dimension (texte) | 5 vendeurs |
| `Région` | Dimension (texte) | 5 régions françaises |
| `Produit` | Dimension (texte) | 5 produits |
| `Catégorie` | Dimension (texte) | Informatique · Mobile · Audio · Wearable |
| `Quantité` | Mesure (#) | Unités vendues |
| `Prix Unitaire` | Mesure (#) | Prix en euros |
| `Montant` | Mesure (#) | Quantité × Prix Unitaire |
| `Objectif` | Mesure (#) | Objectif de vente |

---

## 🔑 Concept fondamental — Dimensions vs Mesures

| | Dimensions (bleu) | Mesures (vert) |
|---|---|---|
| **Rôle** | Segmentent / catégorisent | Se calculent |
| **Exemples** | Produit, Région, Vendeur, Date | Montant, Quantité, Prix |
| **Agrégation** | Aucune | SUM, AVG, COUNT, MIN, MAX |
| **Position** | Lignes, Colonnes, Couleur, Filtre | Axe Y, Taille, Couleur |

**Règle simple :** peux-tu additionner cette valeur de manière significative ? Oui → c'est une mesure.

---

## 🚀 Étape 1 — Connecter les données

```
1. Ouvrir Tableau
2. Fichier → Se connecter à des données → Fichier texte
3. Sélectionner ventes_tableau.csv
4. Vérifier les types de colonnes :
   - Date → icône calendrier 📅
   - Texte → icône Abc
   - Nombres → icône #
5. Cliquer "Feuille 1" en bas
```
Le panneau de gauche affiche maintenant toutes tes colonnes en **Dimensions** (bleu, haut) et **Mesures** (vert, bas).

---

## 🚀 Étape 2 — Bar Chart : CA par Produit

```
1. Sur la Feuille 1 :
   → Glisser "Produit" sur l'étagère Lignes
   → Glisser "Montant" sur l'étagère Colonnes
   
2. Tableau crée automatiquement SUM(Montant) par Produit

3. Trier :
   → Cliquer le bouton de tri dans la barre d'outils (icône barres ↓)
   → Tri décroissant

4. Ajouter de la couleur :
   → Glisser "Catégorie" sur la carte Couleur (panneau Repères)
   → Les barres se colorient par catégorie

5. Renommer la feuille :
   → Double-clic sur l'onglet "Feuille 1" → "CA par Produit"
```

---

## 🚀 Étape 3 — Line Chart : Évolution mensuelle

```
1. Nouvelle feuille :
   → Cliquer l'icône + en bas à droite des onglets

2. Construire la courbe :
   → Glisser "Mois" sur l'étagère Colonnes
   → Glisser "Montant" sur l'étagère Lignes
   → Tableau choisit automatiquement "Lignes" comme type

3. Ajouter les vendeurs :
   → Glisser "Vendeur" sur la carte Couleur
   → 5 courbes apparaissent, une par vendeur

4. Activer les infobulles :
   → Survoler la courbe → les détails apparaissent automatiquement

5. Renommer : "Évolution mensuelle"
```

---

## 🚀 Étape 4 — Assembler le Dashboard

```
1. Nouveau dashboard :
   → Cliquer l'icône dashboard en bas (rectangle à 4 cases)

2. Définir la taille :
   → Onglet "Dashboard" → Taille → Personnalisée → 1200 × 800 px

3. Ajouter les feuilles :
   → Panneau gauche → glisser "CA par Produit" sur le canvas
   → Glisser "Évolution mensuelle" à côté ou en dessous

4. Activer le filtre croisé :
   → Cliquer sur le graphique "CA par Produit"
   → Icône entonnoir 🔽 (coin supérieur droit) → "Utiliser comme filtre"
   → Cliquer une barre → la courbe se filtre automatiquement

5. Sauvegarder :
   → Tableau Public : Fichier → Enregistrer sur Tableau Public
   → Tableau Desktop : Ctrl+S → format .twbx
```

---

## 💡 Raccourcis Tableau utiles

| Action | Raccourci |
|--------|-----------|
| Actualiser les données | F5 |
| Annuler | Ctrl+Z |
| Nouvelle feuille | Ctrl+M |
| Basculer Lignes/Colonnes | Ctrl+W |
| Présentation plein écran | F7 |
| Inverser le tri | Cliquer l'axe |

---


---

⭐ **Si ce projet t'aide, mets une étoile !**
