---
title: 'System Setup'
date: '2022-05-17'
author: 'jmorvan'
keywords: 'config ; dev ; installation'
---

# systemSetup
SystemSetup is a repo with my macOs/Unix system setup for dev/coding! Enjoy! ;)

## Gestionnaires de paquets
Installer Homebrew [https://brew.sh/index_fr](https://brew.sh/index_fr) (macOS et Linux).

## Git [https://git-scm.com/](https://git-scm.com/)
### Installation avec Homebrew
- `brew install git`
- `git --version` #git est livré avec macOS
- `which git` # Pour connaître quelle version est utilisé (la version de macOs par defaut)
- `sudo mv /usr/bin/git /usr/bin/git-apple` | ou | `brew link --overwrite git` # pour switcher sur la version de homebrew si nécessaire

### Configuration du `.gitignore` global : 
Cloner le repo [systemSetup](https://github.com/sardinecan/systemSetup/), puis entrer la commande suivante dans le terminal :
```shell
git config --global core.excludesfile $HOME/files/dh/systemSetup/git/.gitignore
```

## Fonts
Voir [fonts](fonts.md)

## Terminal/shell
### Personnalisation du terminal
Ajouter le thème Hyper snazzy color scheme [https://github.com/sindresorhus/hyper-snazzy](https://github.com/sindresorhus/hyper-snazzy) et l'activer par défaut.

Autres thèmes :
    - Pure: [https://github.com/sindresorhus/pure](https://github.com/sindresorhus/pure) 
    - Molokai color scheme for Vim: [https://github.com/tomasr/molokai](https://github.com/tomasr/molokai)

### Changer le shell pour `zsh`
Depuis macOS Catalina, `zsh` est le shell par défaut sur macOS. Pour les versions antérieurs ou sur d'autres systèmes, il peut être nécessaire d'installer `zsh` ou de l'activer. Pour l'installation et l'activation, voir [Installing-ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH).

Une fois le z shell installé et activé, nous avons accès au fichier `~/.zshrc`.

### Installation de [`oh-my-zsh`](https://github.com/ohmyzsh/ohmyzsh/wiki) et personnalisation
Wiki: [Oh-my-zsh Wiki](https://github.com/ohmyzsh/wiki/tree/main)

Installation :
```shell
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

Activer les plugins: `web-search` et `aliases` dans `~/.zshrc` (`git` est activé par défaut) :
```bash
plugins=(git web-search aliases)
```

Installer le thème [typewritten](https://typewritten.dev/) | [Github](https://github.com/reobin/typewritten)
```shell
git clone https://github.com/reobin/typewritten.git $ZSH_CUSTOM/themes/typewritten
# NB $ZSH_CUSTOM est une variable par defaut de oh-my-zsh)
```

Dans `~/.zshrc`, modifier la ligne :
```bash
ZSH_THEME="typewritten/typewritten"
```
et ajouter les lignes suivante : 
```shell
TYPEWRITTEN_RELATIVE_PATH="adaptive"
TYPEWRITTEN_PROMPT_LAYOUT="pure"
TYPEWRITTEN_ARROW_SYMBOL="|"
TYPEWRITTEN_COLOR_MAPPINGS="primary:red"
```

Si ce n'est pas déjà fait, cloner le repo [systemSetup](https://github.com/sardinecan/systemSetup/) et insérer les lignes : 
- `source $HOME/files/dh/systemSetup/zsh/.zsh_bin`;
- `source $HOME/files/dh/systemSetup/zsh/.zsh_sc`
dans `~/.zshrc` afin d'ajouter les _aliases_ et _custom path_ personnels.
	    
<!--Bat [https://github.com/sharkdp/bat/](https://github.com/sharkdp/bat/): A cat cmd clone with syntax highlighting and Git integration. release : [https://github.com/sharkdp/bat/releases](https://github.com/sharkdp/bat/releases)-->




## Browsers
- Firefox [https://www.mozilla.org/fr/firefox/new/](https://www.mozilla.org/fr/firefox/new/)
- Chrome [https://www.google.com/chrome/](https://www.google.com/chrome/)

## Text Editors
- Webstorm: see [webstorm](webstorm/webstorm.md)
- Visual Studio Code: see [Visual Studio Code](visualStudioCode/vs.md)
- OxygenXML: see [Oxygen XML](oxygenXML/oxygenXML.md)
- Vim: see [Vim](vim/vim.md)

## Image/video editing
- Suite Affinity [https://affinity.serif.com/fr/](https://affinity.serif.com/fr/)
- Final Cut pro

## Programming languages
- Julia Lang [https://julialang.org/](https://julialang.org/)
    - Activating project environment in Julia REPL automatically [see https://bkamins.github.io/julialang/2020/05/10/julia-project-environments.html](https://bkamins.github.io/julialang/2020/05/10/julia-project-environments.html)
    - create a `~/.julia/config/startup.jl` with following content:

```julia
println("Greetings!")
using Pkg
if isfile("Project.toml") && isfile("Manifest.toml")
    Pkg.activate(".")
else
    Pkg.activate("/pbs/home/j/jmorvan/juliaEnv")
end
```

- Python [https://www.python.org/](https://www.python.org/)
    - install with Homebrew: `brew install python`
    - for more informations about Homebrew and Python: [https://docs.brew.sh/Homebrew-and-Python](https://docs.brew.sh/Homebrew-and-Python)



- Github
    - SSH key [https://docs.github.com/en/authentication/connecting-to-github-with-ssh](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
        - create a ssh key and add it to ssh-agent
        - add the new key to the github acount.
    - if `git push` requires username and password despite ssh
    	- Switching remote URLs from HTTPS to SSH: see [Github documentation](https://docs.github.com/fr/get-started/getting-started-with-git/managing-remote-repositories#switching-remote-urls-from-https-to-ssh)

## Libraries
- NodeJS [https://nodejs.org/en/](https://nodejs.org/en/) (LTS preferred)

- Apache Ant [https://ant.apache.org/](https://ant.apache.org/)
    - add Ant to the $Path

- TEI Stylesheets [https://github.com/TEIC/Stylesheets](https://github.com/TEIC/Stylesheets)
    - for MacOS install see: [tei Stylesheets](teiStylesheets/teiStylesheets.md)
