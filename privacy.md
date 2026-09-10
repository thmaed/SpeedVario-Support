---
title: Privacy Policy
---

*[Français](#politique-de-confidentialité--speed-vario-français) · [Support](./)*

# Privacy Policy — Speed Vario

*Last updated: September 2026*

## Overview

Speed Vario ("the app") is a GPS speed and altitude logging application for iPhone and Apple Watch. Your privacy is important. This policy explains what data is used, how it is processed, and how it is protected.

Speed Vario has **no account, no analytics, no advertising and no third‑party trackers**. Your recordings live on your device — and, if you switch on iCloud Backup, in **your own private iCloud space**, which the developer cannot access. There is no developer server of any kind.

## Data used

- **Location (GPS)** — Real‑time and background location is used exclusively to compute speed, altitude and heading, and to record your session route. Track data is stored locally on your device.
- **Motion sensors** — The barometer and accelerometer are used to improve altitude and vertical‑speed accuracy. This data is processed on‑device and is not stored separately.
- **Water sensors (Apple Watch Ultra, Water mode)** — While recording in Water mode, the watch's depth and water‑temperature sensors report submersion state, depth and water temperature. Unlike the motion data above, these readings *are* saved with the session, exactly like speed or altitude. They are measured and stored on your device and are never transmitted.
- **Health data (heart rate & active energy)** — When you record with a paired Apple Watch, these are read from Apple Health (HealthKit) to show them live and save them with the session. See "Health data" below.

## Health data (HealthKit)

When you record an activity with a paired Apple Watch, Speed Vario reads your **heart rate** and **active energy** from Apple HealthKit so they can be shown live and stored alongside the session on your device.

If you enable "Save to Apple Health" (Settings → on by default), Speed Vario also **writes your completed activity to Apple Health as a workout**, including the GPS route, distance, duration, elevation gain, active energy and average heart rate. You can disable this at any time in Settings, and you can revoke HealthKit access at any time in the Apple Health app or in iOS Settings. Health data is read from / written to Apple Health only; it is never sent to any server controlled by the developer, never shared for advertising, and **never stored in iCloud by the app** — including when iCloud Backup is switched on, where heart rate and active energy are deliberately excluded from what is uploaded (see "iCloud Backup" below). Deleting a recorded session deletes its health data from the app's own database.

## iCloud Backup and sync (optional, off by default)

Speed Vario can copy your recorded outings to **your own private iCloud database**, so that a lost, broken or replaced iPhone does not take your history with it. It is **off until you turn it on**, either from the one‑time prompt shown after a few recordings or at any time in Settings → Data → iCloud Backup. Two separate switches:

- **Back up to iCloud** — each outing is uploaded as it is recorded. Deleting an outing on your iPhone does **not** delete the iCloud copy; that is what lets you recover it. Restoring is an explicit action ("Restore from iCloud").
- **Sync my devices** — in addition, outings are downloaded automatically onto other devices signed in to the same iCloud account, and an outing you deliberately delete is deleted on those devices too. Automatic deletion by retention period is **never** propagated: it is a per‑device housekeeping rule, not a decision about that outing.

**Where the data goes.** Into the **private database of your own iCloud account**, using Apple's CloudKit. It counts against your own iCloud storage. The developer has no access to it, cannot list it, and cannot read it. There is no developer‑operated server involved at any point, and no account to create — your Apple Account is the only identity used, by Apple, not by us.

**What is uploaded:** the GPS track (coordinates, altitude, speed, vertical speed, heading), barometric altitude, cadence and step count (from the device's motion sensors), lap marks, session name and statistics, resolved place names, and — in Water mode with an Apple Watch Ultra — water temperature and depth.

**What is never uploaded:** your **heart rate** and **active energy**. These come from Apple HealthKit, and Apple's App Store Review Guidelines (5.1.3) prohibit storing personal health information in iCloud. They are stripped out of everything the app sends, including the pre‑edit snapshot kept for sessions you have trimmed. They remain on the device and in Apple Health. After restoring a session onto another device, the app reads heart rate and active energy back **from Apple Health** for that session's time window — Apple Health has its own end‑to‑end encrypted sync — so the chart is rebuilt without that data ever passing through the app's iCloud storage.

**Turning it off, and erasing it.** Switching the feature off stops all uploads immediately; the copy already in iCloud is left alone. Settings → Data → iCloud Backup → Manage iCloud copy lists everything held there and offers **Erase iCloud copy**, which permanently deletes all of it. Deleting the app, or turning off iCloud Drive for Speed Vario in iOS Settings, also stops any further upload.

## Network use

Speed Vario works offline for its core features (live readout and recording). Country detection for your tracks is performed **entirely on‑device** (no network). A few **optional** features send the relevant coordinates to third‑party services, and only when you use them:

- **Maps, 3D terrain and satellite fly‑through video** use Apple **MapKit**, which sends location to Apple to fetch map imagery and elevation, under Apple's privacy policy. With no network connection the app falls back to a **basemap bundled inside the app** (public‑domain Natural Earth data): coastlines, lakes, rivers, glaciers, urban areas, major roads, cities and airports. That fallback requires no connection and sends nothing anywhere.
- **Place names** — ski resort / lift names and departure/arrival aerodrome names are looked up from **OpenStreetMap** (Overpass API). Only the queried coordinates are sent; the result is cached on your device so the lookup runs once.
- **Aerodromes and runways** — in Aviation mode the app names the fields you took off from, landed at or touched, and the runway used, from a **database bundled inside the app** (derived from public-domain OurAirports data). It is read-only and queried entirely on your device: identifying an airfield sends nothing anywhere, and the flight it belongs to is never transmitted.

No other data is transmitted. There is no developer server, and no location or sensor data is uploaded to the developer.

## Data we do NOT collect

- No personal information (name, email, account).
- No analytics services, advertising SDKs or third‑party trackers.
- No data is uploaded to or stored on any server operated by the developer. (iCloud Backup, when you enable it, stores data in *your* iCloud account — not the developer's, and not accessible to the developer.)
- No data is sold or shared for marketing.

## Data storage

Session recordings (track points, speed, altitude, and — when recorded with an Apple Watch — heart rate, active energy, and in Water mode depth and water temperature) are stored in the local SwiftData database on your device. If you enable iCloud Backup, a copy of each outing **minus heart rate and active energy** is also stored in your own private iCloud database, as described above; with the feature off — its default state — the local database is the only place they exist. Exported files (GPX, CSV, KMZ, FIT, IGC, history archive .zip and fly‑through videos) are written to the system temporary directory, or shared via the iOS share sheet to a destination you choose. Copies left behind in temporary storage are deleted automatically the next time the app launches, and can be cleared at any moment from Settings → Cache.

If you switch on **Raw signal capture** (Settings → System — off by default, and intended for diagnosing sensor behaviour), the app additionally writes CSV files of raw sensor readings, including precise coordinates, into its own Documents folder. When an Apple Watch recording is involved it sends its own file to the iPhone over the direct Watch link. These files never leave your device unless you export them yourself; at most 20 are kept, and they can be exported or deleted from the same screen.

## Data retention and deletion

Sessions are automatically deleted after the retention period set in the app's Settings (7 days, 30 days, 3 months, 6 months, 1 year, or Unlimited; default 30 days). You can change this at any time in Settings → History, and you can delete any session manually from the History tab. GPS history is excluded from unencrypted iTunes / Finder backups. Deleting the app removes all data stored on the device permanently; if iCloud Backup was enabled, the copy in your iCloud account survives until you erase it (Settings → Data → iCloud Backup → Manage iCloud copy → Erase iCloud copy) or delete it from your iCloud storage.

## Children

The app does not target children under 13 and does not knowingly collect data from children.

## Changes to this policy

If this policy changes, the updated version will be posted at this URL with a revised date.

## Contact

Questions? Contact: [variospeed67@gmail.com](mailto:variospeed67@gmail.com)

---

# Politique de confidentialité — Speed Vario (Français)

*Dernière mise à jour : septembre 2026*

## Aperçu

Speed Vario (« l'app ») est une application iPhone et Apple Watch de mesure de vitesse et d'altitude par GPS. Votre vie privée est importante. Cette politique explique quelles données sont utilisées, comment elles sont traitées et protégées.

Speed Vario fonctionne **sans compte, sans analytique, sans publicité et sans traceur tiers**. Vos enregistrements restent sur votre appareil — et, si vous activez la sauvegarde iCloud, dans **votre propre espace iCloud privé**, auquel le développeur n'a aucun accès. Il n'existe aucun serveur du développeur, d'aucune sorte.

## Données utilisées

- **Localisation (GPS)** — La position en temps réel et en arrière‑plan sert exclusivement à calculer la vitesse, l'altitude et le cap, et à enregistrer votre trajet. Les données de trace sont stockées localement sur votre appareil.
- **Capteurs de mouvement** — Le baromètre et l'accéléromètre améliorent la précision de l'altitude et de la vitesse verticale. Ces données sont traitées sur l'appareil et ne sont pas stockées séparément.
- **Capteurs d'eau (Apple Watch Ultra, mode Eau)** — Pendant un enregistrement en mode Eau, les capteurs de profondeur et de température de l'eau de la montre rapportent l'état d'immersion, la profondeur et la température. Contrairement aux données de mouvement ci‑dessus, ces mesures *sont* enregistrées avec la session, au même titre que la vitesse ou l'altitude. Elles sont mesurées et stockées sur votre appareil, et ne sont jamais transmises.
- **Données de santé (fréquence cardiaque et énergie active)** — Lors d'un enregistrement avec une Apple Watch appairée, elles sont lues depuis Apple Santé (HealthKit) pour être affichées en direct et enregistrées avec la session. Voir « Données de santé » ci‑dessous.

## Données de santé (HealthKit)

Lors d'un enregistrement avec une Apple Watch appairée, Speed Vario lit votre **fréquence cardiaque** et votre **énergie active** depuis Apple HealthKit pour les afficher en direct et les enregistrer avec la session sur votre appareil.

Si vous activez « Enregistrer dans Apple Santé » (Réglages → activé par défaut), Speed Vario **écrit aussi votre activité terminée dans Apple Santé sous forme d'entraînement**, avec le tracé GPS, la distance, la durée, le dénivelé positif, l'énergie active et la fréquence cardiaque moyenne. Vous pouvez le désactiver à tout moment dans les Réglages, et révoquer l'accès HealthKit à tout moment dans l'app Santé ou les Réglages iOS. Les données de santé sont uniquement lues depuis / écrites dans Apple Santé ; elles ne sont jamais envoyées à un serveur du développeur, jamais partagées à des fins publicitaires, et **jamais stockées dans iCloud par l'app** — y compris lorsque la sauvegarde iCloud est activée, où la fréquence cardiaque et l'énergie active sont délibérément exclues de ce qui est envoyé (voir « Sauvegarde iCloud » ci‑dessous). Supprimer une session supprime ses données de santé de la base locale de l'app.

## Sauvegarde et synchronisation iCloud (optionnelles, désactivées par défaut)

Speed Vario peut copier vos sorties enregistrées dans **votre propre base iCloud privée**, pour qu'un iPhone perdu, cassé ou remplacé n'emporte pas votre historique avec lui. La fonction est **désactivée tant que vous ne l'activez pas**, soit depuis la proposition affichée une seule fois après quelques enregistrements, soit à tout moment dans Réglages → Données → Sauvegarde iCloud. Deux interrupteurs distincts :

- **Sauvegarder dans iCloud** — chaque sortie est envoyée au fil de son enregistrement. Supprimer une sortie sur votre iPhone ne supprime **pas** la copie iCloud ; c'est précisément ce qui permet de la récupérer. La restauration est une action explicite (« Restaurer depuis iCloud »).
- **Synchroniser mes appareils** — en plus, les sorties sont téléchargées automatiquement sur les autres appareils connectés au même compte iCloud, et une sortie que vous supprimez volontairement l'est aussi sur ces appareils. La suppression automatique par durée de conservation n'est **jamais** propagée : c'est une règle de ménage propre à chaque appareil, pas une décision concernant cette sortie.

**Où vont les données.** Dans la **base privée de votre propre compte iCloud**, via CloudKit d'Apple. Elles comptent sur votre propre stockage iCloud. Le développeur n'y a aucun accès, ne peut pas en dresser la liste et ne peut pas les lire. Aucun serveur exploité par le développeur n'intervient à aucun moment, et il n'y a aucun compte à créer — votre compte Apple est la seule identité utilisée, par Apple, pas par nous.

**Ce qui est envoyé :** le tracé GPS (coordonnées, altitude, vitesse, vitesse verticale, cap), l'altitude barométrique, la cadence et le nombre de pas (issus des capteurs de mouvement de l'appareil), les segments, le nom et les statistiques de la séance, les noms de lieux résolus, et — en mode Eau avec une Apple Watch Ultra — la température de l'eau et la profondeur.

**Ce qui n'est jamais envoyé :** votre **fréquence cardiaque** et votre **énergie active**. Elles proviennent d'Apple HealthKit, et les directives de revue de l'App Store d'Apple (5.1.3) interdisent de stocker des données de santé personnelles dans iCloud. Elles sont retirées de tout ce que l'app envoie, y compris de la copie d'origine conservée pour les séances que vous avez éditées. Elles restent sur l'appareil et dans Apple Santé. Après la restauration d'une séance sur un autre appareil, l'app relit la fréquence cardiaque et l'énergie active **dans Apple Santé** sur la fenêtre temporelle de cette séance — Apple Santé dispose de sa propre synchronisation chiffrée de bout en bout — de sorte que la courbe est reconstituée sans que ces données n'aient jamais transité par le stockage iCloud de l'app.

**Désactiver, et effacer.** Désactiver la fonction interrompt immédiatement tout envoi ; la copie déjà présente dans iCloud est laissée intacte. Réglages → Données → Sauvegarde iCloud → Gérer la copie iCloud dresse la liste de tout ce qui s'y trouve et propose **Effacer la copie iCloud**, qui la supprime définitivement. Supprimer l'app, ou désactiver iCloud Drive pour Speed Vario dans les Réglages iOS, interrompt également tout envoi ultérieur.

## Utilisation du réseau

Speed Vario fonctionne hors ligne pour ses fonctions principales (affichage en direct et enregistrement). La détection des pays de vos traces est réalisée **entièrement sur l'appareil** (sans réseau). Quelques fonctions **optionnelles** envoient les coordonnées concernées à des services tiers, uniquement lorsque vous les utilisez :

- **Cartes, relief 3D et vidéo de survol satellite** utilisent Apple **MapKit**, qui envoie la position à Apple pour récupérer l'imagerie et l'élévation, selon la politique de confidentialité d'Apple. Sans connexion, l'app bascule sur un **fond de carte embarqué** (données Natural Earth, domaine public) : traits de côte, lacs, fleuves, glaciers, zones urbaines, grands axes, villes et aéroports. Ce repli ne demande aucune connexion et n'envoie rien nulle part.
- **Noms de lieux** — les noms de stations / remontées de ski et d'aérodromes de départ/arrivée sont recherchés via **OpenStreetMap** (API Overpass). Seules les coordonnées interrogées sont envoyées ; le résultat est mis en cache sur votre appareil pour ne lancer la recherche qu'une fois.
- **Aérodromes et pistes** — en mode Aviation, l'app nomme les terrains d'où vous avez décollé, où vous vous êtes posé ou que vous avez touchés, ainsi que la piste utilisée, à partir d'une **base embarquée dans l'app** (dérivée des données OurAirports, domaine public). Elle est en lecture seule et interrogée entièrement sur votre appareil : identifier un terrain n'envoie rien nulle part, et le vol auquel il appartient n'est jamais transmis.

Aucune autre donnée n'est transmise. Il n'y a pas de serveur du développeur, et aucune donnée de localisation ou de capteur n'est envoyée au développeur.

## Données que nous ne collectons PAS

- Aucune information personnelle (nom, e‑mail, compte).
- Aucun service d'analytique, SDK publicitaire ou traceur tiers.
- Aucune donnée envoyée ou stockée sur un serveur exploité par le développeur. (La sauvegarde iCloud, lorsque vous l'activez, stocke les données dans *votre* compte iCloud — pas celui du développeur, et il n'y a pas accès.)
- Aucune donnée vendue ou partagée à des fins marketing.

## Stockage des données

Les enregistrements de sessions (points de trace, vitesse, altitude, et — avec une Apple Watch — fréquence cardiaque, énergie active, et en mode Eau la profondeur et la température de l'eau) sont stockés dans la base de données SwiftData locale sur votre appareil. Si vous activez la sauvegarde iCloud, une copie de chaque sortie **privée de la fréquence cardiaque et de l'énergie active** est également stockée dans votre propre base iCloud privée, comme décrit plus haut ; la fonction désactivée — son état par défaut — la base locale est le seul endroit où elles existent. Les fichiers exportés (GPX, CSV, KMZ, FIT, IGC, archive d'historique .zip et vidéos de survol) sont écrits dans le répertoire temporaire du système, ou partagés via la feuille de partage iOS vers une destination que vous choisissez. Les copies laissées dans le stockage temporaire sont supprimées automatiquement au lancement suivant de l'app, et peuvent être effacées à tout moment depuis Réglages → Cache.

Si vous activez la **capture du signal brut** (Réglages → Système — désactivée par défaut, destinée au diagnostic du comportement des capteurs), l'app écrit en plus des fichiers CSV de mesures brutes, coordonnées précises comprises, dans son propre dossier Documents. Lorsqu'un enregistrement Apple Watch est concerné, la montre envoie son propre fichier à l'iPhone par la liaison directe. Ces fichiers ne quittent jamais votre appareil sauf si vous les exportez vous‑même ; 20 au maximum sont conservés, et ils peuvent être exportés ou supprimés depuis le même écran.

## Conservation et suppression

Les sessions sont automatiquement supprimées après la période de rétention définie dans les Réglages (7 jours, 30 jours, 3 mois, 6 mois, 1 an, ou Illimité ; 30 jours par défaut). Vous pouvez la modifier à tout moment dans Réglages → Historique, et supprimer manuellement toute session depuis l'onglet Historique. L'historique GPS est exclu des sauvegardes iTunes / Finder non chiffrées. La désinstallation de l'app supprime définitivement toutes les données stockées sur l'appareil ; si la sauvegarde iCloud était activée, la copie présente dans votre compte iCloud subsiste jusqu'à ce que vous l'effaciez (Réglages → Données → Sauvegarde iCloud → Gérer la copie iCloud → Effacer la copie iCloud) ou que vous la supprimiez de votre stockage iCloud.

## Enfants

L'app ne cible pas les enfants de moins de 13 ans et ne collecte pas sciemment leurs données.

## Modifications de cette politique

En cas de changement, la version mise à jour sera publiée à cette URL avec une date révisée.

## Contact

Questions ? Contact : [variospeed67@gmail.com](mailto:variospeed67@gmail.com)

---

*Speed Vario — © 2026. Tous droits réservés.*
