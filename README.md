# edoSeasonsTracker

<img src="icon-192.png" alt="杏" width="96" align="right">

Application web (PWA) de consultation de la **saisonnalité en Suisse** des **fruits, légumes, champignons, oléagineux** et de produits courants (**lait, œufs, miel, huile d'olive**) : pour chaque produit, sa **période** (récolte vs disponibilité), son **mode de conservation**, l'**origine recommandée** et son **empreinte transport**. Installable sur iPhone et Android, fonctionne **hors-ligne**.

Mono-fichier `index.html` (aucune dépendance à installer), à l'image des autres applications `edo*`.

## Fonctionnalités

- **En ce moment** : produits du mois en Suisse, navigation mensuelle, recherche, filtres par catégorie.
- **Au pic / Bientôt / Dernière chance** : badges en coin de tuile pour repérer ce qui démarre, culmine ou se termine.
- **Transport** : Local · frais / Local · conservation / Europe proche / lointain · avion.
- **Frais local uniquement** : ne montre que la culture en extérieur du mois.
- **Calendrier** glissant sur 6 mois à partir du mois en cours, noms cliquables, tri alphabétique.
- **Fiche produit** : récolte vs disponibilité (+ sources), conservation, origine, variétés, sécurité (champignons), liens Wikipédia / Google Images, commentaires.
- **Multilingue FR / DE / IT** intégral (interface, noms et fiches — traduction IA, langue de référence : français, avec confirmation avant activation).
- **Thème clair / sombre / système** et **mode daltonien** (motifs + lettres).
- **Favoris** et **commentaires** locaux, avec **export / import** JSON pour sauvegarde.

## Catégories de saison

| Repère | Lettre | Signification |
|--------|--------|---------------|
| Abricot | E | De saison, culture en extérieur (frais local) |
| Vert | S | Culture sous serre (Suisse) |
| Abricot pâle | C | Conservation / disponible |
| Gris | — | Hors saison |

Données **indicatives**, recoupées avec les calendriers saisonniers suisses (OFAG, gemüse.ch, Swissmilk, WWF, Bio Suisse). Les dates varient selon la météo, l'altitude et les variétés.

## ⚠️ Champignons

Plusieurs champignons sauvages ressemblent à des espèces vénéneuses. Ne consommez que des champignons identifiés avec certitude ; en cas de doute, faites contrôler votre récolte par un contrôleur officiel (VAPKO). La morille est toxique crue et doit être bien cuite.

## Lancer en local

```bash
python3 -m http.server 8080   # puis http://localhost:8080
```

## Déployer (GitHub Pages)

Pousser ce dossier, puis *Settings → Pages → Deploy from a branch* (`/root`). L'app est servie en HTTPS et devient installable.

## Fichiers

```
index.html               Application (HTML/CSS/JS, autonome)
manifest.webmanifest     Métadonnées PWA
sw.js                    Service worker (cache hors-ligne)
icon-180/192/512*.png    Icônes
favicon.png              Favicon
```

## Limites

Pas de prix (aucune API publique, requêtes inter-sites bloquées). Application de consultation ; informations indicatives, ne remplaçant pas l'avis d'un spécialiste (champignons notamment).

---

Icône : 杏 (kanji de l'abricot). Traductions DE/IT réalisées par IA, langue de référence : français.
