## goreleaser quick guide

```
mkdir myapp
cd myapp
touch main.go
.
.
.
got mod init y44k0v/myapp
git init
git add .
git commit -m "1st comment"
goreleaser init
// without remote repo
goreleaser release --snapshot --clean
git remote add origin https://github.com/y44k0v/testOfgoreleaser.git
git remote set-url origin https://y44k0v:$GITHUB_TOKEN@github.com/y44k0v/testOfgoreleaser.git
git push -u origin master
git tag -a v0.1.0 -m "First release"
git push origin v0.1.0 
goreleaser check
rm -rf dist
goreleaser build --single-target
rm -rf dist
goreleaser release --snapshot 
rm -rf dist
goreleaser release






```