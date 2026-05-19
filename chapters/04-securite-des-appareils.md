## Sécurise Tes Appareils : Téléphone, Ordinateur et Tablettes

Ta vie numérique commence sur tes appareils. C’est là que tu stockes tes mots de passe, que tu reçois tes emails, que tu fais des transferts d’argent via Mobile Money, et que tu travailles sur des projets importants. Un smartphone, un ordinateur ou une tablette non sécurisé, c’est comme laisser la porte de ta maison grande ouverte avec un écriteau “Venez prendre ce que vous voulez”.

En Afrique, où les connexions internet peuvent être instables, les mises à jour sont parfois ignorées, et les applications piratées téléchargées depuis des sources inconnues. Ces habitudes, même si elles semblent pratiques, exposent énormément tes données personnelles, financières et professionnelles.

Il est temps d’agir. Ce chapitre t’apprend à transformer tes appareils en forteresses numériques, avec des étapes simples, accessibles, et surtout, adaptées à ton contexte.

---

### Active les mises à jour automatiques : ton bouclier invisible

Les pirates exploitent souvent des failles de sécurité dans les anciennes versions des systèmes d’exploitation. Une mise à jour, c’est une réparation. Chaque correctif bloque une porte que les hackers auraient pu utiliser.

#### Sur Android

Sur un smartphone Android (le plus répandu en Afrique), va dans **Paramètres > Système > Mises à jour système**. Active l’option **Mise à jour automatique**. Si tu as un forfait limité en data, choisis l’option “Mettre à jour uniquement via Wi-Fi”. Cela évite les frais imprévus.

> **Exemple concret** : En 2023, une faille dans une ancienne version d’Android a permis à des pirates d’installer discrètement des logiciels espions via un simple message SMS. Les utilisateurs à jour ont été protégés.

#### Sur Windows

Ouvre les **Paramètres > Mise à jour Windows**. Clique sur **Mise à jour automatique activée**. Windows mettra à jour ton système en arrière-plan, même quand tu l’utilises.

#### Sur Linux (Ubuntu)

Si tu es développeur ou utilisateur avancé, Linux n’est pas invulnérable. Met à jour régulièrement via le terminal :

```bash
sudo apt update && sudo apt upgrade -y
```

Tu peux automatiser cela avec un cron job :

```bash
# Ouvre l'éditeur de tâches automatiques
crontab -e

# Ajoute cette ligne pour mettre à jour chaque dimanche à 3h du matin
0 3 * * 0 sudo apt update && sudo apt upgrade -y
```

> **Astuce Empire du Web** : Planifie tes mises à jour pendant la nuit, quand tu n’utilises pas ton appareil. Cela minimise l’impact sur ta connexion.

---

### Chiffre tes données : rends-les illisibles en cas de vol

Le chiffrement transforme tes fichiers en texte incompréhensible sans une clé. Même si quelqu’un vole ton téléphone ou ton ordinateur, il ne pourra rien lire.

#### Chiffrement sur Android

La plupart des smartphones récents (Samsung, Huawei, Xiaomi) chiffrent automatiquement les données dès que tu définis un mot de passe d’écran. Vérifie dans **Paramètres > Sécurité > Chiffrement du périphérique**. Si tu vois “Chiffrement activé”, tu es protégé.

> **Attention** : Sans mot de passe ou code PIN, le chiffrement ne fonctionne pas. Un écran déverrouillé = zéro protection.

#### Chiffrement sur Windows

Utilise **BitLocker**, intégré aux versions Pro de Windows. Va dans **Panneau de configuration > Système > BitLocker**. Active-le sur ton disque C:. Tu devras sauvegarder la clé de récupération — stocke-la dans un endroit sûr, comme une clé USB ou un coffre-fort numérique (tu apprendras ça au chapitre 9).

> **Si tu as Windows Familiale** : tu n’as pas BitLocker. Utilise **VeraCrypt**, un logiciel gratuit et open source. Il permet de chiffrer tout le disque ou seulement certains dossiers.

#### Chiffrement sur Linux

Le chiffrement est souvent activé **pendant l’installation d’Ubuntu**. Si tu ne l’as pas fait, tu peux chiffrer ton dossier personnel ou utiliser LUKS.

```bash
# Vérifie si ton disque est chiffré
sudo cryptsetup isLuks /dev/sda2 && echo "Chiffré" || echo "Non chiffré"
```

> **Astuce Empire du Web** : Si tu travailles sur des projets sensibles (ex : application de santé mobile), chiffre ton dossier de travail avec VeraCrypt ou un outil similaire.

---

### Verrouille avec biométrie : visage, empreinte, ou mot de passe ?

Un code PIN simple comme 1234 ou 0000 ne protège rien. Heureusement, les smartphones actuels offrent des options plus sûres.

#### Utilise l’empreinte digitale ou la reconnaissance faciale

Sur Android, configure ton **empreinte digitale** ou **reconnaissance faciale** dans **Paramètres > Biométrie et sécurité**. L’empreinte est plus fiable que la reconnaissance faciale sur les téléphones bas de gamme.

> **Attention** : En cas de coupure ou de changement physique (lunettes, barbe), la reconnaissance peut échouer. Aie toujours un mot de passe de secours.

#### Sur ordinateur : mot de passe fort + verrouillage automatique

Configure ton ordinateur pour se verrouiller automatiquement après 5 minutes d’inactivité.

- **Windows** : Paramètres > Comptes > Options de connexion > Verrouiller après inactivité
- **Linux** : Paramètres > Énergie > Verrouiller l’écran après 5 min

Utilise un mot de passe différent de celui de ton téléphone, et ne le note jamais sur un post-it collé à l’écran !

---

### Installe un antivirus léger, adapté à ta connexion

Un antivirus n’est pas facultatif, surtout si tu partages souvent des fichiers via Bluetooth, WhatsApp ou clé USB.

#### Sur Android : opte pour un antivirus léger

Les antivirus lourds ralentissent les téléphones, surtout ceux avec peu de RAM. Préfère :

- **Kaspersky Security & Antivirus** (version gratuite)
- **Bitdefender Antivirus Free**

Ces apps consomment peu de batterie et de data. Elles détectent les logiciels malveillants dans les APK téléchargés depuis des sites comme 9apps ou Aptoide.

> **Cas réel Empire du Web** : Un développeur ivoirien a perdu tous ses projets après avoir installé une “version modifiée” de WhatsApp. Un antivirus simple l’aurait bloqué.

#### Sur Windows : Windows Defender suffit

Windows 10 et 11 incluent **Microsoft Defender**, un antivirus performant et gratuit. Il est activé par défaut. Pas besoin d’installer un logiciel supplémentaire qui ralentira ton PC.

Vérifie son état :

```powershell
# Ouvre PowerShell en tant qu'administrateur
Get-MpComputerStatus
```

Si `AntivirusEnabled` est True, tu es protégé.

#### Sur Linux : antivirus ? Oui, mais autrement

Linux est moins visé, mais **tu peux transmettre des virus à d’autres** (ex : un Windows que tu aides à réparer). Installe **ClamAV** :

```bash
sudo apt install clamav
sudo freshclam  # Met à jour la base de signatures
clamscan -r /home/tunom  # Analyse ton dossier
```

> **Astuce Empire du Web** : Lance un scan hebdomadaire, surtout si tu reçois beaucoup de fichiers ZIP ou DOCX.

---

### Fais un audit de sécurité sur ton appareil — maintenant

Prends ton téléphone ou ton ordinateur. Suis cette checklist en direct :

1. ✅ **Système à jour ?**  
   - Android : Paramètres > A propos du téléphone > Version  
   - Windows : Paramètres > Mise à jour  
   - Linux : `sudo apt update` puis `sudo apt list --upgradable`

2. ✅ **Chiffrement activé ?**  
   - Android : Paramètres > Sécurité  
   - Windows : BitLocker ou VeraCrypt  
   - Linux : `sudo cryptsetup isLuks /dev/sdX`

3. ✅ **Verrouillage d’écran fort ?**  
   - Code de 6 chiffres minimum, ou biométrie  
   - Verrouillage automatique après 5 min

4. ✅ **Antivirus installé et à jour ?**  
   - Android : Kaspersky ou Bitdefender  
   - Windows : Microsoft Defender actif  
   - Linux : ClamAV mis à jour

5. ✅ **Applications inconnues bloquées ?**  
   - Android : Paramètres > Applications > Sources inconnues → Désactivé

6. ✅ **Localisation et suppression à distance activées ?**  
   - Android : “Localiser mon appareil” dans Google Find My Device  
   - Windows : “Localiser mon appareil” dans les paramètres Microsoft  
   - Linux : Installe `prey` pour le suivi

> **À faire tout de suite** : Si tu as coché moins de 5 cases, corrige cela maintenant. Ton futur toi te remerciera.

---

### Bonnes pratiques quotidiennes pour rester protégé

- **Ne branche jamais de clé USB trouvée dans la rue**. Elle peut contenir un virus qui se lance automatiquement.
- **Évite les apps “mod”** (ex : Facebook modifié, Instagram sans pub). Elles volent souvent tes données.
- **Redémarre ton appareil une fois par semaine**. Cela ferme les processus malveillants en mémoire.
- **Utilise un chargeur officiel**. Les chargeurs piratés peuvent injecter des logiciels espions (“juice jacking”).

> **Cas concret** : Un développeur sénégalais a vu son compte GitHub compromis après avoir utilisé un câble USB public dans un cybercafé. Depuis, il utilise un **câble de chargeur seul** (sans transfert de données).

---

## Points clés

- ✅ Les mises à jour automatiques sont ta première ligne de défense. Active-les sur tous tes appareils.
- ✅ Le chiffrement protège tes données en cas de vol. Active-le dès maintenant.
- ✅ Utilise l’empreinte ou un code fort (6+ chiffres) pour verrouiller ton écran.
- ✅ Installe un antivirus léger, surtout sur Android. Windows Defender suffit sur PC.
- ✅ Fais un audit de sécurité régulier : mise à jour, chiffrement, verrouillage, antivirus.
- ✅ En Afrique, adapte ta sécurité à ta connexion : mises à jour en Wi-Fi, antivirus légers, sauvegardes locales.
- ✅ Un appareil non sécurisé = toutes tes données exposées. Agis maintenant.

> **Prochain défi Empire du Web** : Dans 24 heures, fais une capture d’écran de ton écran de verrouillage et partage-la (sans montrer ton code !) pour prouver que tu as sécurisé ton appareil.