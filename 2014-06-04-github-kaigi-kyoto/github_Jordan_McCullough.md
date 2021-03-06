GitHub
======
- Jordan McCullough (@jordanmccullough)
  - [GitHub: @jordanmccullough](https://github.com/jordanmccullough)
  - [Twitter: @thejordanmcc](https://twitter.com/thejordanmcc)
  - GitHub Trainer
- 資料: [GitHub Training](http://training.github.com/classnotes/2014-06-04-kyoto-workshop.html)

Git
---
- secret recipe!
- githubteacher

```
gh clone githubteacher/hellogitworld
```

Contributeしたい！パーミッションない!

github-flow

```
git branch documentation-improvement
git checkout documentation-improvement
```

pushできない><

```
gh fork
gh pull-request
```

```
git log --oneline --graph --all --decorate
git rebase -i githubstudent/documentation-improvement
git log --oneline --stat --left-right
git rebase --onto master feature
git fetch origin refs/pull/4/head
```

### rebase --onto
```
Another example of --onto option is to rebase part of a branch. If we have the following situation:

                                H---I---J topicB
                              /
                      E---F---G  topicA
                    /
        A---B---C---D  master


then the command

    git rebase --onto master topicA topicB

would result in:

                    H'--I'--J'  topicB
                    /
                    | E---F---G  topicA
                    |/
        A---B---C---D  master
```

gh
--
- [jingweno/gh](https://github.com/jingweno/gh)
- [gh by jingweno](http://owenou.com/gh/)


benry
-----
```
tail -f ~/.zsh_history
```

とっておき..?
-------------
```
touch stuff.log
touch other.log
echo "stuff" > stuff.log
git config --global --list
```

@jordanmccullough's comment
---------------------------

[https://github.com/haya14busa/git-note/commit/3a42d4b934ef9101bb2575442ba3d8d416127151#commitcomment-6590105](https://github.com/haya14busa/git-note/commit/3a42d4b934ef9101bb2575442ba3d8d416127151#commitcomment-6590105)

### GitHub Command Line

`gh` is written in Go and is available here:
https://github.com/jingweno/gh

`hub` is written in Ruby and available here:
https://github.com/github/hub
History tail

The history tail loop is available for download, and looks like this:

[https://github.com/matthewmccullough/scripts/blob/master/historytailzsh](https://github.com/matthewmccullough/scripts/blob/master/historytailzsh)

```
#!/bin/sh

#Ensure we have the quantity specified on the CLI
if [ -z "$2" ]; then ARG_ERR=ERR; fi
if [ -z "$1" ]; then ARG_ERR=ERR; fi
if [ -n "$ARG_ERR" ];
then
    echo "Usage: <sleeptimesecs> <numberoflines>"
    exit
fi

sleeptimesecs=$1
numberoflines=$2

# Tail history
while [ 1 ]; do
    clear
    tail -$numberoflines ~/.zsh_history | sed s/^.*\;//
    sleep $sleeptimesecs
done
```



