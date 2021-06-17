## List of system setup related article, such as vim configuration

### shell setup
1. install [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)
2. install [starship](https://starship.rs/)
3. install neovim (nightly)
4. install `xclip` for vim and system clipboard.
---

### copy the configs from [dotfiles]()
1. .zshrc for zsh
2. starship.toml to .config/starship.toml for starship prompt config
3. copy any one of vimrc to .config/nvim/init.vim
4. tmux.conf from [github/gpakosz](https://github.com/gpakosz/.tmux)
---

### add following plugin
```
plugins=(git
	zsh-syntax-highlighting
	zsh-autosuggestions
    )
```
you may need to download those plugins
```
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting
```

---

### if your shell doesnt support utf-8 
```
export LC_ALL=en_IN.UTF-8
export LANG=en_IN.UTF-8
```
## Installing docker
1. Follow official [documentation](https://docs.docker.com/engine/install/ubuntu/)
2. Running docker commands without sudo.
      
      Check if the docker group is created.
      ```
      sudo groupadd docker
      ```
    
      add user to docker.
      ```
      sudo gpasswd -a $USER
      ```

      try running
      ```
      docker ps
      ```
      if the above command dint work, try logging into new group by
      ```
      newgroup docker
      ```