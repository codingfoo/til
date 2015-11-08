# VIM

## Philosophy
text editing
  move to where you want to make a change
  make the change

command, command, command, your just always giving commands

think ahead and describe

declarative text editing



## vim language

Command
Operator - command that requires a text object or motion

Commands(operator)
  c
  d
  y
  v
  g<something>
  !  filter
  =  format
  >  shift

Commands/Operators
  double operates on line
  uppercase command work till end


Text object

Text object is a thing / unit of text
  w      word
  s      sentence
  p      paragraph
  ' " `  Strings
  [{(    blocks
  t      tags
  others: arguments, indentation, ruby block, surrounding


Motion(movement - motion used without operator)

Motion/movement is range from here(the cursor) to somewhere
  t til does not include
  f til including
  / search

Motions
  Motions alone do movement
  Motions can also be combined with operators
  lowercase motion - forward
  uppercase motion - backward


Extent/Modifiers modify a text object
  a whole object include surround whitespace, leave preceding whitespace
  i whole object without surrounding whitespace


pattern
  register
  repeats
  operation
  movement/motion
operator extent object
pair of lowercase and uppercase
ranges can be absolute or relative


## Configuration

set nocompatible

just basic settings and then customize as needed as you go

vundle or pathogen

make it easy to edit and then reload config

use vimrc and gvimrc

## Resources

yehudakatz.com/2010/07/29/everyone-who-tried-to-convince-me-to-use-vim-was-wrong/
http://mislav.uniqpath.com/2011/12/vim-revisited/

http://stevelosh.com/blog/2010/09/coming-home-to-vim/
https://wincent.com/blog/the-vim-epiphany

http://www.viemu.com/a-why-vi-vim.html
http://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1220118#1220118

## Notes

help:
  <f1>
  :help <topic>
run command
  : also mapped to ; to avoid the shift key
print working dir
  :pwd
change dir
  :cd
open file
  open any file
   e:
  open file in project
   ,t command-t
  remote files
   just use scp/ssh syntax
save file
  :w
quit
  :q
selection
  v selection
  V line selection
  c-v block selection - column edit / rectangle mode / block operations
  esc end selection
edit multiple lines simultaneously
  Use Ctrl+v to select the first column of text in the lines you want to comment.
  Then hit 'I' and type the text you want to insert.
  Then hit 'Esc', wait 1 second and the inserted text will appear on every line
repeat command
  .
macros
  qa start recording macro: a is a register for the macro,
  q  stop recording
  @a run macro in register a
  @@ run macro again
  qA append to macro in register a
  :registers command lets you view macros
  save macros
  recursive macros call @a while recording a macro
registers
  unamed
  numbered
  named
    letters use uppercase letter to append to contents
windows
  all prefaced with c-w
  n new window
  v split vertically
  c close
  o close other
  j k l h movement
navigation
  jklh arrow keys
  * next instance of word under cursor
  # prev instance of word under cursor
deleting
  d delete
undo/redo
  u undo
  c-R redo
  undo tree on a redo a branch is created
find
  / search in document
  n next term
  N previous
find and replace
  :[range]s/search/replace/
  :[range]s/search/replace/c - the c makes it interactive
  [range] % is the whole document, by default just current line
  multiline
  regex by default
find and replace in files - use args command
  :args app/views/*/*
  :argdo %s/, :expire.*)/)/ge | update
completion
  expand tags - part of text prediction
  file templates - just use snippets
  snippets - see snipmate
  text prediction - see supertab
indentation
  auto indent after brace - smartindent
  new line same as above - autoindent
  indent >>
  unindent <<
reformatting
  = correct alignment of code
  V= select code and align
  gg=G'' reindent entire file
run external command
  :!<command> run external command
  :!<command> % run external command on entire file
  :r!<command> get results of command and put in buffer
  :'a,'b!<command>   filter through command
  %! insert unix command

Screen
  H
  M
  L

gg first
G  last

navigate by search
/ ?
n N
* #
g* g#


Registers - things often end up in registers and there is a default register for stuff
  "<any char>

Mark
  m<char> make mark
  `<char> goto mark
  '<char>

operator then search
d/bacon
c/bacon
c?bacon
