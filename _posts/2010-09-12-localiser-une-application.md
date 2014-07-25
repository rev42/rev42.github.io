---
layout: post
title:  "Localiser une application"
date:   2010-09-12 07:00:00
categories: localisation
tags: localisation, l10n
---
La **localisation** (abrégé sous la forme l10n) est le **processus qui permet d'adapter un programme/document aux exigences du
 marché ciblé**.

Attention, le terme "adapter" est important. Il ne s'agit pas simplement de traduction car il faut également **prendre en
compte les différences culturelles** (séparateur décimal, format date et d'heure, disposition du clavier...).

L'étape de l10n arrive après celle de l'internationalisation (abrégé i18n). Pour obtenir une bonne l10n de l'application, il est impératif qu'il y ait
eu un effort d'i18n. J'ai d'ailleurs rédigé une courte [introduction à l'i18n]({% post_url 2010-09-11-internationaliser-une-application %}).


## Les grandes étapes de la localisation

### Définir une date de "gel" des données localisables (lockdown date)
Avant le lancement du processus de localisation, il est nécessaire d'identifier une date à partir de laquelle toutes
modifications sur les données localisables seront conservées.
Pour arriver à définir cette date, il est nécessaire de trouver un accord entre les différents acteurs (service
production, service localisation, service marketing). C'est un exercice assez intéressant où chaque service aura ses
arguments dans le but d'avancer ou de reculer cette date :
  * le marketing connait la **date de sortie du produit** (shipdate) et ne souhaite pas ou peu en changer.
  * La production a aussi en tête la date de sortie mais cherche également à faire le **meilleur produit possible** en
éliminant les erreurs ou incohérences dans le produit source, c'est pourquoi elle souhaite que cette date soit repoussée
 au plus près de la date de sortie du produit.
  * La l10n doit s'adapter et définir au mieux la date idéale à laquelle la modification des données localisables doit
être bloquée. Pour cela, elle prendra en compte le **nombre de mots à traduire**, les **marchés cibles**, la **complexité du produit**,
 les **précédentes réalisations** en terme de localisation du studio de développement/équipe de production...
Bien qu'une date "lockdown" soit définie, il y aura toujours des modifications faites au niveau de la langue source
(oublis, rectifications, corrections des fautes d'orthographe...).

Le but est de fixer une date raisonnable afin que chacun puisse travailler dans les meilleures conditions.

### Traquer toutes modifications sur les données localisables à partir de la date "lockdown".

En effet, à partir de cette date, toutes modifications va **impacter les équipes de localisation et de traduction**.
Une simple phrase modifiée ou ajoutée dans la langue source va demander sa traduction/relecture sur toutes les langues
cibles. l'exercice est encore plus complexe lorsqu'il s'agit d'audio ou vidéo, car il faudra éditer des fichiers plus
lourds et plus long à générer.
Il est impératif qu'un **système de "track"** performant soit mis en place afin d'importer/exporter les données, stocker les
 statistiques de traduction, connaitre les phrases traduites, en cours de traduction...

### Tester le produit et corriger les bugs

On pourrait se dire : à partir du moment où 100% des données localisables ont été traduites, tout est OK. C'est faux !
En effet, un produit localisé même par les meilleurs professionnels du secteur peut totalement se **décrédibiliser** aux yeux
du public s'il n'a pas été testé par des équipes spécialisées dans ce domaine.

La plupart du temps, **les traducteurs n'ont pas les écrans du programme sous les yeux**. Il leur faut donc être vigilant en
s'assurant de la **cohérence des termes** ("Tables" doit-il être traduit par "Tableau" ou "Classement" ?, "Update settings"
doit-il être traduit par "Mettre à jour les paramètres" ou "Mise à jour des paramètres" ?), du contexte ("Back"
signifie-t-il "Arrière" ou "Retour à l'écran précédent" ?) et de ce qui est traduisible ou non (faut-il traduire le
mot "Button" en "Bouton"  ?).

Pour réduire les coûts de traduction, les équipes de développement ont tendance à **réutiliser les mots** au sein d'un
programme dans plusieurs écrans différents (exemple : en anglais, le terme "Back" peut être indifféremment utilisé sur
un écran affichant  un lecteur musical affichant les termes "Back, Next, Play, Stop" et sur un écran permettant le
retour à l'écran précédent.). Lors de l'étape de traduction, ce mot a été traduit une seule fois (exemple : "Retour").
Cependant, en français, nous n'utilisons pas le terme "Retour" dans une lecteur musical, mais plutôt "Précédent". Il
existe donc **plusieurs traductions suivant le contexte**.

Toutes ces questions peuvent faire l'objet d'un échange entre l'équipe de production et de localisation mais il est plus
avantageux et rapide de faire tester le produit par des personnes natives du pays cible pendant la phase de localisation.
Ainsi, tous les problèmes de cohérence ou de contexte seront résolus. De plus, ces équipes assureront la relecture de
phrases/audio/vidéo modifiées, pourront effectuer des traductions urgentes...

**Localiser un programme** d'une culture à une autre demande non seulement des **compétences de traduction** mais également des
**connaissances culturelles de la langue et pays cible** (système de mesures, de temps, monnaie utilisée, termes péjoratifs
ou interdits, couleurs provocatrices dans certains pays...).

Pour obtenir un logiciel localisé, il faudra donc prendre en compte ses **aspects culturels** (localisation) et s'assurer
que le programme a été prévu pour les **gérer convenablement** (internationalisation).