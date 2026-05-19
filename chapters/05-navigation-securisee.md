## Navigue en Toute Sécurité : Internet, Wi-Fi et Réseaux Publics

Internet est devenu une extension de notre quotidien. Que tu sois entrepreneur, freelance, étudiant ou employé, tu y passes plusieurs heures par jour : recherche d’informations, envoi d’emails, paiement de factures, gestion de comptes bancaires, ou encore communication avec des clients. Mais chaque clic, chaque connexion, chaque téléchargement peut exposer tes données si tu n’es pas vigilant.

En Afrique, l’utilisation d’Internet sur des réseaux publics est fréquente. Dans les cybercafés de Dakar, les salles d’attente des aéroports à Abidjan, ou les espaces de coworking à Lagos, les Wi-Fi gratuits sont une bouée de sauvetage face au coût élevé des forfaits mobiles. Pourtant, ces connexions pratiques sont aussi des portes ouvertes aux cybercriminels.

Ce chapitre t’apprend à identifier les risques cachés derrière une simple connexion Wi-Fi, à reconnaître les sites sûrs, et à te protéger efficacement — surtout dans les environnements à haut risque comme les lieux publics.

### Comprendre les risques des réseaux Wi-Fi publics

Un réseau Wi-Fi public, c’est comme une conversation dans un marché bondé : tout le monde peut t’entendre. Ces réseaux sont rarement sécurisés. Ils ne demandent souvent aucun mot de passe, ou utilisent un mot de passe unique pour tous les utilisateurs. Cela signifie que n’importe qui connecté au même réseau peut surveiller ton activité — technique appelée **écoute passive** ou *sniffing*.

Imagine que tu es dans un café à Bamako et que tu consultes ta messagerie Gmail. Sans protection, un pirate assis à deux tables de toi pourrait intercepter ton mot de passe, accéder à tes emails, et même lire tes documents personnels ou bancaires.

Pire encore : certains cybercriminels installent des **points d’accès Wi-Fi piégés**, appelés *evil twin* (jumeau malveillant). Ce sont des faux réseaux qui portent des noms crédibles comme "Wifi_Hotel_Officiel" ou "Free_Internet_Cafe". Une fois connecté, tout ton trafic passe par leur appareil. Ils peuvent rediriger vers des sites frauduleux, voler tes identifiants, ou installer des logiciels malveillants.

> **Exemple concret** : Un développeur freelance à Yaoundé se connecte au "Wi-Fi Hôtel Central" pour envoyer un contrat à un client. Il ne remarque pas que le bon réseau s’appelle "Hôtel Central - Invités". Le faux réseau, sans verrouillage, lui permet d’accéder à internet… mais aussi au pirate, qui capture ses identifiants de connexion GitHub. En quelques heures, le pirate télécharge tous ses projets et exige une rançon.

### Comment identifier un site web sécurisé

Avant de saisir tes informations personnelles, vérifie toujours l’adresse du site. Le petit cadenas vert dans la barre d’adresse n’est pas qu’un détail : il signale que la connexion est **chiffrée** grâce au protocole **HTTPS**.

HTTP (HyperText Transfer Protocol) est le langage de base des sites web. Mais **HTTPS** (HTTP Secure) ajoute une couche de chiffrement via un certificat SSL/TLS. Cela signifie que même si un pirate intercepte les données entre ton appareil et le site, il ne pourra pas les lire.

Compare ces deux exemples :
```
http://banque-exemple.com/login
https://ma-banque-officielle.ci/connexion
```

La première URL commence par `http` — **danger**. La seconde utilise `https` — **sécurisée**. Ne jamais se connecter à un site de banque, de messagerie ou de commerce en ligne sans HTTPS.

Tu peux aller plus loin en cliquant sur le cadenas. Cela t’affiche le certificat du site, émis par une autorité de confiance comme Let’s Encrypt, DigiCert ou Sectigo. Si le certificat est expiré ou invalide, ferme immédiatement la page.

### Utiliser un VPN pour chiffrer ta connexion

Un **VPN (Réseau Privé Virtuel)** est comme un tunnel sécurisé entre ton appareil et internet. Il masque ton adresse IP et chiffre tout ton trafic. Même sur un Wi-Fi public piraté, personne ne peut voir ce que tu fais en ligne.

Voici comment ça fonctionne :
1. Tu te connectes au Wi-Fi d’un cybercafé.
2. Tu lances ton application VPN (ex : ProtonVPN, TunnelBear, ou NordVPN).
3. Le VPN établit une connexion chiffrée avec un serveur distant.
4. Tout ton trafic passe par ce tunnel sécurisé.

> **Cas d’usage africain** : À Kinshasa, un développeur utilise un VPN gratuit pour accéder à GitHub et Stack Overflow, bloqués localement par son FAI. Le VPN contourne la censure, mais surtout, il protège ses identifiants et ses codes sources des regards indiscrets.

**Recommandations pour bien choisir un VPN** :
- Privilégie les services **payants** avec politique de non-enregistrement (*no logs*).
- Évite les VPN gratuits non fiables : certains vendent tes données ou injectent des publicités.
- Installe l’application officielle depuis le site du fournisseur, pas depuis des boutiques tierces.

Exemple d’installation avec ProtonVPN sur Android :
```bash
# 1. Rends-toi sur https://protonvpn.com depuis un navigateur sécurisé
# 2. Télécharge l’application officielle (ne la prends pas sur des sites APK)
# 3. Crée un compte (version gratuite disponible)
# 4. Lance l’appli, connecte-toi, sélectionne un serveur (ex: France, Suisse)
# 5. Active le bouton "Connexion" — le tunnel est ouvert
```

Une fois connecté, même ton opérateur ne verra que tu es sur un serveur ProtonVPN — pas tes sites visités.

### Attention aux applications non officielles et aux téléchargements pirates

En Afrique, le recours aux applications piratées ou modifiées est courant. Pourquoi ? Parce que les logiciels légaux coûtent cher, et les forfaits data sont limités. Beaucoup téléchargent des APK modifiés de WhatsApp, Photoshop ou Visual Studio Code depuis des forums ou groupes WhatsApp.

Mais ces fichiers sont souvent **injectés de malwares**. Un "WhatsApp+ gratuit" peut contenir un cheval de Troie qui enregistre tes messages, vole ton numéro, ou active ton micro à ton insu.

Même les mises à jour via SMS ou notifications push peuvent être frauduleuses. Un message disant *« Télécharge la mise à jour WhatsApp pour éviter la suspension »* n’est **jamais** envoyé par WhatsApp.

**Bonnes pratiques** :
- Télécharge **uniquement** depuis les magasins officiels : Google Play Store, Apple App Store, ou le site officiel du logiciel.
- Sur Android, désactive *« Sources inconnues »* dans les paramètres de sécurité.
- Vérifie les autorisations demandées : une application météo n’a pas besoin d’accéder à tes contacts.

Exemple de vérification d’un APK (avancé) :
```bash
# Sur PC, vérifie l’empreinte numérique (hash) avec sha256sum
sha256sum whatsapp-officiel.apk
# Compare le résultat avec le hash publié sur le site officiel
# S’ils ne correspondent pas → fichier modifié, potentiellement dangereux
```

### Bonnes habitudes pour naviguer en sécurité

La sécurité ne dépend pas que des outils — elle commence par **tes comportements**.

Voici des règles simples à appliquer tous les jours :

1. **Évite les achats ou connexions bancaires sur Wi-Fi public**, même avec un VPN. Attends un réseau privé.
2. **Active le mode privé/incognito** quand tu utilises un ordinateur partagé (cybercafé). Cela empêche l’enregistrement de tes mots de passe.
3. **Déconnecte-toi toujours** de tes comptes après utilisation.
4. **Mets à jour ton navigateur** régulièrement : les mises à jour corrigent des failles de sécurité critiques.
5. **Utilise un gestionnaire de mots de passe** comme Bitwarden ou KeePassXC. Il remplit automatiquement tes identifiants sans que tu les saisisse manuellement — réduisant le risque d’usurpation.

> **Astuce Empire du Web** : Si tu travailles souvent en mobilité, configure un **itinéraire de sécurité**. Exemple :  
> - Arrivée à l’hôtel → connexion au Wi-Fi  
> - Lancement immédiat du VPN  
> - Ouverture du gestionnaire de mots de passe  
> - Navigation uniquement sur HTTPS  
> Ce rituel devient automatique avec la pratique.

---

### Points clés

✅ **HTTPS est ton allié** : vérifie toujours le cadenas vert avant de saisir des données.  
✅ **Un Wi-Fi public est une zone à risque** : ne fais jamais de transactions sensibles sans protection.  
✅ **Un VPN chiffre ton trafic** : utilise ProtonVPN, TunnelBear ou NordVPN pour sécuriser ta connexion.  
✅ **Méfie-toi des applications piratées** : elles coûtent moins cher… mais peuvent te coûter très cher en données volées.  
✅ **Télécharge uniquement depuis les sources officielles** : Google Play, App Store, sites web légitimes.  
✅ **Adopte des réflexes de sécurité** : mode privé, déconnexion, mises à jour, et gestionnaire de mots de passe.  

Internet peut être sûr — à condition de savoir se protéger. Chaque fois que tu te connectes, demande-toi : *« Si quelqu’un m’espionnait en ce moment, que verrait-il ? »* Si la réponse te met mal à l’aise, c’est le moment d’activer ton VPN.