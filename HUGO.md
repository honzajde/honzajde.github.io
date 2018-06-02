# Hugo Tips

build public site:
`hugo`

serve locally (for dev):
`hugo server`  

with drfts enabled:
`hugo server -D`

git push submodules:
`git push --recurse-submodules=on-demand`

update Hugo:
`go get -u -v github.com/gohugoio/hugo`

install binary:
`choco install hugo -confirm`

To publish:  

```sh
hugo
git add public
git commit -m ""
git push --recurse-submodules=on-deman
```

To save (also this works):

```sh
git add public content static themes
# ... same as publish
```

## Troubleshooting

_push declined due to email privacy restrictions_
[https://stackoverflow.com/questions/43378060/meaning-of-the-github-message-push-declined-due-to-email-privacy-restrictions]()

## Resources

[https://gohugo.io/getting-started/quick-start/]()