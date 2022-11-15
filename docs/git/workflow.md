### About

This file describes how to contribute to the repository. Basic idea is to make
short living branches with few commits and make pull request to `dev` branch.

### Detailed description

There is two long living branches `master` and `dev`.

* `master` - is a branch with tested and working code. The commits are only
made from `dev` branch via `pull request`. Usually every commit made to this
branch is with version label.
* `dev` - is the branch where the actual development happens. 

And there are many short living `feature` branches. 

The structure of git flow is shown on image:
<p align="center">
    <img src="images/flow.png" width="80%">
</p>

Basically to make changes, we make new `feature` branch from `dev` branch,
make commits to `feature` branch and then make pull request to `dev` branch
to further merge the new code to `dev` branch.

### Commands to do run

To do those steps do the following in commad line interface:

* Switch to `dev` branch:
```bash
$ git checkout dev

```

* Create new feature branch with it's own name, for example `docs/git/workflow`
and switch to this new created branch (done in one command below)
```bash
$ git checkout -b docs/git/workflow
```

* Make commits:
```bash
.... some changes were made to files ....
$ git add files_changed
$ git commit -m "commit message"
```

* Push changes to server to `docs/git/workflow` branch (this branch will be
automatically created on GitHub)
```bash
$ git push origin dev/docs/workflow
```

* Go to GitHub page and using `Pull request` tab make pull request of
`docs/git/flow` branch to `dev` branch. 

* Resolve merge conflicts, if necessary (on GitHub)

* Merge (on GitHub)

* Delete the feature branch (on GitHub)

* Switch to dev (on local machine)
```bash
$ git checkout dev
```

* Pull merged changes from remote `dev` branch to yout local `dev` branch:
```bash
$ git pull
```
* And delete `docs/git/workflow` branch on your local machine if you want:

```bash
$ git branch --delete docs/git/workflow
```

