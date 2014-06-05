#hiragana-katakana-zshprompt

Add a Hiragana or Katakana in your zsh prompt, and plays the sound, to make you memorize them.
The Hiragana or Katakana is changed after each command.


##Dependancies
 * [mp321](###mpg321)
 * [zsh](###Use ZSH)
 * [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)
 * [japanese-able terminal](###Enable Japanese Characters)


###mpg321

`apt-get install mpg321`

###Use ZSH

`chsh --shell /bin/zsh`

###Enable Japanese Characters

Install Japanese fonts :

`apt-get install 'fonts-takao*'`

Add the following to your Xdefaults or Xressources

```
xterm*utf8:               1
xterm*faceNameDoublesize: TakaoExMincho
xterm*faceSize:           10
```

Run `xrdb -merge [$HOME/.Xdefaults|$HOME/.Xressources]` to have your changes take effect


# Install

Download and extract the files in `$HOME/.hiragana-katakana-prompt/`

##ZSH and oh-my-zsh

Add the following to your `~/.zshrc` or in the `precdm()` function if there is already one 
```
precmd () {
    for config_file ($ZSH/lib/*.zsh); do
        source $config_file
    done
    source $ZSH/themes/$ZSH_THEME.zsh-theme
}
```

Add the content of `bin/gen_random_sym` in your `oh-my-zsh` theme (_see crunch.zsh-theme_), then place `$SYM ` where you want it to be displayed.



# TO-DO
 * oh-my-zsh plugin
 * Chose from Hiragana or Katana, or both
 * List of H/K to ignore
 * Set frequency
