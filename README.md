voici le lien public pour continuer à développer le code source c'est cela que j'ai utilisé pour créer ce code source donc en continuant la conversation vous pourrez faire ce que vous voulez 

https://chat.deepseek.com/share/r4ofyz48ylngl6zlpu

# 📸 Portrait by Voanh Agnès – AI Pic 2 Bulk Pic

**Générez une multitude de portraits stylisés à partir d’une seule image, en utilisant l’API Agnes AI et une interface web tout‑en‑un.**

Ce dépôt regroupe plusieurs **laboratoires de styles** (labs) indépendants, chacun étant une application HTML autonome qui permet de décliner un portrait source selon des dizaines de presets visuels. Le tout fonctionne directement dans le navigateur, sans installation serveur, et gère automatiquement les clés API, le débit (RPM) et les erreurs.

---

## ✨ Fonctionnalités principales

- **Analyse unique** : une seule image de référence (visage, tenue, décor) est analysée et verrouillée pour toutes les générations suivantes.
- **Génération style par style** : chaque onglet de style possède son propre bouton de génération ; vous lancez les styles un par un, à votre rythme.
- **39 presets + Custom** : de nombreux styles visuels majeurs sont couverts (cinéma, illustration, rétro, etc.) et vous pouvez créer vos propres onglets personnalisés.
- **Gestion multi‑clés API** : ajoutez plusieurs clés Agnes AI ; elles tournent en parallèle avec un paceur RPM automatique.
- **Paceur RPM intelligent** : ~15 requêtes/min par clé, rotation automatique, cooldown sur les erreurs 429, et **retry infini** en cas d’échec (plus de blocage).
- **Interface sombre et réactive** : pensée pour une utilisation mobile et desktop.
- **Console intégrée** : suivi en temps réel des opérations et des erreurs.

---

## 📂 Labs inclus dans ce dépôt

Chaque fichier HTML est un **lab indépendant** avec sa propre interface et ses propres presets :

| Fichier | Nom du lab | Description |
|---------|------------|-------------|
| `deepseek_html_20261016_35be39.html` | **Visual.Studio — Multi‑Style Lab v2** | Le lab principal avec 39 presets + onglet Custom. |
| `deepseek_html_20261016_4d5942.html` | **Visual.Studio — Monetize Lab v3.1** | Variante orientée monétisation (styles supplémentaires). |
| `deepseek_html_20261016_500ec2.html` | **Visual.Studio — Consciousness Lab** | Exploration de styles abstraits/conscients. |
| `deepseek_html_20261016_8a5ad9.html` | **Visual.Studio — Wes Anderson Lab** | Presets inspirés de l’esthétique de Wes Anderson. |
| `deepseek_html_20261016_f31b63.html` | **Visual.Studio — Director Lab** | Styles de mise en scène cinématographique. |

> **Note** : tous les labs partagent la même logique de base (analyse d’image, gestion des clés, paceur RPM) mais diffèrent par leurs jeux de presets et leur habillage graphique.

---

## 🚀 Démarrage rapide

### Prérequis

- Un navigateur moderne (Chrome, Firefox, Edge, Safari).
- Une **clé API Agnes AI** valide (obtenez‑la sur [agnes-ai.com](https://www.agnes-ai.com/)).

### Installation

1. Clonez le dépôt :
   ```bash
   git clone https://github.com/laurentvoanhofficiel-jpg/Portrait-by-voanh-agnes-ai-pic-2-bulk-pic.git
   ```
2. Ouvrez l’un des fichiers HTML dans votre navigateur (par exemple `deepseek_html_20261016_35be39.html`).

Aucune compilation, aucun serveur : tout fonctionne côté client.

---

## 🖥️ Utilisation

1. **Ajoutez vos clés API**  
   Dans la section « Clés API Agnes », collez une ou plusieurs clés puis cliquez sur **Valider et enregistrer**.

2. **Chargez une image de personnage**  
   Cliquez sur la zone d’image, choisissez une photo (visage, tenue, décor).  
   Le bouton **Analyser l’image** permet de verrouiller les caractéristiques pour toutes les générations.

3. **Lancez les styles**  
   Chaque onglet de style possède son propre bouton **Générer**.  
   Vous pouvez générer les styles un par un, ou tous à la suite si vous le souhaitez.

4. **Personnalisez avec l’onglet ✏️ Custom**  
   Créez vos propres onglets en définissant un nom et un prompt.  
   Ces onglets se comportent comme les presets natifs.

5. **Suivez la console**  
   La console en bas de page affiche l’état des requêtes, les erreurs éventuelles et les retries.

---

## ⚙️ Configuration avancée

### Paceur RPM

Le paceur est réglé par défaut à **~15 requêtes/minute par clé**.  
Il est possible d’ajuster ce paramètre dans le code (recherchez `RPM` ou `paceur` dans le fichier HTML) :

```javascript
const RPM_LIMIT = 15; // requêtes par minute et par clé
```

### Gestion des erreurs

- **429 (Too Many Requests)** : cooldown automatique avant de réessayer.
- **Erreurs réseau** : retry infini avec backoff exponentiel.
- **Clé invalide** : message dans la console, la clé est ignorée.

### Ajout de clés multiples

Vous pouvez enregistrer plusieurs clés ; elles seront utilisées en rotation pour répartir la charge.

---

## 🎨 Presets de styles

Chaque lab propose un ensemble de presets. Voici un aperçu des catégories couvertes :

- **Cinéma** : Director Lab, Wes Anderson Lab, etc.
- **Illustration** : aquarelle, crayon, digital painting.
- **Rétro / Vintage** : polaroid, film grain, années 80.
- **Abstrait / Conceptuel** : Consciousness Lab.
- **Monétisation** : Monetize Lab (styles optimisés pour la vente).

Vous pouvez consulter la liste complète directement dans l’interface de chaque lab.

---

## 🤝 Contribution

Les contributions sont les bienvenues !  
Si vous souhaitez ajouter un nouveau lab, améliorer l’UI ou corriger un bug :

1. Forkez le dépôt.
2. Créez une branche (`git checkout -b feature/nouveau-lab`).
3. Commitez vos modifications.
4. Ouvrez une pull request.

---

## 📄 Licence

Ce projet n’a pas encore de licence explicite.  
Pour toute utilisation commerciale, veuillez contacter l’auteur.

---

## 🙏 Remerciements

- **Laurent Voanh** pour la conception et le développement.
- **Agnes AI** pour l’API de génération d’images.
- **DeepSeek** pour l’assistance au développement (conversation source : [https://chat.deepseek.com/share/r4ofyz48ylngl6zlpu](https://chat.deepseek.com/share/r4ofyz48ylngl6zlpu)).

---

**Bon portrait !** 🎨
