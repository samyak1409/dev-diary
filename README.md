# Developer Diary


## Update all Python Packages

1) open powershell

2) paste:
```bash
pip freeze | %{$_.split('==')[0]} | %{pip install --upgrade $_}
```


## Pre-Project Process

1) [make a new GitHub repo](https://github.com/new)

2) copy the bash code of `…or create a new repository on the command line`

3) make a local dir for the project files and open git bash there

4) paste the copied bash code whose template is the following:
```bash
git init
echo "# Repository Name" >> README.md
git add README.md
git commit -m "init + readme"
git branch -M main
git remote add origin HTTPS_URL ("https://github.com/username/repository-name.git")
git push -u origin main
```


## README.md

- [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

- [About READMEs](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/about-readmes)

- Badges to put in README:
    - [Shields.io: Quality metadata badges for open source projects](https://shields.io)
    - [For the Badge: Badges for Badges' sake](https://forthebadge.com)


## CMD Hacks

### Instantly hide a file/folder

go to the parent dir, there, open cmd and paste:
```bash
Attrib +h +s +r "file_name"
```

to un-hide:
```bash
Attrib -h -s -r "file_name"
```

### Copying the output of a command

```bash
command | clip
```

### Open a window containing the list of all the previous commands used in the current session

Press `F7`


## [Most famous stack overflow questions](https://stackoverflow.com/questions?tab=Votes)
