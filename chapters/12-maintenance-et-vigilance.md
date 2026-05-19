## Reste Vigilant : Entretien et Mises à Jour de Ta Sécurité

La cybersécurité ne s’arrête pas au moment où tu as changé ton mot de passe ou activé l’authentification à deux facteurs. Elle ne se limite pas à la sécurisation de ton téléphone ou à la suppression d’un message suspect. La protection numérique est une **pratique continue**, comme l’entretien d’une voiture ou la routine d’hygiène personnelle. Si tu l’oublies pendant quelques semaines, les risques reviennent — silencieusement, mais sûrement.

Dans ce chapitre final, tu vas apprendre à **transformer la sécurité en une habitude durable**. Tu découvriras comment intégrer des **vérifications régulières**, rester informé des menaces émergentes en Afrique, sensibiliser ton entourage, et t’adapter aux évolutions technologiques — sans te sentir dépassé.

### Installe des routines de sécurité mensuelles

La régularité est la clé. Pour éviter de te retrouver vulnérable sans t’en rendre compte, planifie des **moments dédiés à la vérification de ta sécurité numérique**. Ces vérifications ne doivent pas être longues ni complexes. L’objectif est d’agir **systématiquement**, pas parfaitement.

Voici une **checklist mensuelle** que tu peux personnaliser selon ton usage :

#### ✅ Vérifie l’état de tes mises à jour
- Systèmes d’exploitation (Android, iOS, Windows, Linux)
- Applications (navigateurs, messageries, bancaires, etc.)
- Routeur Wi-Fi (si tu en possèdes un)

Tu peux automatiser certaines mises à jour :
```bash
# Exemple sous Linux : mise à jour automatique des paquets (Ubuntu/Debian)
sudo apt update && sudo apt upgrade -y
```

Sur Android, active les mises à jour automatiques dans **Paramètres > Système > Mises à jour système**. Pour les développeurs utilisant des outils comme Git, Node.js ou VS Code, vérifie régulièrement les versions via :
```bash
npm outdated  # Affiche les paquets Node.js obsolètes
```

#### ✅ Révise tes accès et autorisations
- Supprime les applications inactives sur ton téléphone ou ordinateur.
- Vérifie les accès tiers à ton compte Google ou Facebook :  
  - Google : [https://myaccount.google.com/permissions](https://myaccount.google.com/permissions)  
  - Facebook : Paramètres > Applications et sites web

#### ✅ Audit des sauvegardes
- Confirme que tes données importantes (photos, projets, contacts) sont bien sauvegardées.
- Teste un petit fichier pour vérifier que tu peux le restaurer (surtout si tu utilises un disque dur externe ou un cloud local comme **SahelCloud** ou **AfriDrive**).

#### ✅ Analyse ton réseau Wi-Fi
- Change le mot de passe de ton routeur tous les 3 mois si possible.
- Utilise un nom de réseau (SSID) neutre (pas ton nom, ton prénom, ou ton adresse).
- Désactive le WPS s’il est activé (souvent une faille de sécurité).

### Suis l’actualité des menaces en Afrique

Les cybermenaces évoluent vite, et **les attaques ciblent de plus en plus l’Afrique**. Les arnaques locales sont souvent plus efficaces car elles utilisent des **références culturelles, des noms d’entreprises locales ou des événements d’actualité**.

Par exemple, pendant la période des subventions gouvernementales au Sénégal ou des distributions de kits scolaires au Cameroun, des **faux SMS ou faux sites web** apparaissent pour voler des identifiants.

#### Où t’informer ?
Reste vigilant en suivant des sources fiables :

- **CERT-PA** (Pôle africain de cybersécurité) : publie des alertes sur les campagnes de phishing en cours.
- **ANINF** (Agence nationale de l'informatique du Sénégal) : alertes sur les fraudes numériques locales.
- **Groupes WhatsApp professionnels** : beaucoup de développeurs africains partagent des alertes dans des groupes fermés (ex : "Développeurs Fullstack Afrique").
- **Podcasts et chaînes YouTube** comme *TechAfrik* ou *Digital Afrika* couvrent souvent les sujets de sécurité.

Un exemple récent : en 2023, une vague de **vishing** (phishing par appel téléphonique) a frappé plusieurs pays d’Afrique de l’Ouest. Des fraudeurs appelaient en se faisant passer pour le service client de Wave ou de Moov Money, demandant les codes PIN. En restant informé, tu peux reconnaître ces schémas avant qu’ils ne te touchent.

### Forme ton entourage : la sécurité est collective

Tu n’es protégé que si ton écosystème l’est aussi. Un membre de ta famille qui clique sur un lien malveillant peut compromettre **tout ton réseau familial ou professionnel**.

Pense à **sensibiliser** :
- Tes parents : explique-leur que **personne du service client ne demandera jamais leur mot de passe**.
- Tes collègues : partage des bonnes pratiques dans ton groupe de travail, surtout si vous utilisez des outils comme Google Drive ou Trello.
- Tes enfants : si tu en as, enseigne-leur les bases : pas de partage de photos personnelles, pas d’ajout d’inconnus sur TikTok ou Snapchat.

Tu peux organiser une **"soirée cybersécurité"** chez toi ou dans ton bureau :
- Montre comment reconnaître un faux lien.
- Fais un exercice de création de mot de passe fort ensemble.
- Installe un gestionnaire de mots de passe comme **Bitwarden** (gratuit et open source) sur leurs téléphones.

Un développeur ivoirien nous a partagé son expérience : après avoir formé son équipe de 8 personnes sur les arnaques par email, ils ont **bloqué une tentative de virement frauduleux de 3 millions de FCFA** en reconnaissant un faux courriel du "directeur financier".

### Adapte-toi aux nouvelles technologies

Chaque nouvelle technologie apporte son lot de risques. Quand tu adopts une innovation — qu’il s’agisse de **paiement mobile, de blockchain, ou d’IA générative** — tu dois aussi adapter ta sécurité.

#### Exemple : les portefeuilles mobiles (Wave, Moov Money, Orange Money)
- Active la **confirmation par code SMS** pour chaque transaction.
- Ne partage jamais ton code PIN, même avec un membre de ta famille.
- Surveille les transactions anormales : un retrait de 500 FCFA peut être un test du pirate.

#### Exemple : l’intelligence artificielle
Les développeurs africains utilisent de plus en plus des outils comme **ChatGPT, GitHub Copilot ou Stable Diffusion**. Mais attention :
- **Ne saisis jamais de données sensibles** (codes, mots de passe, numéros de carte) dans une IA.
- Les prompts peuvent être stockés et utilisés pour entraîner les modèles.

Voici un exemple de mauvaise pratique :
```python
# ❌ DANGEREUX : ne jamais faire ça
prompt = """
Voici mon code API pour accéder à la base de données de mon client au Bénin :
API_KEY = 'sk-abc123xyz987'
Explique-moi pourquoi j’ai une erreur 403.
"""
```

C’est comme donner les clés de ton appartement à un inconnu dans la rue.

La bonne approche :
```python
# ✅ Bonne pratique
prompt = """
J’ai une erreur 403 dans mon appel API. Voici la structure de ma requête :
- Méthode : GET
- En-tête : Authorization: Bearer [TOKEN_REDACTED]
- URL : https://api.exemple.com/data
Quelles sont les causes possibles ?
"""
```

### Ressources locales pour continuer à t’informer

Empire du Web t’offre un **kit d’accompagnement post-cours** pour rester protégé :

1. **Checklist mensuelle téléchargeable** (format PDF et Excel) : à imprimer et coller sur ton bureau.
2. **Annuaire des CERT nationaux en Afrique francophone** :
   - Sénégal : ANINF
   - Côte d’Ivoire : ARCI
   - Mali : CNAC
   - Togo : Agence de sécurité des systèmes d’information
3. **Chaînes Telegram recommandées** :
   - @CyberSecAfrique (alertes en temps réel)
   - @DevAfrique_Sec (pour développeurs)
4. **Simulateur de phishing** : un outil en ligne pour t’entraîner chaque mois.

Tu peux aussi rejoindre le **Club Sécurité Empire du Web**, un espace privé où des experts répondent à tes questions chaque semaine.

### Points clés

- **La cybersécurité est une habitude**, pas une tâche ponctuelle. Intègre-la à ta routine comme tu le fais pour ton hygiène ou ton alimentation.
- **Planifie des vérifications mensuelles** : mises à jour, sauvegardes, accès tiers, Wi-Fi.
- **Reste informé des menaces locales** en Afrique via des sources comme les CERT nationaux, les groupes professionnels et les médias tech.
- **Protège ton écosystème** : forme ta famille, tes collègues et tes proches. La sécurité est collective.
- **Adapte ta protection aux nouvelles technologies** : mobile money, IA, cloud. Chaque outil nouveau demande une vigilance nouvelle.
- **Utilise les ressources fournies** : checklist, annuaires, simulateurs, et communautés pour avancer sereinement.

Tu as maintenant toutes les clés en main. Ce n’est pas la fin, c’est le **début d’une nouvelle posture numérique**. Chaque clic, chaque mot de passe, chaque mise à jour compte. Et chaque geste de vigilance te rapproche d’une vie numérique plus libre, plus sûre, et plus puissante. 👨‍💻🛡️