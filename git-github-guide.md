
#### Contributing to open source ongithub for begineers

github.com/eggheadio-github/stack-overflow-copy-paste/blob/master/contributing.md

##### Setup instruction:
1/ Fork the repo
2/ Clone the repo
3/ Create a branch
4/ Run npm install
5/ Run npm t && npm run build.
6/ Run npm run test:watch
7./ Make your changes and make tests pass.
8./ If things working , add changes with git add
and run npm run commit to our standards.
9/ Push changes to your fork git push
10. Create a pull request
11. Iterate the solution.
12. Get merged.

##### Fork the Repo
$ git clone url.git

git remote -> origin  upstream

#### To pull updates from the repo not your own .

git remote add upstream url.git
git fetch upstream

git branch --set-upstream-to=upstream/master
master
git pull
git branch -D pr/last
git checkout -b pr/last
npm install  -> to install new dependencies added
5/ Run npm t && npm run build.

git commit -am 'whatever'
git commit -am 'feat(last) : add last function'
git commit -am 'feat(last) : add last function' --no-verify
git push

##### Working with branches on a project


onesi@Namraj-4GZ7 MINGW64 ~/Desktop
$ cd ~/Desktop

onesi@Namraj-4GZ7 MINGW64 ~/Desktop
$ mkdir sassessentials

onesi@Namraj-4GZ7 MINGW64 ~/Desktop
$ cd sassessentials

onesi@Namraj-4GZ7 MINGW64 ~/Desktop/sassessentials
$ git clone --bare https://github.com/planetoftheweb/sassEssentials.git .git

$ git config --bool core.bare false
$ git branch
$ git reset --hard
$ git branch
$ npm install
$ git checkout 02_03e  # if error

$ git stash
$ git checkout 0203_e

#### Taking a screen shot in windwos
windows +shift + S
