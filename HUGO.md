# Hugo

## Install 

install (Windows):
`choco install hugo -confirm`  
update (Windows): download from releases page (unzip into portable)  

install (Ubuntu): `sudo snap install hugo`

## Clone this repository with submodules

```sh
git clone --recurse-submodules -j8 https://github.com/honzajde/honzajde-blog-src.git
cd honzajde-blog-src
# -j8 is an optional performance optimization
```

## Develop

serve locally:
`hugo server`  

serve with a **given theme**:
`hugo server -t <theme dir name>`

serve with **drafts enabled**:
`hugo server -D`

## Install theme (example)

```sh
git submodule add https://github.com/ertuil/erblog themes/erblog
git submodule init
git submodule update
```

## Publish

build public site:
`hugo`

go to `./public` and do `git push` from there (might be required!?)

git push submodules:
`git push --recurse-submodules=on-demand`

```sh
hugo
git add public content static themes
git commit -m ""
git push --recurse-submodules=on-deman
```

## Troubleshooting

### push declined due to email privacy restrictions

[https://stackoverflow.com/questions/43378060/meaning-of-the-github-message-push-declined-due-to-email-privacy-restrictions]()

Go to github settings/email and copy your noreply email address from there:

```sh
git config user.email {ID}+{username}@users.noreply.github.com
git commit --amend --reset-author
git push
```

## Useful Resources

[https://gohugo.io/getting-started/quick-start/]()
