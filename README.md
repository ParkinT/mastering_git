Mastering Git
=============
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/ParkinT/mastering_git?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Thom Parkin

ISBN: [978-1-78355-413-3](http://goo.gl/iC43kt) from [Packt Publishing](http://www.packtpub.com/)


===

## Video Tutorial Course - 100+ minutes

### Addendum

#### Git Workflow

I recommend [Git Workflows for Pros: A Good Git Guide](http://www.toptal.com/git/git-workflows-for-pros-a-good-git-guide) by [Joe James](http://www.joejames.io/) for an in-depth exposition of various Git Workflow options.

#### Current Branch in the Prompt

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

#### [Details of the Diff output](https://github.com/ParkinT/mastering_git/wiki/Details-of-the-Diff-Output)

===

#### How to Write a Git Commit Message
[This terrific article](http://chris.beams.io/posts/git-commit/) by [Chris Beams](http://chris.beams.io/) contains lots of good advice.
I particularly like the idea of finishing the sentence "If applied, this commit will...". That is what I intended in Mastering Git when I stated the message should advise "the developer of the future" (usually me) how the project will change if this commit is checked out.

===

The smart people at GitHub have provided this [compact reference for **Undo** almost anything in git](https://github.com/blog/2019-how-to-undo-almost-anything-with-git).

===

#### Legit
[Legit](http://www.git-legit.org/) is a complementary command-line interface for Git, optimized for workflow simplicity.  [Fork it on GitHub](https://github.com/kennethreitz/legit) and contribute to the project! 

#### First Aid Git
[First Aid Git](http://ricardofilipe.com/projects/firstaidgit/) is a very useful resource, carefully curated list of common questions about git.
Much better than the SHOTGUN approach of StackOverflow.

#### Git Bisect
The wonderful people at GitHub have written [this great short explanation of th `git bisect` command](https://github.com/blog/2094-new-year-new-git-release?utm_source=twitter&utm_medium=social&utm_campaign=git-release-2.7#review-of-git-bisect)

===

'Mastering Git' was written entirely with [BeeGit](http://www.beegit.com), and as a valued student YOU have direct access to a special promotional offer.
If you subscribe to Beegit's terrific service and enter the Coupon Code "MasteringGit", you will be rewarded.

This entire presentation was developed, tested and validated using [Nitrous.IO](http://pro.nitrous.io/).

===

[![Mastering Git is 'Nitrous Charged'](https://gist.githubusercontent.com/ParkinT/22e59e6b450d4694431a/raw/d2bde10f78da6fd5b438f0cb726b09f527d48bbf/NitrousCharged.png)](https://pro.nitrous.io/)

&copy; Packt Publishing 2015-2016 -- all rights reserved
