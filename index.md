---
title: Support
---

*[Privacy policy](privacy) · [Version française](#speed-vario--assistance)*

# Speed Vario — Support

*Last updated: September 2026*

A question, a bug, a translation that reads wrong: **variospeed67@gmail.com**

Speed Vario is an independent, one-person project, offered as-is. There is no support desk and no guaranteed response time — but every message is read, and feedback genuinely shapes what gets built next. When reporting a problem, please include your iPhone (and Apple Watch) model, the iOS version, and a short description of what you saw.

---

## What comes up most often

### GPS is not locking

Settings → Privacy & Security → Location Services → Speed Vario, set to **While Using** or **Always**. *Always* is what lets a recording continue in the background with the screen locked. Indoors, expect a weak fix or none: this is a GPS logger, and it has little to work with under a roof.

### The altitude looks wrong

Barometric altitude is the most accurate reading available, but it follows the weather: a passing front moves the reference. The app re-anchors on GPS as it goes. On a summit or after a long climb, give it a minute outdoors with a clear sky view.

### Heart rate shows "—" on the watch

Open the iPhone Watch app → Privacy → Health → Speed Vario and make sure **Heart Rate** is enabled. This permission can reset itself after reinstalling the app, and it is the cause almost every time.

### Ski runs or the resort name are missing

Piste, lift and resort names are fetched once from OpenStreetMap and then cached. Open the session while online; from then on they stay available offline.

### Country flags are missing on a track

They are computed offline the first time a session appears in the logbook. Just open the Logbook tab.

### A session disappeared after a crash

Speed Vario has crash recovery: relaunch, and the interrupted session should be restored on its own.

---

## Backing up and moving your history

Two ways, and the first is the one to pick.

**iCloud backup (automatic).** Settings → Data → iCloud Backup. Once on, every outing is copied to your own private iCloud space as it is recorded. On a new iPhone, install the app and tap **Restore from iCloud** — the whole history comes back. Turn on **Sync my devices** as well and your outings also appear on an iPad or a second iPhone signed in to the same iCloud account.

**History archive .zip (manual).** Settings → Data → History Archive exports everything as one file you can keep in Files, mail to yourself, or re-import later. Still the right tool for taking your tracks *out* of the app, or for keeping a copy somewhere other than iCloud.

### Does my heart rate go to iCloud?

**No — never.** Apple's rules forbid apps from storing health data in iCloud, so heart rate and active energy are stripped out of everything Speed Vario uploads. They stay on the device and in Apple Health. When you restore a session onto a new iPhone, the app reads them back from Apple Health for that session's time window, so the heart-rate chart is rebuilt anyway — provided "Save to Apple Health" was on when you recorded it.

### iCloud says "No iCloud account on this device"

Open iOS Settings → your name → iCloud and sign in. Check that iCloud Drive is on: an account signed in with iCloud Drive switched off cannot store app data.

### I deleted an outing by mistake — can I get it back?

If iCloud backup is on and "Sync my devices" is *off*: yes. A local deletion leaves the cloud copy untouched — that is the whole point of a backup. Settings → Data → iCloud Backup → **Restore from iCloud** brings back everything missing from the device. With sync on, a deliberate deletion is propagated on purpose and cannot be undone.

### Will iCloud backup delete my old sessions when the retention period expires?

No. Automatic deletion by retention period is a per-device housekeeping rule and is never propagated to iCloud or to your other devices — an iPhone set to 30 days will not wipe the history of an iPad set to Unlimited.

### How do I delete my data?

In the Logbook, swipe left on any session to delete it, or uninstall the app to remove everything held on the device. If you used iCloud backup, erase the cloud copy too: Settings → Data → iCloud Backup → Manage iCloud copy → **Erase iCloud copy**. That copy lives in your own iCloud account — the developer has no access to it and cannot delete it for you.

---

## What the app does

- Real-time speed (km/h, mph, knots), GPS + barometric altitude, and vertical speed (variometer)
- Live glide ratio in flight, heading, and a GPS-quality indicator
- One-tap recording, background recording, and crash recovery
- **Skiing:** automatic run / lift detection, day dashboard, piste and lift names from OpenStreetMap
- **Aviation:** pressure altitude (flight level), airtime, departure → arrival aerodromes, IGC import / export
- **Apple Watch:** live readout, standalone recording when the iPhone is out of range, haptic variometer
- **Water (Apple Watch Ultra):** water temperature, depth and immersion time
- Interactive map with a speed-coloured route, 3D terrain view, and 3D fly-through video export
- Flags of every country your track crosses
- Apple Health: workouts saved with their GPS route
- Optional iCloud backup and multi-device sync — your own iCloud, no account, no subscription
- Export GPX, CSV, KMZ, FIT and IGC; import GPX, CSV, IGC
- No account, no ads, no trackers

---
---

# Speed Vario — Assistance

*Dernière mise à jour : septembre 2026*

Une question, un défaut à signaler, une traduction qui sonne faux : **variospeed67@gmail.com**

Speed Vario est un projet indépendant, écrit par une seule personne, fourni tel quel. Il n'y a pas de service d'assistance ni de délai de réponse garanti — mais chaque message est lu, et les retours orientent réellement la suite. Pour signaler un problème, indiquez le modèle d'iPhone (et d'Apple Watch), la version d'iOS, et ce que vous avez observé.

---

## Ce qui revient le plus souvent

### Le GPS n'accroche pas

Réglages → Confidentialité et sécurité → Service de localisation → Speed Vario, réglé sur **Lorsque l'app est active** ou **Toujours**. C'est *Toujours* qui permet à un enregistrement de continuer en arrière-plan, écran verrouillé. À l'intérieur, attendez-vous à un signal faible ou nul : c'est un enregistreur GPS, et sous un toit il n'a pas grand-chose à se mettre sous la dent.

### L'altitude semble fausse

L'altitude barométrique est la mesure la plus fine disponible, mais elle suit la météo : un front qui passe déplace la référence. L'app se recale sur le GPS au fil de la sortie. Sur un sommet ou après une longue montée, laissez-lui une minute à ciel dégagé.

### La montre affiche « — » à la place du pouls

Ouvrez l'app Watch sur l'iPhone → Confidentialité → Santé → Speed Vario et vérifiez que **Fréquence cardiaque** est activé. Cette autorisation se réinitialise parfois après une réinstallation, et c'est la cause quasi systématique.

### Les pistes de ski ou le nom de la station manquent

Les noms de pistes, remontées et stations sont récupérés une fois depuis OpenStreetMap puis mis en cache. Ouvrez la séance en étant connecté ; ensuite ils restent disponibles hors ligne.

### Les drapeaux des pays manquent sur une trace

Ils sont calculés hors ligne à la première apparition de la séance dans le carnet. Il suffit d'ouvrir l'onglet Carnet.

### Une séance a disparu après un plantage

Speed Vario récupère les enregistrements interrompus : relancez l'app, la séance devrait revenir d'elle-même.

---

## Sauvegarder et déplacer son historique

Deux chemins, et le premier est celui à choisir.

**Sauvegarde iCloud (automatique).** Réglages → Données → Sauvegarde iCloud. Une fois activée, chaque sortie est copiée dans votre espace iCloud privé au fil de son enregistrement. Sur un nouvel iPhone, installez l'app et touchez **Restaurer depuis iCloud** : tout l'historique revient. Activez aussi **Synchroniser mes appareils** et vos sorties apparaissent également sur un iPad ou un second iPhone connecté au même compte iCloud.

**Archive .zip (manuelle).** Réglages → Données → Sauvegarde de l'historique exporte tout dans un fichier unique, à ranger dans Fichiers, à s'envoyer par mail, ou à réimporter plus tard. Cela reste le bon outil pour sortir ses traces de l'app, ou pour garder une copie ailleurs que dans iCloud.

### Ma fréquence cardiaque monte-t-elle dans iCloud ?

**Non — jamais.** Les règles d'Apple interdisent aux apps de stocker des données de santé dans iCloud : la fréquence cardiaque et l'énergie active sont donc retirées de tout ce que Speed Vario envoie. Elles restent sur l'appareil et dans Apple Santé. Lors d'une restauration sur un nouvel iPhone, l'app les relit dans Apple Santé sur la fenêtre temporelle de la séance, si bien que la courbe cardiaque est reconstituée malgré tout — à condition que « Enregistrer dans Apple Santé » ait été actif au moment de l'enregistrement.

### iCloud affiche « Aucun compte iCloud sur cet appareil »

Ouvrez Réglages iOS → votre nom → iCloud et connectez-vous. Vérifiez aussi qu'iCloud Drive est activé : un compte connecté mais iCloud Drive coupé ne peut pas stocker de données d'app.

### J'ai supprimé une sortie par erreur — puis-je la récupérer ?

Si la sauvegarde iCloud est active et que « Synchroniser mes appareils » est *désactivé* : oui. Une suppression locale ne touche pas la copie du nuage — c'est tout l'intérêt d'une sauvegarde. Réglages → Données → Sauvegarde iCloud → **Restaurer depuis iCloud** ramène tout ce qui manque à l'appareil. Avec la synchronisation active, une suppression volontaire est propagée à dessein et ne peut pas être annulée.

### La sauvegarde iCloud va-t-elle supprimer mes anciennes séances à l'expiration de la durée de conservation ?

Non. La suppression automatique par durée de conservation est une règle de ménage propre à chaque appareil, jamais propagée à iCloud ni aux autres appareils : un iPhone réglé sur 30 jours n'effacera pas l'historique d'un iPad réglé sur « Illimité ».

### Comment supprimer mes données ?

Dans le Carnet, balayez une séance vers la gauche pour la supprimer, ou désinstallez l'app pour effacer tout ce qu'elle détient sur l'appareil. Si vous avez utilisé la sauvegarde iCloud, effacez aussi la copie du nuage : Réglages → Données → Sauvegarde iCloud → Gérer la copie iCloud → **Effacer la copie iCloud**. Cette copie vit dans votre propre compte iCloud — le développeur n'y a aucun accès et ne peut pas la supprimer à votre place.

---

## Ce que fait l'app

- Vitesse en temps réel (km/h, mph, nœuds), altitude GPS + barométrique, vitesse verticale (variomètre)
- Finesse en direct en vol, cap, indicateur de qualité GPS
- Enregistrement en un tap, en arrière-plan, avec récupération après plantage
- **Ski :** découpage automatique en pistes et remontées, tableau de bord du jour, noms via OpenStreetMap
- **Aviation :** altitude pression (niveau de vol), temps de vol, aérodromes de départ et d'arrivée, import/export IGC
- **Apple Watch :** affichage en direct, enregistrement autonome hors de portée de l'iPhone, variomètre haptique
- **Eau (Apple Watch Ultra) :** température de l'eau, profondeur et durée d'immersion
- Carte interactive au tracé coloré par la vitesse, vue terrain 3D, export vidéo de survol
- Drapeaux de tous les pays traversés
- Apple Santé : entraînements enregistrés avec leur tracé GPS
- Sauvegarde iCloud et synchronisation multi-appareils, optionnelles — votre iCloud, sans compte ni abonnement
- Export GPX, CSV, KMZ, FIT et IGC ; import GPX, CSV, IGC
- Sans compte, sans publicité, sans traceur

---

*Speed Vario — © 2026. Tous droits réservés.*
