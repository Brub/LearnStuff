# PROMPT and RPROMPT configuration
The configuration of the z-shell prompt and rprompt is done in the .zshrc file.

There are a lot of option that can be used, they stars all with a %

## PROMPT
example:

```
PROMPT='%(?.%F{green}✅.%F{red}❌%?)%f [%B%K{221}%F{52}%~%f%k%b] '
```


## RPROMPT
example:

```
RPROMPT='%K{87}%F{21}[%* %D]%f%k'
```

## options info
### time / date
* %t
* %T
* %*
* %w
* %W
* %D

### current directory
* %~
* %/

### colours & text format
* bold: %B %b
* undelined: %U %u
* text colour: %F{123} %f [colour codes can be found here](https://upload.wikimedia.org/wikipedia/commons/1/15/Xterm_256color_chart.svg)
* background colour: %K{156} %f [colour codes can be found here](https://upload.wikimedia.org/wikipedia/commons/1/15/Xterm_256color_chart.svg)
