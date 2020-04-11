# DevEnv
https://medium.com/ayuth/iterm2-zsh-oh-my-zsh-the-most-power-full-of-terminal-on-macos-bdb2823fb04c
https://gist.github.com/kevin-smets/8568070

1. iterm2 + zsh
  1. brew cask install iterm2
  2. brew install zsh
  3. install oh-my-zsh
     sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
  4. cd Downloads
     curl -O https://raw.githubusercontent.com/MartinSeeler/iterm2-material-design/master/material-design-colors.itermcolors
  5. goto iTerm2 > Preferences > Profiles > Colors Tab
  6. Click Color Presets… at the bottom right
  7. Click Import…
  8. Select the material-design-colors.itermcolors file
  9. Select the material-design-colors from Load Presets…
  10. enable docker plugin
      vi ~/.zshrc
      search plugin --> /plugin
      # Which plugins would you like to load? (plugins can be found in ~/.oh-my-zsh/plugins/*)
      # Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
      # Example format: plugins=(rails git textmate ruby lighthouse)
      # Add wisely, as too many plugins slow down shell startup.
      plugins=(
        git
        docker <-- add
      )
  11. add aliases to ~/.zshrc
      alias dps="docker ps"
      alias dst="docker stats"
      alias dpsa="docker ps -a"
      alias dimgs="docker images"
      alias dcup="docker-compose up -d"
      alias dcdown="docker-compose down"
      alias dcstart="docker-compose start"
      alias dcstop="docker-compose stop"
  
  * Solarize+powerlevel9k/10k
    https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k
  
    git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
    
    edit ~/.zshrc 
      ZSH_THEME="powerlevel10k/powerlevel10k"
      POWERLEVEL9K_MODE="awesome-patched"
