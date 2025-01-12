---
nav_title: 10 janvier 2023
page_order: 2
noindex: true
page_type: update
description: "Cet article contient les notes de version du 10/01/2023."
---

# Version du 10 janvier 2023

## Composant de mise à jour de l’utilisateur pour Canvas Flow

Le composant de [mise à jour de l’utilisateur]({{site.baseurl}}/user_guide/engagement_tools/canvas/canvas_components/user_update/) vous permet de mettre à jour les attributs, événements et achats d’un utilisateur dans un éditeur JSON. Il n’est donc pas nécessaire d’inclure des informations sensibles, par exemple des clés API. 

## Mettre en place des groupes d’abonnement par API

Lorsque vous créez de nouveaux utilisateurs au moyen de l’endpoint [/users/track]({{site.baseurl}}/api/endpoints/user_data/post_user_track/), vous pouvez définir des groupes d'abonnement dans l’objet attributs d’utilisateur, ce qui vous permet de créer un utilisateur et de définir l’état du groupe d’abonnement dans un seul appel API.

## Accès anticipé au tableau de bord des conversions

Le [tableau de bord de conversions]({{site.baseurl}}/user_guide/data_and_analytics/your_analytics_dashboards/conversions_dashboard/) vous permet d’analyser les conversions entre les campagnes, les Canvas et les canaux en utilisant des méthodes d’attribution différentes. Vous pouvez suivre ces méthodes d’attribution spécifiquement :

- **Conversions d’ouverture :** Les conversions qui se sont produites après qu’un utilisateur a ouvert le message
- **Conversions de clic :** Les conversions qui se sont produites après qu’un utilisateur a cliqué le message
- **Conversions reçues :** Les conversions qui se sont produites après qu’un utilisateur a reçu le message
- **Conversions au dernier clic :** Les conversions qui se sont produites après qu’un utilisateur a cliqué le message, si ce message était le plus récent cliqué par l’utilisateur (cette fonctionnalité est actuellement testée par un petit groupe de clients en accès anticipé)

Cette fonctionnalité est actuellement disponible en accès anticipé. Si vous souhaitez participer à l’accès anticipé, contactez votre gestionnaire du succès des clients.

## Événements de sortie Canvas pour Currents de Braze

Vous pouvez suivre le moment où vos utilisateurs quittent un Canvas en effectuant un événement ou en faisant correspondre une audience. Consultez la section [Événements d’engagement de message]({{site.baseurl}}/user_guide/data_and_analytics/braze_currents/event_glossary/message_engagement_events/) dans le Glossaire d’événements Currents pour plus d’informations.

 ## Mises à jour SDK

Les mises à jour SDK suivantes ont été publiées. Les dernières mises à jour sont répertoriées ci-dessous ; vous pouvez trouver toutes les autres mises à jour en consultant les journaux de modifications SDK correspondants.

- [SDK Web 4.5.1](https://github.com/braze-inc/braze-web-sdk/blob/master/CHANGELOG.md)
- [AppboyKit iOS SDK 4.5.2](https://github.com/Appboy/appboy-ios-sdk/releases/tag/4.5.2)
- [SDK Swift 5.8.0–5.8.1](https://github.com/braze-inc/braze-swift-sdk/blob/main/CHANGELOG.md#580)
	- Renomme la classe `BrazeLocation` en `BrazeLocationProvider` pour éviter de mettre dans l’ombre le module du même nom.
- [SDK Flutter 3.0.1](https://pub.dev/packages/braze_plugin/changelog)
- [SDK Android 24.0.0](https://github.com/Appboy/appboy-android-sdk/blob/master/CHANGELOG.md)
	- La fonctionnalité de positionnement et de geofence a été déplacée dans un nouveau module appelé `com.braze:android-sdk-location`.
	- Les classes et les fichiers Appboy ont tous été déplacés vers Braze.
	- Modification du comportement par défaut de `DefaultContentCardsUpdateHandler` pour utiliser la date de création au lieu de la date de dernière mise à jour lors du tri des cartes de contenu.
	- BrazeUser.setFacebookData() et BrazeUser.setTwitterData() supprimés.