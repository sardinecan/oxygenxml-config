# MacOS Basic Config

## Logiciels 
### Navigateurs
- Firefox [https://www.mozilla.org/fr/firefox/new/](https://www.mozilla.org/fr/firefox/new/)
- Chrome [https://www.google.com/chrome/](https://www.google.com/chrome/)

### Éditeurs
- Webstorm [https://www.jetbrains.com/fr-fr/webstorm/](https://www.jetbrains.com/fr-fr/webstorm/)
- Visual Studio Code [https://code.visualstudio.com/](https://code.visualstudio.com/)
- OxygenXML [https://www.oxygenxml.com/](https://www.oxygenxml.com/)
    - dans Préférences/Éditeur/Formatage
        - cocher seulement : `détecter l'indentation à l'ouverture` ; `indenter avec Entrée` ; `activer Smart Enter`
        - Changer les valeurs de :
            - `largeur d'indentation` : `3`
            - `Longueur de ligne` : `10000`
    - dans Préférences/Éditeur/Formatage/XML :
        - cocher : `Conserver les lignes vides` ; `Conserver les sauts de ligne dans les attributs` ; `Indenter les éléments en ligne`
        - dans `Espacement des éléments/Conserver les espaces`, ajouter : `//p//*` ; `//head//*` ; `//dateline//*` ; `//signed//*` ; `//choice`


### Gestionnaire de Pacquets
- Homebrew [https://brew.sh/index_fr](https://brew.sh/index_fr)

### Traitement images
- Suite Affinity [https://affinity.serif.com/fr/](https://affinity.serif.com/fr/)
- Final Cut pro 

### Programmation et développement web
- oh-my-zsh [https://ohmyz.sh/#install](https://ohmyz.sh/#install)
    - installer thème `SolarizedDark` pour le terminal [https://ethanschoonover.com/solarized/](https://ethanschoonover.com/solarized/) | sur github perso #todo
    - 
- Git [https://git-scm.com/](https://git-scm.com/)
    - avec Homebrew 
        - `brew install git`
        - `git --version` #git est installé par défaut sur macOs
        - `which git` # permet de savoir qu'elle version est utilisée (par défaut celle de macOs)
        - `sudo mv /usr/bin/git /usr/bin/git-apple` | or | `brew link --overwrite git` # pour utiliser la dernière version téléchargée avec homebrew
- Github 
    - clé SSH [https://docs.github.com/en/authentication/connecting-to-github-with-ssh](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
        - générer un clé ssh et l'ajouter à ssh-agent
        - ajouter la nouvelle clé ssh au compte github
- NodeJS [https://nodejs.org/en/](https://nodejs.org/en/) (de préférence LTS)
- Apache Ant [https://ant.apache.org/](https://ant.apache.org/)
- Julia Lang [https://julialang.org/](https://julialang.org/)
- Python []()
    - avec Homebrew







