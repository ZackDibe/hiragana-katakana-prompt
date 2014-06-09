#hiragana-katakana-zshprompt

Add a Hiragana or Katakana in your zsh prompt, and plays the sound, to make you memorize them.
The Hiragana or Katakana is changed after each command.

* [Dependencies](https://github.com/Mawu3n4/hiragana-katakana-prompt#dependencies)
* [Installation](https://github.com/Mawu3n4/hiragana-katakana-prompt#install)
* [Options](https://github.com/Mawu3n4/hiragana-katakana-prompt#options)

##Dependencies
 * [mpg321](https://github.com/Mawu3n4/hiragana-katakana-prompt#mpg321)
 * [japanese-able terminal](https://github.com/Mawu3n4/hiragana-katakana-prompt#enable-japanese-characters)


###mpg321

`apt-get install mpg321`

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

## Install

Download and extract the files in `$HOME/.hiragana-katakana-prompt/`

### Easy install

Run the `configure` script

Add `$(hirakata)` in your prompt

Done !

### ZSH and [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)

Move the `files` and `sounds` directories in the `hirakata` plugin (located in `oh-my-zsh/plugins`)

Move the `hirakata` plugin to your `.oh-my-zsh/custom/plugins` directory

Add hirakata in your plugins list in the ZSHrc
```shell
plugins=(hirakata ...)
```

You can now add `$(hirataka)` in your prompt where you want it to be displayed.

Don't forget to use `precmd()` in your theme, like so :

`$ZSH/themes/mawuena.zsh-theme`

```
precmd() {
      PROMPT="${CL_BROWN}%(!.#.❆)%{$reset_color%} $CRUNCH_DIR_$(hirakata)$CRUNCH_PROMPT%{$reset_color%}"
    }
```

### ZSH only

Add the following in your `$HOME/.zshrc`
```
HK="$HOME/.hiragana-katakana-prompt"
source $HK/bin/gen_random_sym
```

Wrap your prompt in `precmd()` and add `$(hirataka)` where you want it to be displayed, such as :
```
precmd() {
      PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ $(hirataka)'
    }
```

## Options

Options can be combined

### romaji

`$(hirakata romaji)`

Displays the romaji translation right next to the character

### hiragana

`$(hirakata hiragana)`

Only select an Hiragana character

### katakana

`$(hirakata katakana)`

Only select a Katakana character


## TO-DO
 * ~~oh-my-zsh plugin~~
 * ~~Chose from Hiragana or Katana, or both~~
 * List of H/K to ignore
 * Set frequency
 * ~~BASH install~~
 * ~~Install script~~
