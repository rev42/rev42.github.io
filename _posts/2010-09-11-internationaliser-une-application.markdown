---
layout: post
title:  "Internationaliser une application"
date:   2010-09-11 07:00:00
categories: localisation
tags: internalisation, localisation, i18n
---

L'internationalisation (i18n) correspond à toutes les techniques utilisables permettant de gérer plusieurs langues et
conventions culturelles au sein d'une application.
L'i18n est principalement exécutée par des personnes techniques (programmeurs) qui adaptent leur code/outil afin de
faciliter l'intégration de langues supplémentaires (voir paragraphe Principes de base de l'i18n d'une application).
La conception d'une application doit rapidement prendre en compte l'aspect internationalisation (i18n). Plus l'i18n
intervient tôt dans la conception, plus il sera facile de la localiser par la suite.


## Différence entre Internationalisation et Localisation :
L'internationalisation d'une application doit permettre de localiser cette application sans effort particulier côté
programmation.
Voici quelques exemples qui éclaircissent la différence entre ces 3 termes (internationalisation, localisation et
traduction) :

Imaginons un écran affichant les informations relatives à un circuit de course automobile.

En version américaine :
<table>
    <tr>
        <th>Race Date</th>
        <td>29 may 2009</td>
    </tr>
    <tr>
        <th>Number of laps</th>
        <td>45</td>
    </tr>
    <tr>
        <th>Circuit length</th>
        <td>3,30 miles</td>
    </tr>
    <tr>
        <th>Race distance</th>
        <td>191,12 miles</td>
    </tr>
    <tr>
        <th>Lap Record</th>
        <td>1:34.105 - J Button (2001)</td>
    </tr>
</table>

L'internationalisation du programme pour l'Europe devra permettre de convertir les distances dans le système métrique
mais également de changer le séparateur de décimales (ex : 3.30 miles doit être converti en 5,30 kilomètres, 1:34.105
doit s'afficher 1'34"105 en français...).

L'étape de localisation sera de s'assurer que tous les changements liés à la région cible s'affiche convenablement à
l'écran (peut-être faudra-t-il adapter la taille de la boite de dialogue ?). Il faudra également vérifier que ces
conversions fonctionnent dans toutes les langues cibles du programme (qu'en est-il du format de temps en polonais,
tchèque ou italien ?, quel est leur séparateur de décimale ?).

La traduction va fournir le texte traduit.


## Intérêt de l'internationalisation d'une application :

  * Economique : une application localisée améliore les ventes dans les pays concernés (un jeu vidéo en anglais intégrale
aura moins de succès qu'une version anglais sous-titrée qui, elle, aura moins de succès que sa version localisée intégrale).
  * Image de l'entreprise : une société qui localise ses applications améliorera son image auprès de son public et touchera
un public plus large.
  * Juridique : en France, il existe une loi obligeant les applications à être traduites en français
    [Loi Toubon](http://fr.wikipedia.org/wiki/Loi_Toubon).


## Principes de base de l'internationalisation d'une application :
  * Se poser la question du marché cible (pays européens et anglo-saxons seulement ? pays asiatiques ? pays du monde arabe
?). L'impact peut aller d'une simple localisation (traduction, adaptation) pour les pays européens à une localisation
plus pointue comme, par exemple, en arabe (écriture de droite à gauche) ou en japonais (écriture syllabaire). L'effort
d'internationalisation ne sera pas le même et n'aura pas le même coût financier.

  * Prendre en compte au plus tôt l'i18n facilitera sa l10n (définir rapidement le référentiel de localisation pour chaque
pays : format de date/heure, ordre alphabétique, système monétaire...).
Exemple : comment formater les nombres ? la réponse sera : 9,000.00 (format US) - 9.000,00 (format français) /
123,456,789.00 (US) - 12,34,56,789.00 (Inde)
Comment trier les chaines de caractères par ordre alphabétique ? : il faut définir l'ordre alphabétique pour chaque
langue (en allemand, ä vient après a - en suédois, ä vient après z).

  * Faire un code le plus neutre possible au niveau localisation (pas de messages en dur dans le code, prise en compte du
référentiel de localisation).

  * Séparer le cœur de l'application des données localisables.

  * Regrouper les données localisées afin d'en faciliter l'extraction, le traitement et l'importation.
Exemple : il est intéressant d'avoir un répertoire "Audio" puis des sous-répertoires par langue "FRA", "SPA", "ITA"...
De même pour le texte, il faut regrouper autant que possible le texte de l'application dans un seul fichier par langue :
 il sera plus simple par la suite de le localiser (envoi du fichier anglais aux traducteurs), de remplacer les versions
 localisées (une nouvelle version/correction du fichier se fera par un simple copier/coller).

  * Préparer les écrans de manière à laisser plus de place aux textes localisés. En effet, en moyenne, le texte localisé
prend 20 à 25% plus de place que le texte anglais.
Exemple : le mot "buy" en anglais se traduit par "acheter" en français (+4 caractères), "comprar" (+4 caractères) en
espagnol. Le mot "ranking" => "classement" en français (+3 caractères), "clasificación" en espagnol (+3 caractères).

Souvent l'équipe de développement demande d'utiliser des abréviations ("cl." pour "classement") mais cela impacte
directement l'expérience utilisateur : une application comportant de nombreuses abréviations est difficile à lire, à
comprendre et impacte directement la qualité du produit.

- Utiliser une police de caractères supportant toutes les langues à localiser (attention aux licences d'utilisation).
- Utiliser un encodage de données adapté : privilégier l'UTF-8 (sans BOM).
- Eviter la concaténation de mots à partir de plusieurs variables. Essayer autant que possible de créer un identifiant
par phrase.