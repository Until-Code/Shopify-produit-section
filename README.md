# Section produit personnalisée – Shopify (thème Dawn)

Intégration d'une **section custom** sur le thème **Dawn** pour afficher un produit avec ses **variantes** et un **design interactif (hover)**.

- **Section créée :** `sections/hover.liquid` → affichage produit + variantes + accordéons  
- **Responsive :** Desktop & Mobile  
- **Éléments personnalisables :** couleurs, textes, variantes, boutons, accordéons  
- **Démo en ligne :** [Voir le produit](https://z1znwa-06.myshopify.com/products/gellule)

---

## 🚀 Installation

### 1) Cloner le projet

```bash
git clone https://github.com/Until-Code/Shopify-produit-section.git
cd Shopify-produit-section
```

### 2) Tester en local

Vérifiez le rendu complet (assets, templates, sections) avec Shopify CLI :

```bash
shopify theme dev --store votreboutique.myshopify.com
```

> Astuce : contrôlez que tous les fichiers sous `assets/` et `config/` sont bien présents pour éviter les erreurs d’import.

### 3) Déployer sur votre boutique

**Créer un nouveau thème brouillon** (aucun écrasement) :

```bash
shopify theme push --unpublished
```

**OU** mettre à jour un thème **spécifique** (remplace ses fichiers) :

```bash
shopify theme list           # pour récupérer les Theme ID
shopify theme push THEME_ID  # push vers un thème de test
```

**Publier directement sur le thème actif** (⚠️ prudence) :

```bash
shopify theme push --live
```

---

## 🧩 Utilisation dans l’éditeur

- La section apparaît sous le nom **« Hover »** dans l’éditeur de thème.  
- Chemin de fichier : `sections/hover.liquid`.

---

## ⚙️ Options de personnalisation

- **Images** : nombres d'images, effet hover pour la partie gallerie et main image différent ou similaire(héritage du main image.  
- **Couleurs** : titres, sous-titres, étiquettes de variantes, boutons.  
- **Textes** : titres/CTA/labels.  
- **Variantes** : sélection et affichage dynamique.  
- **Boutons** : état normal/hover, libellés.  
- **Accordéons** : contenu descriptif, caractéristiques, FAQ.

---

## ✅ Prérequis

- **Shopify CLI** connecté à votre boutique (`shopify login`).  
- Accès à une boutique Shopify (plan actif) avec thème **Dawn** (version récente recommandée).

---

## 🧪 Workflow conseillé

1. `shopify theme pull live` *(optionnel)* pour récupérer la base du thème actif.  
2. Dev local avec `shopify theme dev`.  
3. `shopify theme push --unpublished` pour créer un thème de test.  
4. Vérifications & QA dans l’admin (aperçu).  
5. Publication : `shopify theme push THEME_ID --live` une fois validé.

---

## ❓FAQ rapide

- **`theme dev` modifie le site en ligne ?**  
  Non. C’est un **aperçu local** avec hot reload, rien n’est publié tant que vous ne faites pas `theme push`.

- **Puis-je éviter d’écraser un thème existant ?**  
  Oui, utilisez `--unpublished` pour créer un **nouveau thème**.

- **Comment être sûr du bon Theme ID ?**  
  `shopify theme list` affiche tous les thèmes avec leurs IDs.

---

👤 **Auteur** : [Djemal Sardarian](https://github.com/Until-Code)  
📅 **Date** : Septembre 2025
