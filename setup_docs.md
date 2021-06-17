## List of system setup related article, such as vim configuration

#### shell setup
1. install [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)
2. install [starship](https://starship.rs/)
3. install neovim (nightly)

#### copy the configs from [dotfiles]()
1. .zshrc for zsh
2. starship.toml to .config/starship.toml for starship prompt config
3. copy any one of vimrc to .config/nvim/init.vim
4. tmux.conf from [github/gpakosz](https://github.com/gpakosz/.tmux)

#### add following plugin
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting


#### if your shell doesnt support utf-8 
```
export LC_ALL=en_IN.UTF-8
export LANG=en_IN.UTF-8
```
* setup alias for neovim as vim, vim
* [setting up vim for yaml file](https://www.arthurkoziel.com/setting-up-vim-for-yaml/index.html)


#### Tools



