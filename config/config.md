# MacOS Basic Config

## Polices de caractère
- IBM Plex [https://www.ibm.com/plex/specs/](https://www.ibm.com/plex/specs/)
    - Release depuis repo Github [https://github.com/IBM/plex/releases/latest](https://github.com/IBM/plex/releases/latest) (télécharger openType)
    - Repo Github [https://github.com/IBM/plex](https://github.com/IBM/plex)

## Logiciels 
### Navigateurs
- Firefox [https://www.mozilla.org/fr/firefox/new/](https://www.mozilla.org/fr/firefox/new/)
- Chrome [https://www.google.com/chrome/](https://www.google.com/chrome/)

### Éditeurs
- Webstorm [https://www.jetbrains.com/fr-fr/webstorm/](https://www.jetbrains.com/fr-fr/webstorm/)
    - changer la police pour `IBM Plex Mono`
    - la configuration de Webstorm est synchronisée sur le serveur jetbrain, pour l'activer : menu Webstorm/Settings/Settings Sync
        - cliquer sur `Enable Settings Sync`
        - dans la nouvelle fenêtre qui s'ouvre cliquer sur `Get Settings from Account`
- Visual Studio Code [https://code.visualstudio.com/](https://code.visualstudio.com/)
    - Activer la synchronisation des tags html/xml : 
        - Sur macOs : ⌘ + ⇧ + p / taper dans l'invite `settings.json` (user) puis ajouter dans le document `"editor.linkedEditing": true`
    - Changer la police pour `IBM Plex Mono`
    - la configuration de VS Code est synchronisée sur github, pour l'activer : 
        - cliquer sur la roue dentée en bas à gauche de la fenêtre VS Code puis sur activier la synchronisation des paramètres
        - sur l'invite suivante cliquer sur `sign in & turn on | se connecter` puis choisir `sign in with Github | se connecter avec Github`
        - choisir ensuite l'option `remplacer localement`
        - documentation [https://code.visualstudio.com/docs/editor/settings-sync](https://code.visualstudio.com/docs/editor/settings-sync)
- OxygenXML [https://www.oxygenxml.com/](https://www.oxygenxml.com/)
    - dans Préférences/Éditeur/Formatage
        - cocher seulement : `détecter l'indentation à l'ouverture` ; `indenter avec Entrée` ; `activer Smart Enter`
        - Changer les valeurs de :
            - `largeur d'indentation` : `3`
            - `Longueur de ligne` : `10000`
    - dans Préférences/Éditeur/Formatage/XML :
        - cocher : `Conserver les lignes vides` ; `Conserver les sauts de ligne dans les attributs` ; `Indenter les éléments en ligne`
        - dans `Espacement des éléments/Conserver les espaces`, ajouter : `//p//*` ; `//head//*` ; `//dateline//*` ; `//signed//*` ; `//choice`
    - dans Preferences/XML/XSLT/FO/XQuery/XSLT/Saxon/Saxon HE/PE/EE
        - décocher la case `Étendre les attributs par défaut ("-expand")`
    - changer la police pour `IBM Plex Mono`

### Gestionnaire de Pacquets
- Homebrew [https://brew.sh/index_fr](https://brew.sh/index_fr)

### Traitement images
- Suite Affinity [https://affinity.serif.com/fr/](https://affinity.serif.com/fr/)
- Final Cut pro 

### Programmation et développement web
- oh-my-zsh [https://ohmyz.sh/#install](https://ohmyz.sh/#install)
    - installer thème `SolarizedDark` pour le terminal [https://ethanschoonover.com/solarized/](https://ethanschoonover.com/solarized/) | sur github perso #todo
    - changer la police du terminale `IBM Plex Mono`
    - ajouter dans le fichier binaries à `~/.zshrc` la ligne `source /Users/josselinmorvan/files/dh/code-code-codex/cheatsheets/config/.zsh_bin`.
    - ajouter dans le fichier shortcuts à `~/.zshrc` la ligne `source /Users/josselinmorvan/files/dh/code-code-codex/cheatsheets/config/.zsh_sc`.
    - activer les plugins `git` (activé par défaut) et `web-search` dans `~/.zshrc`. NB les plugins sont séparés par un espace.
- Git [https://git-scm.com/](https://git-scm.com/)
    - avec Homebrew 
        - `brew install git`
        - `git --version` #git est installé par défaut sur macOs
        - `which git` # permet de savoir qu'elle version est utilisée (par défaut celle de macOs)
        - `sudo mv /usr/bin/git /usr/bin/git-apple` | or | `brew link --overwrite git` # pour utiliser la dernière version téléchargée avec homebrew
    - Configurer un gitignore global 
        - `git config --global core.excludesfile path/to/.gitignore`
- Github 
    - clé SSH [https://docs.github.com/en/authentication/connecting-to-github-with-ssh](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
        - générer un clé ssh et l'ajouter à ssh-agent
        - ajouter la nouvelle clé ssh au compte github
- NodeJS [https://nodejs.org/en/](https://nodejs.org/en/) (de préférence LTS)
- Vim 
    - créer à la racine un fichier `.vimrc`
    - ajouter :
    ```txt
    "default vim
    source $VIMRUNTIME/defaults.vim
    
    "Enable line number
    set number
    
    "Enable syntax highlight
    syntax on
    filetype on
    colorscheme default
 
    "Enable autoindent
    set autoindent
    ```
- Apache Ant [https://ant.apache.org/](https://ant.apache.org/)
    - ajouter Ant dans le $Path
- Julia Lang [https://julialang.org/](https://julialang.org/)
- Python []()
    - avec Homebrew
- TEI Stylesheets [https://github.com/TEIC/Stylesheets](https://github.com/TEIC/Stylesheets)
    - Installation
        - Pour MacOS, télécharger le fork [https://github.com/sardinecan/Stylesheets](https://github.com/sardinecan/Stylesheets)
            - pour information, les modifications apportées au fichier `Makefile` pour l'installation avec MacOs X
                - variable PREFIX : `/usr` par `/tmp/tei`
                - ligne `cp --preserve=timestamps bin/transformtei ${PREFIX}/bin` par `cp -p bin/transformtei ${PREFIX}/bin`
                - ligne `cp --preserve=timestamps source/p5subset.xml ${PREFIX}/source` par `cp -p source/p5subset.xml ${PREFIX}/source`
                - ligne `perl -p -i -e 's+^APPHOME=.*+APPHOME=/usr/share/xml/tei/stylesheet+' ${PREFIX}/bin/transformtei` par `perl -p -i -e 's+^APPHOME=.*+APPHOME=${PREFIX}/share/xml/tei/stylesheet+' ${PREFIX}/bin/transformtei`
        - aller dans répertoire : `cd path/to/local/Stylesheets`
        - installation : `make install`
            - si la commande Make ne s'exécute pas il est probable sur Xcode commande line soit manquant, pour l'installer : `xcode-select --install`
            - si besoin de changer une variable pour l'installation : `make PREFIX=destination/path/for/installation install`
        - ajouter les `binaries` dans le `$PATH`
            - ajouter la ligne 
                ```txt
                # teic Stylesheets
                export PATH=$PATH:/tmp/tei/bin/
                ```
    - Ajouter un `profile` personalisé
        - créer un profile dans le sous-répertoire `Stylesheets/profile` selon le pattern suivant : `profiles/$PROFILENAME/$FORMAT/from.xsl` ou `profiles/$PROFILENAME/$FORMAT/to.xsl` par exemple : 
            - `profiles/local/docx/from.xsl`
        - pour importer le traitement par défaut, ajouter dans la feuille xslt créée une règle `xsl:import` , par exemple :
            - `<xsl:import href="../../default/docx/from.xsl" />`
            - ```xml
                <xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" 
                 xmlns:xs="http://www.w3.org/2001/XMLSchema"
                 xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"
                 xmlns:wne="http://schemas.microsoft.com/office/word/2006/wordml"
                 xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"
                 xmlns="http://www.tei-c.org/ns/1.0"
                 exclude-result-prefixes="xs w"
                 version="2.0">
                    <xsl:import href="../../default/docx/from.xsl"/>
                    <!-- nouvelles règles-->
                    <xsl:template match="/">[…]</xsl:template>
                </xsl:stylesheet>```
        - résintaller les stylesheets : `cd path/to/tei/Stylesheets ; make install`
    - appeler une transformation : par exemple `docxtotei inputFile outputFile`
    - appeler une transformation avec un profile personnalisé : `docxtotei --profile=$PROFILENAME inputFile outputFile` par exemple `docxtotei --profile=local inputFile outputFile`
    - NOTA : Note that if your $FORMAT is docx, this directory must contain a file template.docx which is used to create .docx files from. See the sample in the default profile.
    - NOTA 2 : [Converting from DOCX format](https://listserv.brown.edu/archives/cgi-bin/wa?A2=TEI-L;1123776a.1605) : "The TEI conversions from docx are better in many ways than the conversions from other the wordprocessing formats. There are also small tricks like having docx styles of 'tei_elementName' to get certain phrase-level elements converted."
    - NOTA 3 : [https://dixit.uni-koeln.de/wp-content/uploads/2015/04/Camp2-15-Sebastian_Rahtz_-_Working_with_TEI_Stylesheets__talk.pdf](https://dixit.uni-koeln.de/wp-content/uploads/2015/04/Camp2-15-Sebastian_Rahtz_-_Working_with_TEI_Stylesheets__talk.pdf)
    - NOTA 4 : documentation accessible dans le répertoire d'installation par exemple : `/tmp/tei/share/doc/tei-xsl/index.html` 

### Autres pacquets 
   - Bat [https://github.com/sharkdp/bat/](https://github.com/sharkdp/bat/): A cat cmd  clone with syntax highlighting and Git integration.
      - release : [https://github.com/sharkdp/bat/releases](https://github.com/sharkdp/bat/releases)
