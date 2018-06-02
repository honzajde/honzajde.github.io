# Hugo Tips

build public site:
`hugo`

serve locally (for devel):
`hugo server`  

serve locally with a given theme:
`hugo server -t <theme dir name>`

serve locally with drafts enabled:
`hugo server -D`

might be required:
go to `./public` and do `git push` from there

git push submodules:
`git push --recurse-submodules=on-demand`

install binary:
`choco install hugo -confirm`

update hugo: download from releases page (unzip into portable)

To publish:  

```sh
hugo
git add public
git commit -m ""
git push --recurse-submodules=on-deman
```

To save new posts (this works):

```sh
git add public content static themes
# ... same as publish
```

## Troubleshooting

### push declined due to email privacy restrictions
[https://stackoverflow.com/questions/43378060/meaning-of-the-github-message-push-declined-due-to-email-privacy-restrictions]()

Go to github settings/email and copy your noreply email address from there:

```bash
git config user.email {ID}+{username}@users.noreply.github.com
git commit --amend --reset-author
git push
```

## Resources

[https://gohugo.io/getting-started/quick-start/]()