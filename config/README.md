# MacOS Basic Config
My macOs setup for coding! Enjoy! ;)

## Fonts
See [fonts](fonts/fonts.md)

## Browsers
- Firefox [https://www.mozilla.org/fr/firefox/new/](https://www.mozilla.org/fr/firefox/new/)
- Chrome [https://www.google.com/chrome/](https://www.google.com/chrome/)

## Text Editors
- Webstorm: see [webstorm](webstorm/webstorm.md)
- Visual Studio Code: see [Visual Studio Code](visualStudioCode/vs.md)
- OxygenXML: see [Oxygen XML](oxygenXML/oxygenXML.md)
- Vim: see [Vim](vim/vim.md)

## Package Manager
- Homebrew: see [https://brew.sh/index_fr](https://brew.sh/index_fr)

## Image/video editing
- Suite Affinity [https://affinity.serif.com/fr/](https://affinity.serif.com/fr/)
- Final Cut pro 

## Terminal/shell
- terminal
    - install `SolarizedDark` theme [https://ethanschoonover.com/solarized/](https://ethanschoonover.com/solarized/);
    - change font for `IBM Plex Mono`.
- ZSH
    - Oh-my-zsh: see [https://ohmyz.sh/#install](https://ohmyz.sh/#install)
        - add plugins: `web-search` and `aliases` to `~/.zshrc` (`git` is enable by default): `plugins=(git web-search aliases zsh-syntax-highlighting)`;
    	- Wiki: [Oh-my-zsh Wiki](https://github.com/ohmyzsh/wiki/tree/main)
    - Install theme [typewritten](https://typewritten.dev/) | [Github](https://github.com/reobin/typewritten):
    	- `git clone https://github.com/reobin/typewritten.git $ZSH_CUSTOM/themes/typewritten` (NB $ZSH_CUSTOM is a default variable with oh-my-zsh)
	    - change `ZSH_THEME="typewritten/typewritten"` in `~/.zshrc`
	    - and add lines `TYPEWRITTEN_RELATIVE_PATH="adaptive"` | `TYPEWRITTEN_PROMPT_LAYOUT="pure"` | `TYPEWRITTEN_ARROW_SYMBOL="|"`.
    - Zsh-syntax-highlighting: see [https://github.com/zsh-users/zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
    	- Just `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`
	- activate the plugin in `~/.zshrc`: `plugins=( [plugins...] zsh-syntax-highlighting)`
    - Bat [https://github.com/sharkdp/bat/](https://github.com/sharkdp/bat/): A cat cmd clone with syntax highlighting and Git integration.
        - release : [https://github.com/sharkdp/bat/releases](https://github.com/sharkdp/bat/releases)
    - My custom path and aliases, just add to `~/.zshrc`:
        - (path binaries): `source $HOME/files/dh/code-code-codex/cheatsheets/config/zsh/.zsh_bin`;
        - (aliases): `source $HOME/files/dh/code-code-codex/cheatsheets/config/zsh/.zsh_sc`.

- Other Themes
    - Pure: [https://github.com/sindresorhus/pure](https://github.com/sindresorhus/pure)
    - Hyper snazzy color scheme: [https://github.com/sindresorhus/hyper-snazzy](https://github.com/sindresorhus/hyper-snazzy)a
    - Molokai color scheme for Vim: [https://github.com/tomasr/molokai](https://github.com/tomasr/molokai)

## Programming languages
- Julia Lang [https://julialang.org/](https://julialang.org/)
- Python [https://www.python.org/](https://www.python.org/)
    - install with Homebrew: `brew install python`
    - for more informations about Homebrew and Python: [https://docs.brew.sh/Homebrew-and-Python](https://docs.brew.sh/Homebrew-and-Python)

## version control system
- Git [https://git-scm.com/](https://git-scm.com/)
    - install with Homebrew 
        - `brew install git`
        - `git --version` #git comes by default with macOs
        - `which git` # to know which git version is used (the macOs one by default)
        - `sudo mv /usr/bin/git /usr/bin/git-apple` | or | `brew link --overwrite git` # to switch to the homebrew version if needed
    - to configure a global gitignore  
        - `git config --global core.excludesfile $HOME/files/dh/code-code-codex/cheatsheets/config/git/.gitignore` 
    - see [git folder](git/git.md)

- Github 
    - SSH key [https://docs.github.com/en/authentication/connecting-to-github-with-ssh](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
        - create a ssh key and add it to ssh-agent
        - add the new key to the github acount.
    - if `git push` requires username and password despite ssh
    	- Switching remote URLs from HTTPS to SSH: see [Github documentation](https://docs.github.com/fr/get-started/getting-started-with-git/managing-remote-repositories#switching-remote-urls-from-https-to-ssh)
        - List your existing remotes in order to get the name of the remote you want to change.
        ```console
        $ git remote -v
        > origin  https://github.com/OWNER/REPOSITORY.git (fetch)
        > origin  https://github.com/OWNER/REPOSITORY.git (push)
        ```
        - Change your remote's URL from HTTPS to SSH with the git remote set-url command.
        ```console
        git remote set-url origin git@github.com:OWNER/REPOSITORY.git
        ```

        - Verify that the remote URL has changed.
        ```console
        $ git remote -v
        # Verify new remote URL
        > origin  git@github.com:OWNER/REPOSITORY.git (fetch)
        > origin  git@github.com:OWNER/REPOSITORY.git (push)
        ```
        
## Libraries
- NodeJS [https://nodejs.org/en/](https://nodejs.org/en/) (LTS preferred)

- Apache Ant [https://ant.apache.org/](https://ant.apache.org/)
    - add Ant to the $Path

- TEI Stylesheets [https://github.com/TEIC/Stylesheets](https://github.com/TEIC/Stylesheets)
    - for MacOS install see: [tei Stylesheets](teiStylesheets/teiStylesheets.md)    
