---
title: Privacy Policy
---

*[Français](#politique-de-confidentialité--speed-vario-français) · [Support](./)*

# Privacy Policy — Speed Vario

*Last updated: 21 October 2026*

## Overview

Speed Vario ("the app") is a GPS speed and altitude logging application for iPhone and Apple Watch. Your privacy is important. This policy explains what data is used, how it is processed, and how it is protected.

Speed Vario has **no account, no analytics, no advertising and no third‑party trackers**. Your recordings live on your device — and, if you switch on iCloud Backup, in **your own private iCloud space**, which the developer cannot access. There is no developer server that receives your data (unless you switch on live sharing, below): the only files the developer publishes are static map data (place names, see below), served by GitHub Pages.

## Data used

- **Location (GPS)** — Real‑time and background location is used exclusively to compute speed, altitude and heading, and to record your session route. Track data is stored locally on your device.
- **Motion sensors** — The barometer and accelerometer are used to improve altitude and vertical‑speed accuracy. This data is processed on‑device and is not stored separately.
- **Water sensors (Apple Watch Ultra, Water mode)** — While recording in Water mode, the watch's depth and water‑temperature sensors report submersion state, depth and water temperature. Unlike the motion data above, these readings *are* saved with the session, exactly like speed or altitude. They are measured and stored on your device and are never transmitted.
- **Health data (heart rate & active energy)** — When you record with a paired Apple Watch, these are read from Apple Health (HealthKit) to show them live and save them with the session. See "Health data" below.

## Health data (HealthKit)

When you record an activity with a paired Apple Watch, Speed Vario reads your **heart rate** and **active energy** from Apple HealthKit so they can be shown live and stored alongside the session on your device.

If you enable "Save to Apple Health" (Settings → on by default), Speed Vario also **writes your completed activity to Apple Health as a workout**, including the GPS route, distance, duration, elevation gain, active energy and average heart rate. You can disable this at any time in Settings, and you can revoke HealthKit access at any time in the Apple Health app or in iOS Settings. Health data is read from / written to Apple Health only; it is never sent to any server controlled by the developer (the only exception is live sharing, if you start it: heart rate then travels **encrypted**, see "Live sharing"), never shared for advertising, and **never stored in iCloud by the app** — including when iCloud Backup is switched on, where heart rate and active energy are deliberately excluded from what is uploaded (see "iCloud Backup" below). Deleting a recorded session deletes its health data from the app's own database.

## iCloud Backup and sync (optional, off by default)

Speed Vario can copy your recorded outings to **your own private iCloud database**, so that a lost, broken or replaced iPhone does not take your history with it. It is **off until you turn it on**, either from the one‑time prompt shown after a few recordings or at any time in Settings → Data → iCloud Backup. Two separate switches:

- **Back up to iCloud** — each outing is uploaded as it is recorded. Deleting an outing on your iPhone does **not** delete the iCloud copy; that is what lets you recover it. Restoring is an explicit action ("Restore from iCloud").
- **Sync my devices** — in addition, outings are downloaded automatically onto other devices signed in to the same iCloud account, and an outing you deliberately delete is deleted on those devices too. Automatic deletion by retention period is **never** propagated: it is a per‑device housekeeping rule, not a decision about that outing.

**Where the data goes.** Into the **private database of your own iCloud account**, using Apple's CloudKit. It counts against your own iCloud storage. The developer has no access to it, cannot list it, and cannot read it. There is no developer‑operated server involved at any point, and no account to create — your Apple Account is the only identity used, by Apple, not by us.

**What is uploaded:** the GPS track (coordinates, altitude, speed, vertical speed, heading), barometric altitude, cadence and step count (from the device's motion sensors), lap marks, session name and statistics, resolved place names, and — in Water mode with an Apple Watch Ultra — water temperature and depth.

**What is never uploaded:** your **heart rate** and **active energy**. These come from Apple HealthKit, and Apple's App Store Review Guidelines (5.1.3) prohibit storing personal health information in iCloud. They are stripped out of everything the app sends, including the pre‑edit snapshot kept for sessions you have trimmed. They remain on the device and in Apple Health. After restoring a session onto another device, the app reads heart rate and active energy back **from Apple Health** for that session's time window — Apple Health has its own end‑to‑end encrypted sync — so the chart is rebuilt without that data ever passing through the app's iCloud storage.

**Turning it off, and erasing it.** Switching the feature off stops all uploads immediately; the copy already in iCloud is left alone. Settings → Data → iCloud Backup → Manage iCloud copy lists everything held there and offers **Erase iCloud copy**, which permanently deletes all of it. Deleting the app, or turning off iCloud Drive for Speed Vario in iOS Settings, also stops any further upload.

## Live sharing (optional, off by default)

Live sharing lets someone you choose follow your outing on a map, in real time, from a web page. It is **off by default**: nothing is created or sent until you read the notice and tap "Start sharing". You can stop it at any time (a red Stop button is always within reach, on the iPhone and on the Apple Watch), and it also ends with your recording. This is the **only** feature that sends your data to a server chosen by the developer, so it is described here in detail.

**What is sent.** Roughly every 15 seconds (every 30 seconds below 30 % battery; sharing stops below 10 %): position, altitude, speed, vertical speed, distance, climb and descent, heading, cadence and steps where measured, height above ground where available, battery level, and the name of the outing if you typed one. **Heart rate is sent only if you switch on the separate "Share my heart rate" option** (off by default); if it is off, no heart rate is ever included. Heart rate is health data: it travels only inside the encrypted stream, is never used for advertising, and is never written to iCloud.

**End-to-end encryption.** Every point is encrypted **on your device** (AES-256-GCM) before it leaves. The key is created for that one share and exists only in the link you share (in the part after the "#", which browsers never send to any server) and in its QR code. The developer, Google and the hosting service receive only encrypted bytes and **cannot read your position, your heart rate or the name of your outing**. The viewer's browser decrypts the data locally.

**What the server can still see, because encryption cannot hide it:** that a share exists, when and how often data is sent, when it started and ended, the number of points, the size of the messages (kept constant on purpose), and the IP addresses of your devices and of the people who open the link (an approximate area, as for any web request). One anonymous Firebase account is created per share; it is not linked to your name, your Apple ID or any other share.

**Who processes it.** A Google Firebase project operated by the developer (Realtime Database, Authentication with anonymous accounts, and Hosting for the viewer page at speedvario.web.app); Google acts as a processor. The app talks to it with plain HTTPS requests and contains no Google or Firebase SDK. The viewer page loads map tiles from OpenFreeMap and elevation tiles from AWS Terrain Tiles, which can see the map area a viewer looks at. The page contains no analytics, no cookies and no advertising; it keeps the link only in the browser tab (session storage) and removes the key from the address bar as soon as it has read it.

**How long.** The link stops working 2 hours after your recording ends (the final track stays visible for that time) and never lives more than 24 hours, whatever happens. The app then deletes the data from the server the next time it launches. If you resume recording within 10 minutes, the same link carries on.

**Who can see it.** Anyone who holds the complete link can read the outing until it expires: share it only with people you trust. Stopping the sharing ends the link for everyone.

## Network use

Speed Vario works offline for its core features (live readout and recording). Country detection for your tracks is performed **entirely on‑device** (no network). A few **optional** features send the relevant coordinates to third‑party services, and only when you use them (live sharing, which sends end-to-end encrypted data to the developer's Firebase project, is described in its own section above):

- **Maps, 3D terrain and satellite fly‑through video** use Apple **MapKit**, which sends location to Apple to fetch map imagery and elevation, under Apple's privacy policy. With no network connection the app falls back to a **basemap bundled inside the app** (public‑domain Natural Earth data): coastlines, lakes, rivers, glaciers, urban areas, major roads, cities and airports. That fallback requires no connection and sends nothing anywhere.
- **Offline place names** — the offline basemap names towns, villages, peaks and passes from **OpenStreetMap** data. Cities, towns and well‑known peaks are bundled inside the app. Villages, hamlets and the other peaks and passes of the area around you are downloaded **ahead of time, while you have a connection**, so the map can name them once you lose it: the app requests the files of the 1° squares (about 100 km) around your position from **GitHub Pages** (thmaed.github.io), where they are published as static files. Only the address of each square is requested — never your precise position, your tracks or any identifier — though, as with any web request, GitHub sees your IP address. The files are kept on your device and refreshed every few months.
- **Place names** — ski resort / lift names and departure/arrival aerodrome names are looked up from **OpenStreetMap** (Overpass API). Only the queried coordinates are sent; the result is cached on your device so the lookup runs once.
- **Route drawing** — when you draw a route on the map, the trails and paths of the area shown are downloaded from **OpenStreetMap** (Overpass API) so the route can follow them. Only the rectangle of map being viewed is sent, never your position or the route; the trails are kept on your device for 30 days and the way along them is computed entirely on your device. By car — and on foot when OpenStreetMap does not answer — the way between two points you placed is asked of Apple (**MapKit** directions): those two points are sent to Apple, under Apple's privacy policy.
- **Ski lifts** — on skis, the height above ground is shown only while you ride a chairlift, gondola or cable car. To know where those are, the app asks **OpenStreetMap** (Overpass API) for the lifts within about 10 km of your position, once per area; nothing else is sent, and the answer is kept on your device.
- **Elevation** — the climbing of a drawn route, the 3D terrain, the fly‑through video and the **height above ground** read elevation from the open **AWS Terrain Tiles** (Amazon Web Services open data), with **OpenTopoData** (opentopodata.org, open SRTM data) as a fallback for some views. Only the tiles or points covering the area are requested. For the height above ground, the tiles around your position are fetched when you arm take‑off detection or start a recording, and you can download an area in advance from Settings → Offline terrain. When the Apple Watch records, it requests the same tiles and lifts for its own position, through the iPhone's connection or its own. Tiles are kept on the device (up to 250 MB on the iPhone, 60 MB on the watch; the least used go first) and can be erased from the same screen.
- **Aerodromes and runways** — in Aviation mode the app names the fields you took off from, landed at or touched, and the runway used, from a **database bundled inside the app** (derived from public-domain OurAirports data). It is read-only and queried entirely on your device: identifying an airfield sends nothing anywhere, and the flight it belongs to is never transmitted.

No other data is transmitted. There is no developer server; the only data that leaves your device for a service the developer chose is live sharing, if you start it — encrypted, and unreadable by the developer.

## Data we do NOT collect

- No personal information (name, email, account).
- No analytics services, advertising SDKs or third‑party trackers.
- Unless you start live sharing (encrypted, see above), no data is uploaded to or stored on any server operated by the developer. (iCloud Backup, when you enable it, stores data in *your* iCloud account — not the developer's, and not accessible to the developer.)
- No data is sold or shared for marketing.

## Data storage

Session recordings (track points, speed, altitude, and — when recorded with an Apple Watch — heart rate, active energy, and in Water mode depth and water temperature) are stored in the local SwiftData database on your device. If you enable iCloud Backup, a copy of each outing **minus heart rate and active energy** is also stored in your own private iCloud database, as described above; with the feature off — its default state — the local database is the only place they exist. Exported files (GPX, CSV, KMZ, FIT, IGC, history archive .zip and fly‑through videos) are written to the system temporary directory, or shared via the iOS share sheet to a destination you choose. Copies left behind in temporary storage are deleted automatically the next time the app launches, and can be cleared at any moment from Settings → Cache.

If you switch on **Record raw data** (Settings → Data → Raw data — off by default, and intended for diagnosing sensor behaviour), the app additionally writes CSV files of raw sensor readings, including precise coordinates, into its own Documents folder. When an Apple Watch recording is involved it sends its own file to the iPhone over the direct Watch link. These files never leave your device unless you export them yourself; those of the last 30 outings are kept, and they can be exported or deleted from the same screen. Elevator and roller-coaster rides (experimental modes) always keep their motion-sensor readings, for 30 days, so that a ride can be recalculated; they include the few GPS positions of the ride and stay on your device.

## Data retention and deletion

Sessions are automatically deleted after the retention period set in the app's Settings (7 days, 30 days, 3 months, 6 months, 1 year, or Unlimited; default 30 days). You can change this at any time in Settings → History, and you can delete any session manually from the History tab. GPS history is excluded from unencrypted iTunes / Finder backups. Live sharing data is kept for at most 24 h, and 2 h after the end of the outing; the app erases it from the server the next time it launches, and you can stop it at any time. Deleting the app removes all data stored on the device permanently; if iCloud Backup was enabled, the copy in your iCloud account survives until you erase it (Settings → Data → iCloud Backup → Manage iCloud copy → Erase iCloud copy) or delete it from your iCloud storage.

## Children

The app does not target children under 13 and does not knowingly collect data from children.

## Changes to this policy

If this policy changes, the updated version will be posted at this URL with a revised date.

## Contact

Questions? Contact: [variospeed67@gmail.com](mailto:variospeed67@gmail.com)

---

# Politique de confidentialité — Speed Vario (Français)

*Dernière mise à jour : 21 octobre 2026*

## Aperçu

Speed Vario (« l'app ») est une application iPhone et Apple Watch de mesure de vitesse et d'altitude par GPS. Votre vie privée est importante. Cette politique explique quelles données sont utilisées, comment elles sont traitées et protégées.

Speed Vario fonctionne **sans compte, sans analytique, sans publicité et sans traceur tiers**. Vos enregistrements restent sur votre appareil — et, si vous activez la sauvegarde iCloud, dans **votre propre espace iCloud privé**, auquel le développeur n'a aucun accès. Il n'existe aucun serveur du développeur qui reçoive vos données (sauf si vous activez le partage en direct, plus bas) : les seuls fichiers que publie le développeur sont des données cartographiques statiques (noms de lieux, voir plus bas), servies par GitHub Pages.

## Données utilisées

- **Localisation (GPS)** — La position en temps réel et en arrière‑plan sert exclusivement à calculer la vitesse, l'altitude et le cap, et à enregistrer votre trajet. Les données de trace sont stockées localement sur votre appareil.
- **Capteurs de mouvement** — Le baromètre et l'accéléromètre améliorent la précision de l'altitude et de la vitesse verticale. Ces données sont traitées sur l'appareil et ne sont pas stockées séparément.
- **Capteurs d'eau (Apple Watch Ultra, mode Eau)** — Pendant un enregistrement en mode Eau, les capteurs de profondeur et de température de l'eau de la montre rapportent l'état d'immersion, la profondeur et la température. Contrairement aux données de mouvement ci‑dessus, ces mesures *sont* enregistrées avec la session, au même titre que la vitesse ou l'altitude. Elles sont mesurées et stockées sur votre appareil, et ne sont jamais transmises.
- **Données de santé (fréquence cardiaque et énergie active)** — Lors d'un enregistrement avec une Apple Watch appairée, elles sont lues depuis Apple Santé (HealthKit) pour être affichées en direct et enregistrées avec la session. Voir « Données de santé » ci‑dessous.

## Données de santé (HealthKit)

Lors d'un enregistrement avec une Apple Watch appairée, Speed Vario lit votre **fréquence cardiaque** et votre **énergie active** depuis Apple HealthKit pour les afficher en direct et les enregistrer avec la session sur votre appareil.

Si vous activez « Enregistrer dans Apple Santé » (Réglages → activé par défaut), Speed Vario **écrit aussi votre activité terminée dans Apple Santé sous forme d'entraînement**, avec le tracé GPS, la distance, la durée, le dénivelé positif, l'énergie active et la fréquence cardiaque moyenne. Vous pouvez le désactiver à tout moment dans les Réglages, et révoquer l'accès HealthKit à tout moment dans l'app Santé ou les Réglages iOS. Les données de santé sont uniquement lues depuis / écrites dans Apple Santé ; elles ne sont jamais envoyées à un serveur du développeur (seule exception : le partage en direct, si vous le démarrez — la fréquence cardiaque voyage alors **chiffrée**, voir « Partage en direct »), jamais partagées à des fins publicitaires, et **jamais stockées dans iCloud par l'app** — y compris lorsque la sauvegarde iCloud est activée, où la fréquence cardiaque et l'énergie active sont délibérément exclues de ce qui est envoyé (voir « Sauvegarde iCloud » ci‑dessous). Supprimer une session supprime ses données de santé de la base locale de l'app.

## Sauvegarde et synchronisation iCloud (optionnelles, désactivées par défaut)

Speed Vario peut copier vos sorties enregistrées dans **votre propre base iCloud privée**, pour qu'un iPhone perdu, cassé ou remplacé n'emporte pas votre historique avec lui. La fonction est **désactivée tant que vous ne l'activez pas**, soit depuis la proposition affichée une seule fois après quelques enregistrements, soit à tout moment dans Réglages → Données → Sauvegarde iCloud. Deux interrupteurs distincts :

- **Sauvegarder dans iCloud** — chaque sortie est envoyée au fil de son enregistrement. Supprimer une sortie sur votre iPhone ne supprime **pas** la copie iCloud ; c'est précisément ce qui permet de la récupérer. La restauration est une action explicite (« Restaurer depuis iCloud »).
- **Synchroniser mes appareils** — en plus, les sorties sont téléchargées automatiquement sur les autres appareils connectés au même compte iCloud, et une sortie que vous supprimez volontairement l'est aussi sur ces appareils. La suppression automatique par durée de conservation n'est **jamais** propagée : c'est une règle de ménage propre à chaque appareil, pas une décision concernant cette sortie.

**Où vont les données.** Dans la **base privée de votre propre compte iCloud**, via CloudKit d'Apple. Elles comptent sur votre propre stockage iCloud. Le développeur n'y a aucun accès, ne peut pas en dresser la liste et ne peut pas les lire. Aucun serveur exploité par le développeur n'intervient à aucun moment, et il n'y a aucun compte à créer — votre compte Apple est la seule identité utilisée, par Apple, pas par nous.

**Ce qui est envoyé :** le tracé GPS (coordonnées, altitude, vitesse, vitesse verticale, cap), l'altitude barométrique, la cadence et le nombre de pas (issus des capteurs de mouvement de l'appareil), les segments, le nom et les statistiques de la séance, les noms de lieux résolus, et — en mode Eau avec une Apple Watch Ultra — la température de l'eau et la profondeur.

**Ce qui n'est jamais envoyé :** votre **fréquence cardiaque** et votre **énergie active**. Elles proviennent d'Apple HealthKit, et les directives de revue de l'App Store d'Apple (5.1.3) interdisent de stocker des données de santé personnelles dans iCloud. Elles sont retirées de tout ce que l'app envoie, y compris de la copie d'origine conservée pour les séances que vous avez éditées. Elles restent sur l'appareil et dans Apple Santé. Après la restauration d'une séance sur un autre appareil, l'app relit la fréquence cardiaque et l'énergie active **dans Apple Santé** sur la fenêtre temporelle de cette séance — Apple Santé dispose de sa propre synchronisation chiffrée de bout en bout — de sorte que la courbe est reconstituée sans que ces données n'aient jamais transité par le stockage iCloud de l'app.

**Désactiver, et effacer.** Désactiver la fonction interrompt immédiatement tout envoi ; la copie déjà présente dans iCloud est laissée intacte. Réglages → Données → Sauvegarde iCloud → Gérer la copie iCloud dresse la liste de tout ce qui s'y trouve et propose **Effacer la copie iCloud**, qui la supprime définitivement. Supprimer l'app, ou désactiver iCloud Drive pour Speed Vario dans les Réglages iOS, interrompt également tout envoi ultérieur.

## Partage en direct (facultatif, désactivé par défaut)

Le partage en direct permet à la personne de votre choix de suivre votre sortie sur une carte, en temps réel, depuis une page web. Il est **désactivé par défaut** : rien n'est créé ni envoyé tant que vous n'avez pas lu l'avis et touché « Démarrer le partage ». Vous pouvez l'arrêter à tout moment (un bouton Arrêter rouge reste toujours à portée, sur l'iPhone comme sur l'Apple Watch), et il s'arrête aussi avec votre enregistrement. C'est la **seule** fonction qui envoie vos données vers un serveur choisi par le développeur ; elle est donc décrite ici en détail.

**Ce qui est envoyé.** Environ toutes les 15 secondes (30 secondes sous 30 % de batterie ; le partage s'arrête sous 10 %) : position, altitude, vitesse, vitesse verticale, distance, dénivelé positif et négatif, cap, cadence et pas quand ils sont mesurés, hauteur sol quand elle est disponible, niveau de batterie, et le nom de la sortie si vous en avez saisi un. **La fréquence cardiaque n'est envoyée que si vous activez l'option distincte « Partager ma fréquence cardiaque »** (désactivée par défaut) ; si elle est désactivée, aucune fréquence cardiaque n'est jamais incluse. La fréquence cardiaque est une donnée de santé : elle ne voyage que dans le flux chiffré, n'est jamais utilisée à des fins publicitaires et n'est jamais écrite dans iCloud.

**Chiffrement de bout en bout.** Chaque point est chiffré **sur votre appareil** (AES-256-GCM) avant de partir. La clé est créée pour ce seul partage et n'existe que dans le lien que vous partagez (dans la partie après le « # », que les navigateurs n'envoient à aucun serveur) et dans son QR code. Le développeur, Google et l'hébergeur ne reçoivent que des octets chiffrés et **ne peuvent lire ni votre position, ni votre fréquence cardiaque, ni le nom de votre sortie**. Le navigateur du spectateur déchiffre les données localement.

**Ce que le serveur peut quand même voir, parce que le chiffrement ne peut pas le cacher :** qu'un partage existe, quand et à quel rythme des données sont envoyées, l'heure de début et de fin, le nombre de points, la taille des messages (constante exprès), et les adresses IP de vos appareils et des personnes qui ouvrent le lien (une zone approximative, comme pour toute requête web). Un compte Firebase anonyme est créé par partage ; il n'est lié ni à votre nom, ni à votre identifiant Apple, ni à un autre partage.

**Qui traite les données.** Un projet Google Firebase exploité par le développeur (Realtime Database, Authentication avec comptes anonymes, et Hosting pour la page du spectateur à speedvario.web.app) ; Google agit comme sous-traitant. L'app lui parle par de simples requêtes HTTPS et ne contient aucun SDK Google ni Firebase. La page du spectateur charge des tuiles de carte d'OpenFreeMap et des tuiles de relief d'AWS Terrain Tiles, qui voient la zone de carte regardée. La page ne contient ni analytique, ni cookie, ni publicité ; elle ne garde le lien que dans l'onglet du navigateur (stockage de session) et retire la clé de la barre d'adresse dès qu'elle l'a lue.

**Combien de temps.** Le lien cesse de fonctionner 2 heures après la fin de votre enregistrement (la trace finale reste visible pendant ce temps) et ne dure jamais plus de 24 heures, quoi qu'il arrive. L'app efface ensuite les données du serveur au lancement suivant. Si vous reprenez l'enregistrement dans les 10 minutes, le même lien continue.

**Qui peut voir.** Quiconque possède le lien COMPLET peut lire la sortie jusqu'à son expiration : ne le partagez qu'avec des personnes de confiance. Arrêter le partage met fin au lien pour tout le monde.

## Utilisation du réseau

Speed Vario fonctionne hors ligne pour ses fonctions principales (affichage en direct et enregistrement). La détection des pays de vos traces est réalisée **entièrement sur l'appareil** (sans réseau). Quelques fonctions **optionnelles** envoient les coordonnées concernées à des services tiers, uniquement lorsque vous les utilisez :

- **Cartes, relief 3D et vidéo de survol satellite** utilisent Apple **MapKit**, qui envoie la position à Apple pour récupérer l'imagerie et l'élévation, selon la politique de confidentialité d'Apple. Sans connexion, l'app bascule sur un **fond de carte embarqué** (données Natural Earth, domaine public) : traits de côte, lacs, fleuves, glaciers, zones urbaines, grands axes, villes et aéroports. Ce repli ne demande aucune connexion et n'envoie rien nulle part.
- **Noms de lieux hors ligne** — le fond de carte embarqué nomme villes, villages, sommets et cols à partir des données **OpenStreetMap**. Les villes et les sommets connus sont embarqués dans l'app. Les villages, hameaux et autres sommets et cols de la région où vous vous trouvez sont téléchargés **à l'avance, tant que vous avez une connexion**, pour que la carte puisse les nommer une fois la connexion perdue : l'app demande les fichiers des carrés de 1° (environ 100 km) autour de votre position à **GitHub Pages** (thmaed.github.io), où ils sont publiés sous forme de fichiers statiques. Seule l'adresse de chaque carré est demandée — jamais votre position précise, vos traces ni aucun identifiant — même si, comme pour toute requête web, GitHub voit votre adresse IP. Les fichiers restent sur votre appareil et sont rafraîchis tous les quelques mois.
- **Noms de lieux** — les noms de stations / remontées de ski et d'aérodromes de départ/arrivée sont recherchés via **OpenStreetMap** (API Overpass). Seules les coordonnées interrogées sont envoyées ; le résultat est mis en cache sur votre appareil pour ne lancer la recherche qu'une fois.
- **Tracé d'itinéraire** — quand vous tracez un itinéraire sur la carte, les sentiers et chemins de la zone affichée sont téléchargés depuis **OpenStreetMap** (API Overpass) pour que le tracé puisse les suivre. Seul le rectangle de carte affiché est envoyé, jamais votre position ni l'itinéraire ; les sentiers sont gardés 30 jours sur votre appareil et le chemin est calculé entièrement sur votre appareil. En voiture — et à pied quand OpenStreetMap ne répond pas — le chemin entre deux points que vous avez posés est demandé à Apple (itinéraires **MapKit**) : ces deux points sont envoyés à Apple, selon la politique de confidentialité d'Apple.
- **Remontées mécaniques** — à ski, la hauteur sol ne s'affiche que sur un télésiège, une télécabine ou un téléphérique. Pour savoir où ils se trouvent, l'app demande à **OpenStreetMap** (API Overpass) les remontées situées à une dizaine de kilomètres de votre position, une fois par zone ; rien d'autre n'est envoyé, et la réponse est gardée sur votre appareil.
- **Altitude du relief** — le dénivelé d'un itinéraire tracé, le relief 3D, la vidéo de survol et la **hauteur sol** lisent l'altitude dans les **AWS Terrain Tiles** ouvertes (données ouvertes d'Amazon Web Services), avec **OpenTopoData** (opentopodata.org, données SRTM ouvertes) en secours pour certaines vues. Seules les tuiles ou les points couvrant la zone sont demandés. Pour la hauteur sol, les tuiles autour de votre position sont chargées quand vous armez la détection du décollage ou démarrez un enregistrement, et vous pouvez télécharger une zone à l'avance depuis Réglages → Relief hors ligne. Quand l'Apple Watch enregistre, elle demande les mêmes tuiles et les mêmes remontées pour sa propre position, par la connexion de l'iPhone ou la sienne. Les tuiles restent sur l'appareil (jusqu'à 250 Mo sur l'iPhone, 60 Mo sur la montre ; les moins utilisées partent en premier) et s'effacent depuis le même écran.
- **Aérodromes et pistes** — en mode Aviation, l'app nomme les terrains d'où vous avez décollé, où vous vous êtes posé ou que vous avez touchés, ainsi que la piste utilisée, à partir d'une **base embarquée dans l'app** (dérivée des données OurAirports, domaine public). Elle est en lecture seule et interrogée entièrement sur votre appareil : identifier un terrain n'envoie rien nulle part, et le vol auquel il appartient n'est jamais transmis.

Aucune autre donnée n'est transmise. Il n'y a pas de serveur du développeur ; les seules données qui quittent votre appareil vers un service choisi par le développeur relèvent du partage en direct, si vous le démarrez — chiffrées, et illisibles par le développeur.

## Données que nous ne collectons PAS

- Aucune information personnelle (nom, e‑mail, compte).
- Aucun service d'analytique, SDK publicitaire ou traceur tiers.
- Aucune donnée envoyée ou stockée sur un serveur exploité par le développeur. (La sauvegarde iCloud, lorsque vous l'activez, stocke les données dans *votre* compte iCloud — pas celui du développeur, et il n'y a pas accès.)
- Aucune donnée vendue ou partagée à des fins marketing.

## Stockage des données

Les enregistrements de sessions (points de trace, vitesse, altitude, et — avec une Apple Watch — fréquence cardiaque, énergie active, et en mode Eau la profondeur et la température de l'eau) sont stockés dans la base de données SwiftData locale sur votre appareil. Si vous activez la sauvegarde iCloud, une copie de chaque sortie **privée de la fréquence cardiaque et de l'énergie active** est également stockée dans votre propre base iCloud privée, comme décrit plus haut ; la fonction désactivée — son état par défaut — la base locale est le seul endroit où elles existent. Les fichiers exportés (GPX, CSV, KMZ, FIT, IGC, archive d'historique .zip et vidéos de survol) sont écrits dans le répertoire temporaire du système, ou partagés via la feuille de partage iOS vers une destination que vous choisissez. Les copies laissées dans le stockage temporaire sont supprimées automatiquement au lancement suivant de l'app, et peuvent être effacées à tout moment depuis Réglages → Cache.

Si vous activez **Enregistrer les données brutes** (Réglages → Données → Données brutes — désactivé par défaut, destinée au diagnostic du comportement des capteurs), l'app écrit en plus des fichiers CSV de mesures brutes, coordonnées précises comprises, dans son propre dossier Documents. Lorsqu'un enregistrement Apple Watch est concerné, la montre envoie son propre fichier à l'iPhone par la liaison directe. Ces fichiers ne quittent jamais votre appareil sauf si vous les exportez vous‑même ; ceux des 30 dernières sorties sont conservés, et ils peuvent être exportés ou supprimés depuis le même écran. Les trajets en ascenseur et en montagnes russes (modes expérimentaux) gardent toujours leurs mesures de mouvement, 30 jours, pour pouvoir être recalculés ; elles comprennent les quelques positions GPS du trajet et restent sur votre appareil.

## Conservation et suppression

Les sessions sont automatiquement supprimées après la période de rétention définie dans les Réglages (7 jours, 30 jours, 3 mois, 6 mois, 1 an, ou Illimité ; 30 jours par défaut). Vous pouvez la modifier à tout moment dans Réglages → Historique, et supprimer manuellement toute session depuis l'onglet Historique. L'historique GPS est exclu des sauvegardes iTunes / Finder non chiffrées. Les données du partage en direct sont conservées 24 h au plus, et 2 h après la fin de la sortie ; l'app les efface du serveur au lancement suivant, et vous pouvez l'arrêter à tout moment. La désinstallation de l'app supprime définitivement toutes les données stockées sur l'appareil ; si la sauvegarde iCloud était activée, la copie présente dans votre compte iCloud subsiste jusqu'à ce que vous l'effaciez (Réglages → Données → Sauvegarde iCloud → Gérer la copie iCloud → Effacer la copie iCloud) ou que vous la supprimiez de votre stockage iCloud.

## Enfants

L'app ne cible pas les enfants de moins de 13 ans et ne collecte pas sciemment leurs données.

## Modifications de cette politique

En cas de changement, la version mise à jour sera publiée à cette URL avec une date révisée.

## Contact

Questions ? Contact : [variospeed67@gmail.com](mailto:variospeed67@gmail.com)

---

*Speed Vario — © 2026. Tous droits réservés.*
