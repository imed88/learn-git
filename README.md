benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~
$ mkdir learn_git

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~
$ cd learn_git/

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git
$ touch third.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git
$ git config --global user.name "imed88"

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git
$ git config --global user.email "benzimededdine@gmail.com"

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git
$ git config --list
core.symlinks=false
core.autocrlf=true
core.fscache=true
color.diff=auto
color.status=auto
color.branch=auto
color.interactive=true
help.format=html
rebase.autosquash=true
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
http.sslbackend=openssl
diff.astextplain.textconv=astextplain
credential.helper=manager
user.name=imed88
user.email=benzimededdine@gmail.com

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git
$ git init
Initialized empty Git repository in C:/Users/benzarti imed eddine/learn_git/.git                                                                                                                /

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        third.txt

nothing added to commit but untracked files present (use "git add" to track)

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git add third.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   third.txt


benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git commit -m "Adding third.txt"
[master (root-commit) 0ed4d89] Adding third.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 third.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git log
commit 0ed4d89ec2bb2bf5656cbad6fab31d4a3dfc1217 (HEAD -> master)
Author: imed88 <benzimededdine@gmail.com>
Date:   Fri Jan 12 20:08:51 2024 +0100

    Adding third.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ touch fourth.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git add third.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git add fourth.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git commit -m "adding fourth.txt"
[master 715d3a2] adding fourth.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 fourth.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ rm third.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ ls
fourth.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git add
Nothing specified, nothing added.
Maybe you wanted to say 'git add .'?

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git add .

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git commit -m "Removing third.txt"
[master d2b26e0] Removing third.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 delete mode 100644 third.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git log
commit d2b26e092e5ad094f0ef46baefec8ff3ce889d27 (HEAD -> master)
Author: imed88 <benzimededdine@gmail.com>
Date:   Fri Jan 12 20:15:07 2024 +0100

    Removing third.txt

commit 715d3a2b89e70c596f8b98b5e9ed621ef4af661a
Author: imed88 <benzimededdine@gmail.com>
Date:   Fri Jan 12 20:11:23 2024 +0100

    adding fourth.txt

commit 0ed4d89ec2bb2bf5656cbad6fab31d4a3dfc1217
Author: imed88 <benzimededdine@gmail.com>
Date:   Fri Jan 12 20:08:51 2024 +0100

    Adding third.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git config --global core.pager 'cat'

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ ls -al
total 44
drwxr-xr-x 1 benzarti imed eddine 197121 0 janv. 12 20:11 ./
drwxr-xr-x 1 benzarti imed eddine 197121 0 janv. 12 20:33 ../
drwxr-xr-x 1 benzarti imed eddine 197121 0 janv. 12 20:15 .git/
-rw-r--r-- 1 benzarti imed eddine 197121 0 janv. 12 20:10 fourth.txt

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git config --global --list
user.name=imed88
user.email=benzimededdine@gmail.com
core.pager=cat

benzarti imed eddine@LAPTOP-HHFAD38D MINGW64 ~/learn_git (master)
$ git config --global
usage: git config [<options>]

Config file location
    --global              use global config file
    --system              use system config file
    --local               use repository config file
    -f, --file <file>     use given config file
    --blob <blob-id>      read config from given blob object

Action
    --get                 get value: name [value-regex]
    --get-all             get all values: key [value-regex]
    --get-regexp          get values for regexp: name-regex [value-regex]
    --get-urlmatch        get value specific for the URL: section[.var] URL
    --replace-all         replace all matching variables: name value [value_rege                                                                                                                x]
    --add                 add a new variable: name value
    --unset               remove a variable: name [value-regex]
    --unset-all           remove all matches: name [value-regex]
    --rename-section      rename section: old-name new-name
    --remove-section      remove a section: name
    -l, --list            list all
    -e, --edit            open an editor
    --get-color           find the color configured: slot [default]
    --get-colorbool       find the color setting: slot [stdout-is-tty]

Type
    --bool                value is "true" or "false"
    --int                 value is decimal number
    --bool-or-int         value is --bool or --int
    --path                value is a path (file or directory name)
    --expiry-date         value is an expiry date

Other
    -z, --null            terminate values with NUL byte
    --name-only           show variable names only
    --includes            respect include directives on lookup
    --show-origin         show origin of config (file, standard input, blob, com                                                                                                                mand line)
