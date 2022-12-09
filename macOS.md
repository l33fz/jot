#### Useful commands:
mov -> .mp4
`ffmpeg -i my-video.mov -vcodec h264 -acodec mp2 my-video.mp4`

Remove Audio (-an flag)
`ffmpeg -i $input_file -c copy -an $output_file`

---

## Homebrew Packet Manager

Homebrew is a packet manager for macOS, meaning you can install and update apps downloaded by this packet manager with a single command through the terminal~ 

Homebrew uses some abstract terminology, so here's what they mean (essentially):

**Formula-**
The package definition

**Keg-**
The installation prefix of a Formula

**Cellar-**
All Kegs are installed here

**Tap**
A Git repository of Formulae and/or commands

**Cask**
An extension of Homebrew to install macOS native apps

---
## zsh (not bash)

In your home directory^[~ or $HOME, or use `cd $HOME && pwd` to view the full path] you may or may not find a configuration file named `.zshrc` for your shell, the Z Shell. 

>Things to configure in `.zshrc`:
>* Prompt
>* Aliases
>* $VARIABLES
>* cool text~


### Setting your terminal prompt

| Code   | Substitution                       |
| ------ | ---------------------------------- |
| `%n`   | username                           |
| `%m`   | MacBook model name                 |
| `%/`   | current directory                  |
| `%1~`  | current working directory          |
| `%#`   | '#' if root / '%' if standard      |
| `%D`   | yy-mm-dd                           |
| `%W`   | mm/dd/yy                           |
| `%t`   | system time (12h format)           |
| `%T`   | system time (24h format)           |
| `%*`   | system time (24h w/seconds format) |
| `%F{}` | Formatting start (end with %f)     |
| `%B`   | Bold start (end with %b)           |
| `%S`   | Highlight (end with %s)            |
| `%U`   | Underline (end with %u)            |

**Set it with:**
```zsh
PROMPT='(custom formatting for prompt)'
```

**Example:**
```zsh
PROMPT='%F{46}%n%f %F{11}%/%f %# '
```

### Aliases

```zsh
alias YourCommand='echo Change the text in the quotes to a command'
# Example - opens the .zshrc in terminal text editor
alias Ezsh='nano $HOME/.zshrc'
```

## Exporting Variables

```zsh
export VARIABLE="VALUE"

export PATH="$HOME/mycommands:$PATH"
```

> Make sure to add `:$PATH` at the end when exporting PATH




## Any command is free game, go crazy (no)





---

My config:
```zsh
PROMPT='
%F{7}%n%f%F{7}%#%f %F{11}%~%f
$'

# 1. OpenJDK / 2,3. MacPorts
export PATH="/usr/local/opt/openjdk/bin:$PATH"
export PATH="/opt/local/bin:$PATH"
export PATH="/opt/local/sbin:$PATH"

# ALIASES
# alias [alias]='command'
alias newjavaclass='cp $HOME/javaws/java-class-template'
alias Display_img='kitty +kitten icat'
alias O='open -a Preview'
alias Envim='nvim $HOME/.config/nvim/'
alias Ezsh='vim $HOME/.zshrc'

echo "\\    /\\"
echo " )  ( ')"
echo "(  /  )"
echo " \(__)| kitty +kitten themes"
```
