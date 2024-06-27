---
title: 'oxygenxml-config'
date: '2022-05-17'
author: 'jmorvan'
keywords: 'config ; dev ; editor ; xml'
---

# OxygenXML Config
[Oxygen XML](https://www.oxygenxml.com/)

Mes paramètres personnalisés sont stockés dans le fichier `globalSettings.xml` et les scénarios de transformation sont sauvegardés dans `transformation.scenarios` (repo [systemSetup](https://github.com/sardinecan/systemSetup/)).

Pour importer les paramètres et les scénarios : `options/(importer les options globales | importer les scénarios de transformation)` 

Pour une configuration manuelle :
- Formatage : 
    - `Préférences/Éditeur/Formatage` : 
	    - cocher seulement : `détecter l'indentation à l'ouverture` ; `indenter avec Entrée` ; `activer Smart Enter`
	    - changer les valeurs pour : `largeur d'indentation` : `3` et `Longueur de ligne` : `10000`
    - `Préférences/Éditeur/Formatage/XML` :
	    - cocher : `Conserver les lignes vides` ; `Conserver les sauts de ligne dans les attributs` ; `Indenter les éléments en ligne`
	    - ajouter `//p/*` ; `//head//*` ; `//dateline//*` ; `//signed//*` ; `//choice` à `Espacement des éléments/Conserver les espaces`
- Saxon 
    - `Préférences/XML/XSLT/FO/XQuery/XSLT/Saxon/Saxon HE/PE/EE`
	    - désélectionner `Étendre les attributs par défaut ("-expand")`
