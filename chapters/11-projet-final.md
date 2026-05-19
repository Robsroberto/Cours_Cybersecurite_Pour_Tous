## Audit Complet de Ta Sécurité Numérique

Tu as acquis des outils puissants au fil des chapitres : gestion de mots de passe, chiffrement, détection du phishing, sauvegardes fiables. Maintenant, il est temps de tout rassembler. Ce projet final n’est pas un examen, c’est un levier de transformation. Il s’agit de passer de la théorie à l’action concrète, en auditant **tous les aspects de ta vie numérique**, qu’ils soient personnels ou professionnels.

L’objectif ? Identifier tes points faibles, prioriser les corrections, et construire un plan d’action réaliste, efficace, et durable. À la fin de ce chapitre, tu auras non seulement sécurisé ton environnement actuel, mais tu auras aussi mis en place un processus que tu pourras répéter régulièrement.

---

### Étape 1 : Liste de tous tes appareils et comptes

Commence par créer un document — un carnet, un fichier texte, ou une feuille de calcul. Note **tout** ce que tu utilises régulièrement. Ne sous-estime rien.

#### Appareils à inventorier
- Smartphone (Android ou iOS)
- Ordinateur portable ou de bureau (Windows, macOS, Linux)
- Tablette
- Disques durs externes
- Routeur Wi-Fi
- Smart TV ou autres objets connectés (montre, enceinte, etc.)

Exemple concret :  
Un développeur freelance à Abidjan utilise un smartphone Android pour ses appels, un ordinateur portable Lenovo sous Linux pour coder, un disque dur externe pour ses sauvegardes, et une clé 4G de son opérateur local (Moov, Orange, etc.) comme connexion principale.

#### Comptes en ligne à répertorier
- Email (personnel, professionnel, ancien)
- Réseaux sociaux (WhatsApp, Facebook, LinkedIn, Twitter/X, Instagram)
- Services bancaires en ligne
- Plateformes de travail (Trello, Slack, GitHub, GitLab)
- Services de stockage cloud (Google Drive, Dropbox, iCloud)
- Abonnements (Netflix, Spotify, etc.)
- Comptes de développeur (Google Play, Apple Developer, AWS, etc.)

Tu peux organiser ces comptes en deux colonnes : **utilisation fréquente** et **utilisation occasionnelle**. Cela t’aidera à prioriser.

---

### Étape 2 : Évaluation de la sécurité de chaque élément

Maintenant que tu as ta liste, évalue chaque item selon les critères appris dans les chapitres précédents.

#### Pour chaque appareil
Pose-toi ces questions :
- Est-il à jour (système d’exploitation, applications) ?
- A-t-il un mot de passe ou un code d’accès ?
- Est-il protégé par chiffrement (ex : BitLocker sur Windows, FileVault sur macOS, chiffrement activé sur Android) ?
- Utilise-t-il un antivirus ou un pare-feu ?

Exemple :  
Un développeur à Dakar utilise un vieux téléphone Android sans mise à jour depuis 2022. Il n’a pas de verrouillage d’écran. Ce téléphone est **hautement vulnérable**. Même s’il ne contient pas de données sensibles, il peut servir de porte d’entrée vers d’autres comptes (ex : réinitialisation de mot de passe via SMS).

#### Pour chaque compte en ligne
Pose-toi ces questions :
- Utilises-tu un mot de passe unique et fort (au moins 12 caractères, lettres, chiffres, symboles) ?
- Utilises-tu l’authentification à deux facteurs (2FA) ?
- Le mot de passe est-il partagé entre plusieurs comptes ?
- As-tu vérifié si ton email a été compromis ? (Utilise [haveibeenpwned.com](https://haveibeenpwned.com))

Exemple :  
Un développeur à Kinshasa utilise le même mot de passe pour son email Gmail, son compte GitHub et sa banque en ligne. Même si le mot de passe est long, **le réutiliser est une grave erreur**. Si un site moins sécurisé fuit ses données, tous ses comptes sont menacés.

Tu peux créer un tableau simple :

| Compte | Mot de passe unique ? | 2FA activé ? | Date de dernière mise à jour du mot de passe | Risque |
|--------|------------------------|-------------|-----------------------------------------------|--------|
| Gmail | Oui | Oui | 03/2024 | Faible |
| Facebook | Non (utilise même que Twitter) | Non | 12/2021 | Élevé |
| GitHub | Oui | Oui (via Google Authenticator) | 06/2023 | Modéré |

---

### Étape 3 : Analyse de tes habitudes numériques

La technologie n’est qu’une partie du problème. Tes comportements jouent un rôle crucial.

Pose-toi ces questions :
- Utilises-tu souvent le Wi-Fi public (cafés, gares, espaces de coworking) sans VPN ?
- Clics-tu sur des liens dans des emails ou messages WhatsApp sans vérifier l’expéditeur ?
- Partages-tu tes informations personnelles (date de naissance, lieu de résidence) publiquement sur les réseaux sociaux ?
- Télécharges-tu des applications en dehors des stores officiels (APK depuis des sites inconnus) ?

Exemple :  
Un développeur à Lomé utilise régulièrement le Wi-Fi du centre commercial pour accéder à sa messagerie professionnelle. Il ne sait pas que cette connexion est non chiffrée. Un pirate sur le même réseau pourrait intercepter ses données. **Solution : utiliser un VPN fiable comme ProtonVPN ou Mullvad, même sur mobile.**

---

### Étape 4 : Rédige ton plan d’action personnalisé

À partir de ton audit, identifie les **3 vulnérabilités les plus critiques** et établis un plan pour les corriger.

Exemple de plan d’action :

1. **Problème** : Mots de passe réutilisés sur plusieurs comptes.  
   **Action** : Installer un gestionnaire de mots de passe (Bitwarden, KeePassXC).  
   **Étapes** :
   - Télécharger Bitwarden sur mon téléphone et mon ordinateur.
   - Créer un mot de passe maître très fort (ex : `Café#Dev2024!Lomé@Secure`).
   - Importer tous mes comptes.
   - Générer de nouveaux mots de passe uniques pour Gmail, Facebook, GitHub.
   - Activer la 2FA sur ces comptes.

2. **Problème** : Ancien téléphone Android sans mise à jour.  
   **Action** : Réinitialiser l’appareil et activer le chiffrement.  
   **Étapes** :
   - Sauvegarder les données importantes.
   - Réinitialiser aux paramètres d’usine.
   - Mettre à jour le système si possible.
   - Activer le verrouillage par code PIN (6 chiffres) et le chiffrement dans les paramètres.

3. **Problème** : Navigation sans protection sur Wi-Fi public.  
   **Action** : Installer un VPN sur tous mes appareils.  
   **Étapes** :
   - Choisir un fournisseur de confiance (ProtonVPN, gratuit pour usage basique).
   - Installer l’application sur Android et Linux.
   - Activer le démarrage automatique du VPN.

Tu peux aussi prévoir des actions à plus long terme :
- Chiffrer ton disque dur externe avec **VeraCrypt**.
- Mettre en place un calendrier de sauvegarde mensuel.
- Former un collègue ou un proche à la cybersécurité.

---

### Étape 5 : Mise en œuvre immédiate

Ne repousse rien à demain. Commence **aujourd’hui**.

Voici un script de terminal simple pour vérifier rapidement l’état de ton système Linux (utile pour les développeurs) :

```bash
#!/bin/bash
# Script d'audit rapide - Empire du Web

echo "🔍 Audit de sécurité système - $(date)"
echo "----------------------------------------"

# Vérifier les mises à jour système
echo "📦 Mises à jour disponibles ?"
apt list --upgradable 2>/dev/null | head -5

# Vérifier le pare-feu (ufw)
echo "🛡️  Pare-feu actif ?"
ufw status | grep -q "active" && echo "✅ Actif" || echo "❌ Inactif - Active-le avec 'sudo ufw enable'"

# Vérifier les services en écoute
echo "🌐 Services en écoute (ports ouverts) :"
ss -tuln | grep LISTEN

# Vérifier les dernières connexions
echo "👤 Dernières connexions :"
last | head -3

echo "✅ Audit terminé. Agis sur les points critiques."
```

Sauve ce script dans un fichier `audit.sh`, rends-le exécutable (`chmod +x audit.sh`) et lance-le dans ton terminal. Il te donnera un aperçu rapide des risques sur ta machine.

---

### Étape 6 : Documente et planifie un suivi

À la fin de ton audit, crée un document de synthèse :
- Liste des vulnérabilités corrigées
- Actions en cours
- Actions à faire dans 1 mois (ex : changer tous les mots de passe faibles)
- Date du prochain audit (ex : 3 mois plus tard)

Tu peux utiliser un outil simple comme **Google Docs** ou **Notion**. Si tu travailles en équipe, partage une version anonymisée pour sensibiliser tes collègues.

---

## Points clés

- ✅ **Un audit complet passe par l’inventaire systématique** de tous tes appareils, comptes et habitudes.
- ✅ **La réutilisation de mots de passe est l’une des erreurs les plus courantes** — utilise un gestionnaire comme Bitwarden.
- ✅ **La 2FA sauve des comptes** — active-la sur ton email, GitHub, et banque en ligne.
- ✅ **Même les petits appareils (téléphone, routeur) peuvent être des points d’entrée** pour les pirates.
- ✅ **Le comportement compte autant que la technologie** — évite les Wi-Fi publics non sécurisés, ne clique pas sur des liens douteux.
- ✅ **Agis immédiatement sur les 3 risques les plus critiques** — ne te disperse pas.
- ✅ **Documente ton plan d’action et planifie un suivi** — la cybersécurité est un processus, pas un événement ponctuel.

Ce projet n’est pas la fin. C’est le début d’une nouvelle hygiène numérique. En l’appliquant, tu passes du statut de victime potentielle à celui de **gardien de ta sécurité**. Et c’est exactement ce que t’enseigne Empire du Web : ne pas subir le numérique, mais le maîtriser.