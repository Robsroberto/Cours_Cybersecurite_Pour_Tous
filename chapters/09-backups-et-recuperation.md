## Sauvegarde Tes Données : Ne Perds Jamais l’Essentiel

Tu as passé des heures à créer un document important, à monter une vidéo pour ton business en ligne, ou à collecter des données clients pour ton application mobile. Un jour, ton téléphone tombe dans l’eau. Ton ordinateur plante sans prévenir. Un virus crypte tous tes fichiers. Et d’un coup, tout disparaît. Pas de sauvegarde. Rien à récupérer. C’est une situation que des milliers d’Africains vivent chaque année — souvent sans même s’en rendre compte avant qu’il ne soit trop tard.

La vérité est simple : **tout appareil peut tomber en panne, être volé, ou infecté**. Mais ce n’est pas la fin du monde — **si tu as une sauvegarde**.

### Pourquoi la sauvegarde est ton filet de sécurité

Imagine que tu construis une maison. Tu installes des serrures, des grilles, mais tu n’as pas d’extincteur. Si un incendie se déclare, tout peut brûler. La sauvegarde, c’est ton extincteur numérique. Elle ne t’empêche pas l’attaque, mais elle te permet de tout reconstruire.

En Afrique, où l’accès à Internet peut être instable, les coupures d’électricité fréquentes, et les équipements parfois limités, **la sauvegarde régulière est encore plus cruciale**. Tu ne peux pas toujours compter sur le cloud si la connexion est coupée pendant trois jours. C’est pourquoi tu dois combiner plusieurs méthodes.

### Sauvegarde locale : contrôle total, pas besoin d’internet

La sauvegarde locale consiste à copier tes fichiers sur un appareil physique que tu possèdes : disque dur externe, clé USB, ou carte mémoire.

#### Avantages
- Pas besoin d’internet
- Rapide à configurer
- Moins coûteux à long terme
- Contrôle total sur tes données

#### Cas concret : Awa, développeuse freelance au Sénégal

Awa travaille sur des projets web pour des clients de la Côte d’Ivoire et du Bénin. Chaque soir, avant de dormir, elle branche son disque dur externe de 1 To et copie ses dossiers de travail : codes sources, designs Figma, contrats. Elle garde le disque dans une boîte métallique, à l’abri de l’humidité. Quand son ordinateur a planté après une surtension, elle a récupéré tout son travail en 20 minutes.

#### Bonnes pratiques
- Utilise un disque dur externe de qualité (marques comme WD ou Seagate)
- Évite les clés USB bon marché — elles tombent en panne vite
- Étiquette ton disque : “Sauvegarde Travail – Mai 2025”
- Stocke-le dans un endroit sûr, à l’écart du feu, de l’eau et des enfants

```bash
# Exemple de script simple sous Linux/Mac pour automatiser une sauvegarde locale
rsync -av /home/awa/projets/ /media/awa/disque_sauvegarde/projets/
```

Ce script copie tous les fichiers du dossier `projets` vers le disque de sauvegarde. Tu peux le programmer avec `cron` pour qu’il s’exécute chaque soir à 22h.

### Sauvegarde cloud : synchronisation automatique, accessible partout

Le cloud, c’est le stockage en ligne. Tu envoies tes fichiers sur des serveurs distants, accessibles depuis n’importe quel appareil avec internet.

#### Services populaires en Afrique
- **Google Drive** : 15 Go gratuits, intégré à Gmail et Google Docs
- **Mega** : 20 Go gratuits, chiffrement de bout en bout
- **Dropbox** : 2 Go gratuits, bon pour les petits fichiers

#### Cas concret : Ibrahim, formateur à Abidjan

Ibrahim anime des formations sur le développement mobile. Il utilise Google Drive pour stocker ses cours, ses présentations et les exercices des élèves. Même quand il change d’ordinateur, il retrouve tout instantanément. Quand son téléphone a été volé dans un taxi, il a récupéré ses fichiers depuis un cybercafé en moins de 10 minutes.

#### Avantages
- Accessible de n’importe où
- Synchronisation automatique
- Protection contre les catastrophes physiques (incendie, inondation)

#### Limites en contexte africain
- Nécessite une connexion internet fiable
- Les forfaits data peuvent être chers
- Les vitesses de téléchargement sont parfois lentes

#### Solution : sauvegarde cloud intelligente

Tu n’as pas besoin de tout sauvegarder en ligne. Priorise :
- Les fichiers en cours de travail
- Les documents officiels (carte d’identité, diplômes, contrats)
- Les contacts et photos importantes

Utilise les fonctionnalités hors ligne de Google Drive ou OneDrive : elles permettent de marquer certains fichiers comme "toujours disponibles", même sans internet.

```javascript
// Exemple : script Node.js pour uploader un fichier vers Google Drive (via API)
const {google} = require('googleapis');
const fs = require('fs');

const auth = new google.auth.GoogleAuth({
  keyFile: 'credentials.json',
  scopes: 'https://www.googleapis.com/auth/drive'
});

async function uploadFile() {
  const drive = google.drive({version: 'v3', auth});
  const fileMetadata = {name: 'rapport_mensuel.pdf'};
  const media = {mimeType: 'application/pdf', body: fs.createReadStream('rapport_mensuel.pdf')};
  
  const res = await drive.files.create({resource: fileMetadata, media});
  console.log('Fichier sauvegardé sur Google Drive :', res.data.id);
}
```

Ce type d’automatisation est utile si tu gères un site web ou une application qui génère des rapports quotidiennement.

### La règle des 3-2-1 : ta stratégie infaillible

Pour être vraiment protégé, adopte la **règle des 3-2-1** :
- **3** copies de tes données (originale + 2 sauvegardes)
- Sur **2** supports physiques différents (ex : ordinateur + disque dur)
- Dont **1** stockée hors site (ex : cloud ou chez un proche)

#### Exemple concret
Tu es entrepreneur au Cameroun et tu gères une boutique en ligne. Voici ta stratégie :
1. **Copie 1** : sur ton ordinateur (fichiers produits, commandes, clients)
2. **Copie 2** : sur un disque dur externe (mis à jour chaque semaine)
3. **Copie 3** : sur Mega (fichiers critiques, synchronisés chaque jour)

Si ton bureau brûle, tu perds les deux premières copies — mais tu as toujours la troisième.

### Calendrier de sauvegarde : simple et réaliste

Tu n’as pas besoin de sauvegarder 10 fois par jour. Ce qui compte, c’est la **régularité**.

Voici un calendrier adapté à la réalité africaine :

| Type de fichier         | Fréquence       | Support         |
|-------------------------|-----------------|-----------------|
| Projets en cours        | Quotidien       | Cloud + USB     |
| Documents officiels     | Mensuel         | Disque dur      |
| Photos et vidéos        | Hebdomadaire    | Google Drive    |
| Bases de données        | Après chaque mise à jour | Cloud chiffré |

Tu peux t’aider d’un tableau en papier sur ton mur, ou d’un rappel dans ton téléphone.

### Teste ta sauvegarde : ne découvre pas trop tard qu’elle ne fonctionne pas

Beaucoup de gens pensent avoir une sauvegarde… jusqu’au jour où ils en ont besoin. Et là, mauvaise surprise : le fichier est corrompu, le disque ne répond plus, ou le cloud n’a pas synchronisé depuis un mois.

#### Exercice : simulation de perte

1. Choisis un fichier important (un CV, une facture, un projet).
2. Supprime-le de ton ordinateur.
3. Essaye de le récupérer depuis ta sauvegarde (disque dur ou cloud).
4. Note le temps que ça prend, les difficultés rencontrées.

Si tu n’y arrives pas en moins de 15 minutes, **ta sauvegarde n’est pas fiable**. Reprends ton système.

### Sauvegarde mobile : pense aussi à ton téléphone

Ton téléphone contient souvent plus d’informations personnelles et professionnelles que ton ordinateur : contacts, photos, messages, applications bancaires.

#### Solutions
- **Android** : active la sauvegarde automatique dans Google (Paramètres > Comptes > Sauvegarde)
- **iPhone** : utilise iCloud ou sauvegarde via iTunes sur un ordinateur
- **Apps tierces** : Syncthing (gratuit, open source, pas besoin de cloud)

#### Bonne pratique
Chaque dimanche soir, branche ton téléphone à ton ordinateur et copie manuellement les dossiers DCIM (photos), Téléchargements, et Documents.

---

## Points clés

- **Tout appareil peut tomber en panne** — la sauvegarde est ta meilleure assurance.
- **Combines sauvegarde locale (disque dur, clé USB) et cloud (Google Drive, Mega)** pour couvrir tous les scénarios.
- En contexte africain, privilégie les solutions **peu gourmandes en data** et adapte ta fréquence de sauvegarde à ta connectivité.
- Applique la **règle des 3-2-1** : 3 copies, 2 supports, 1 hors site.
- **Automatise** quand c’est possible (scripts, synchronisation), mais reste vigilant.
- **Teste régulièrement** ta sauvegarde : récupérer un fichier doit être rapide et simple.
- Ton téléphone aussi a besoin d’une stratégie de sauvegarde — ne l’oublie pas.

Chez Empire du Web, nous croyons que ta sécurité numérique ne dépend pas de ton budget, mais de tes habitudes. Une sauvegarde bien faite, même simple, vaut mille pare-feu. Mets-la en place dès ce soir.