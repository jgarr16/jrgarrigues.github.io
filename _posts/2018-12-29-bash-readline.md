---
title: "Bash Readline"
excerpt: Mods to the Bourne-again shell. 
categories: tech
thumbnail: wrench
published: true
---
!["Linux"](/images/linux.png)

In order to enable readline in bash, edit (or create) the <code>~/.inputrc</code> file to include the following:

```
  # up arrow
  "\e[A":history-search-backward
  # down arrow
  "\e[B":history-search-forward
```

More can be found on the Bash Reference Manual, in particular on the [bash readline](http://www.gnu.org/software/bash/manual/bashref.html#Readline-Interaction)

