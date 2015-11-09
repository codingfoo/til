# Nix

## Commandline

for customizations only extend dont replace

Incrementally create a chain of commands on commandline
splat pass through args
column command
git run command in alias


Subshells
  run multiple commands in a subshell to avoid switch $( cd ; ant )
  <()
  $()

; chain together execution dont stop on errors
&& chain together execution stop on errors

Aliases
  management(edit, reload)
  short, one or two letters
  contain switches
  move to scripts for bigger

chown(only root)
chgrp
chmod
+-
rwx
u=user
g=group
o=other/world
a=all:w


> overwrite
>> append
<


aliases -> functions -> scripts


sftp command
scp use lowercase r other uppercase R for recursive

mkdir -p
-p make intermediate dirs, and no error if it exists

tar
czvf
c compress
z zip
v verbose
f file
x extract

pbcopy/pbpaste
open (dir,file,app)

key-installer/ssh-copy-id

tab completion expanding {} *

whatis - short help
whereis
which
xargs - smash multiple lines onto single line
view - read only vi
pstree


cd shorthand
  cd
  ~
  - prev dir

History
  !!  expands to the last command and all arguments
  !-3 3rd-to-last command and all arguments
  !^  first argument of the last command in history
  !:2 2nd argument of the last command
  !$  last argument of the last command
  !*  all arguments of the last command, but not the command itself
  !42 expands to the 42nd command in the history list
  !foo  last command beginning with "foo"
  !?baz last command containing "baz"
  ^foo^bar  last command with the first occurrence of "foo" replaced with "bar"
  !:gs/foo/bar  last command with all occurrences of "foo" replaced with "bar"
  <any_above>:p   prints command without executing

Job control
  bg jobnum
  ctl z suspends
  suspend
  foreground
  background send to background but not suspended
  detach


dirstack

mv foo/{from,to}_name


Shell Programming

; chain together execution dont stop on errors
&& chain together execution stop on errors

while loops have a std out and std in

set -e dont ket errors silently pass

detect when writing to a pipe rather than a terminal
quote varables when passing them as args

objdump
objdump can dissemble

dd

od (output in hex and ascii)

online upgrades pass file descriptors

strace -s 2000 -f ./binaryname



tricks
double click on brace matching will be highlighted in iterm
nest tests in a module, so they are in the same namespace
_ in irb is the last return value
ctags
temporarily cd into another dir in editor to view code checkouts
context in searching
use terminal find rather than grep(provides more context)
increase font size
start with dummy error to make sure you test suite does errors
make sure environment is sane
put html between two closed tags to mark the begin and end without messing up css by nesting. ie rails partials sync
put #comments after commands to make easier to find history wise

pipe into ruby

use ctrl R rather than up arrows
