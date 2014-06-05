#hiragana-katakana-zshprompt

Add a Hiragan or Katakana in your zsh prompt to make you memorize them.


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


# TO-DO
 * Chose from Hiragana or Katana, or both
 * List of H/K to ignore
