# Tmux
-
#### Instructions

To keep it simple, we'll follow these conventions.

* `PREFIX` means the default `CTRL-b` here, though I have remapped my `PREFIX` to `CTRL-s` because it's better find it better to reach (also because most of my colleagues already use these key bidings). I hear some people have mapped their `Caps-lock-a` as their `PREFIX`. Use your discretion here. There are no rules. 

* `CTRL-s` means "press the CTRL and s keys simultaneously"

* `CTRL-R` means the same thing, except that you'll need to use
the `SHIFT` key to produce the capital "R". Just notice the capital letters.

* `CTRL-s d` means "press the CTRL and s keys simultaneously, then release,
and then press d"

* `$ tmux new-session` the dollar sign represents the prompt from the shell session.·

## Basics

#### Creating Named Sessions

`$ tmux new -s <name_of_session>`

#### Attaching From Sessions
 
 `$ tmux attach -t <name_of_existing_session>`

#### Detaching From Sessions

* `CTRL-s` `d`, or
* `PREFIX` `d`
  * NOTE: *The session you just dettached from, is still running in the background,
meaning you can still re-attach to it later.*

#### Killing Sessions

`$ tmux kill-session -t <name_of_session>`

## Window Management (Tabs)

#### Creating and naming a window with a new session

 `$ tmux new -s <name_of_session> -n <name_of_window>`

  * The `-n` flag tells tmux to name the first window whatever you pass in the `name_of_window`.

#### Creating a window from an existing session

  `PREFIX` `c` 
        
NOTE: You can then rename your newly created window by using *`PREFIX` `,`*
  
#### Tmux Command Line Mode

  `PREFIX` `:`
  
  then in the prompt we should be able to enter
  
  `new-window -n <name_of_window>`
  
   * Except that this is rather verbose and long to create a named window (tab).

#### Switching Windows

`PREFIX` `<1..9>`

#### Displaying a list of windows

`PREFIX` `w`

#### Closing a window with a prompt

`PREFIX` `&`

#### Spliting windows

  * Horizontally (will stack one pane on top of each other)
  
  `PREFIX` `-` (hyphen)
  
  * Vertically (will put one pane next to each other)
  
  `PREFIX` `\`

#### Resizing split windows

 * Smaller steps
 
   `SHIFT-LEFT` `SHIFT-RIGHT` `SHIFT-UP` `SHIFT-DOWN`

 * Bigger steps
 
   `CTRL-LEFT` `CTRL-RIGHT` `CTRL-UP` `CTRL-DOWN`

## Settings

* Reloads .tmux.conf

`PREFIX` `r`
