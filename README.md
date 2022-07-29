# Developer Diary


## Update all Python Packages

Open powershell and paste:
```bash
pip freeze | %{$_.split('==')[0]} | %{pip install --upgrade $_}
```


## Pre-Project Process

1) [Make a new GitHub repo](https://github.com/new)

2) Copy the bash code of `…or create a new repository on the command line`

3) Make a local dir for the project files and open Git Bash there

4) Paste the copied bash code whose template is the following:
```bash
git init
echo "# Repository Name" >> README.md
git add README.md
git commit -m "init + readme"
git branch -M main
git remote add origin HTTPS_URL ("https://github.com/username/repository-name.git")
git push -u origin main
```


## Go to i-th (a Previous) Commit

1) Copy commit hash using:
```bash
git log
```

2) Paste:
```bash
git reset copied_commit_hash
```

3) 
Either add the (new) changes and commit:
```bash
git add .
git commit -m "commit message"
```
Or restore the committed changes of copied_commit_hash:
```bash
git restore .
```

4) Upload:
```bash
git push --force
```
`--force` because remote had the commits that we have reset locally


## Overwrite Last Commit

1) Add the changed files: (if there aren't any changed files, then the following steps will just change the commit message)
```bash
git add .
```

2) Commit the changes:
```bash
git commit --amend -m "new commit message"
```

3) Upload:
```bash
git push --force
```


## GitHub Contribution Process with Examples

1) Go to the repository you want to contribute, and fork

2) Open Git Bash, clone the forked repo:
```bash
git clone https://github.com/samyak1409/first-contributions.git
```

3) Add the remote-upstream (remote-origin is your (forked) repo, upstream-origin is repo from which you have forked):
```bash
git remote add upstream https://github.com/firstcontributions/first-contributions.git
```

4) Create a new temp branch for PR and switch to it:
```bash
git branch add-samyak-jain
git checkout add-samyak-jain
```
Single command for this: 
```bash
git checkout -b add-samyak-jain
```

5) Now, make the desired changes in the files

6) Add the changed files, commit, and push:
```bash
git add .
git commit -m "Add Samyak Jain to Contributors list"
git push origin add-samyak-jain
```

8) Go to the repo, compare and create pull request

9) Congrats! You just completed the standard `Fork -> Clone -> Edit -> PR` workflow that you'll encounter often as a contributor!

10) Once the pull request is merged:
- Delete the temp branch:
```bash
git branch -d add-samyak-jain
```
- And then update origin:
```bash
git pull upstream
git push origin
```


## README.md

- [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

- [About READMEs](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/about-readmes)

- Badges to put in README:
    - [Shields.io: Quality metadata badges for open source projects](https://shields.io)
    - [For the Badge: Badges for Badges' sake](https://forthebadge.com)


## CMD Hacks

### Instantly hide a file/folder

Go to the parent dir, there, open cmd and paste:
```bash
Attrib +h +s +r "file_name"
```

To un-hide:
```bash
Attrib -h -s -r "file_name"
```

### Copying the output of a command

```bash
command | clip
```

### Open a window containing the list of all the previous commands used in the current session

Press `F7`


## Most Voted Stack Overflow Questions

- [Overall](https://stackoverflow.com/questions?tab=Votes)
- Topic-wise e.g. [Git](https://stackoverflow.com/questions/tagged/git?sort=MostVotes), [Python](https://stackoverflow.com/questions/tagged/python?sort=MostVotes)


## Most Voted LeetCode Discussions

- [Interview Questions](https://leetcode.com/discuss/interview-question?orderBy=most_votes)
- [Interview Experiences](https://leetcode.com/discuss/interview-experience?orderBy=most_votes)
- Etc.

### [Important and Useful links from all over the LeetCode](https://leetcode.com/discuss/general-discussion/665604/Important-and-Useful-links-from-all-over-the-LeetCode)
