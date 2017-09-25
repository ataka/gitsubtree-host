# gitsubtree-host

```
$ git subtree split --prefix=lib -b lib-master
$ git push lib lib-master:master
```

## Develop on feature branch

```
$ git checkout -b feature/1
$ ed -p: README.md
$ git commit
$ ed -p: lib/sample.md
$ git commit
...
$ git checkout master
$ git merge feature/1
```

Then push commits to host repositories.

```
$ git push origin master
$ git subtree push --prefix=lib lib master
```
