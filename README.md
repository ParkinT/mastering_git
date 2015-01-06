Mastering Git
=============
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/ParkinT/mastering_git?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Thom Parkin

ISBN: [978-1-78355-413-3](http://goo.gl/iC43kt) from [Packt Publishing](http://www.packtpub.com/)


===

## Video Tutorial Course - 120 minutes


### Addendum

Add this to the `~/.bashrc` file on your computer for the customized command prompt that shows your current 'git' branch:

```
[ -z "$PS1" ] && return

function parse_git_dirty
{
  git diff --no-ext-diff --quiet --exit-code &> /dev/null || echo "*"
}

function parse_git_branch
{
  git branch --no-color >2 /dev/null | sed -e '/^[^*]/d' -e "s/* \(.*\)/(\1$(parse_git_dirty))/"
}

export CLICOLOR=1
export PS1="\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;36m\]\w\[\033[00m\]\$(parse_git_branch)\$ "
```

#### Details of the Diff output

{{THOM: add this to wiki}}

short form - XY PATH1 -> PATH2
For paths with merge conflicts, X and 'Y' show the modification states of each side of the merge. For paths that do not have merge conflicts, X shows the status of the index, and Y shows the status of the work tree. For untracked paths, XY are ??. Other status codes can be interpreted as follows: ' ' = unmodified

 - 'M' = modified
 - 'A' = added
 - 'D' = deleted
 - 'R' = renamed
 - 'C' = copied
 - 'U' = updated but unmerged

===

'Mastering Git' was written entirely with [BeeGit](http://www.beegit.com), and as a valued reader YOU have direct access to a special promotional offer.
If you subscribe to Beegit's terrific service and enter the Coupon Code "MasteringGit", you will be rewarded.

This entire presentation was developed, tested and validated using [Nitrous.IO](http://goo.gl/40W3l).

===

[![Mastering Git is 'Nitrous Charged'](https://gist.githubusercontent.com/ParkinT/22e59e6b450d4694431a/raw/d2bde10f78da6fd5b438f0cb726b09f527d48bbf/NitrousCharged.png)](https://www.nitrous.io/hack_button?source=embed&runtime=go&repo=ParkinT%2mastering_git.git)

&copy; Packt Publishing 2015 -- all rights reserved
