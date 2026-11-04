# Enquête IA et métiers (UIDT) : mise en ligne sur GitHub

Principe : la page (index.html) est hébergée sur GitHub Pages ; les réponses sont envoyées dans une feuille Google Sheets via le script Code.gs. Tout est gratuit et indépendant de Claude.

## Étape 1 : la feuille et le script Google (10 min)
1. Va sur https://sheets.google.com et crée une feuille vide nommée « Enquête IA ».
2. Menu **Extensions > Apps Script**. Supprime le code existant, colle le contenu de **Code.gs**, clique sur l’icône disquette (Enregistrer).
3. Clique sur **Déployer > Nouveau déploiement**. Type : **Application Web**.
   - Exécuter en tant que : **Moi**
   - Qui a accès : **Tout le monde**
4. Clique sur **Déployer**, accepte les autorisations (« Paramètres avancés > Accéder à … » si Google avertit), puis **copie l’URL** qui se termine par `/exec`.

## Étape 2 : brancher la page
Ouvre **index.html** dans un éditeur de texte (ou directement sur GitHub avec l’icône crayon) et remplace `COLLER_ICI_L_URL_DU_SCRIPT` par l’URL copiée, en gardant les guillemets.

## Étape 3 : GitHub Pages
1. Crée un compte sur https://github.com puis un dépôt **public** nommé par exemple `enquete-ia` (**New repository**).
2. **Add file > Upload files** : envoie `index.html` (tu peux ajouter aussi Code.gs et LISEZMOI.md) puis **Commit changes**.
3. **Settings > Pages** : Source = **Deploy from a branch**, Branch = **main** / **(root)**, **Save**.
4. Après 1 à 2 minutes, le site est à : `https://TON-PSEUDO.github.io/enquete-ia/`

## Les liens des enquêteurs
- Mohamed : `https://TON-PSEUDO.github.io/enquete-ia/#mohamed`
- Ndeye Amy : `https://TON-PSEUDO.github.io/enquete-ia/#amy`

Le nom de l’enquêteur s’affiche et est enregistré avec chaque réponse. Les réponses des deux arrivent dans la même feuille.

## Récupérer et étudier les données
Dans Google Sheets : **Fichier > Télécharger > Excel (.xlsx)** ou **CSV**. Une ligne par réponse ; les choix multiples sont séparés par « | ».

## Bon à savoir
- Les personnes enquêtées n’ont pas besoin de compte : elles ouvrent le lien et répondent.
- Sans connexion, la réponse est gardée sur l’appareil et renvoyée automatiquement plus tard.
- Garde la feuille Google **privée** (ne la partage pas) : elle contient les noms et téléphones.
- Si tu modifies Code.gs, refais **Déployer > Gérer les déploiements > Modifier > Nouvelle version**.
- Pour changer un nom d’enquêteur ou ajouter un enquêteur, modifie la ligne `var E={...}` dans index.html.
