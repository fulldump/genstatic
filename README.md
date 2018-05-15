# GenStatic

Embed static files into go binary

It grabs a directory and generate a go file with all content in base64:

```go
package statics

var Files = map[string]string{
	"about.css":  ``,
	"about.html": `PGgxPkFib3...4uLgo8L3A+Cgo=`,
	"index.css":  `Cltjb21...xcHg7CiAgfQoKfQ==`,
	"index.html": `PGRpdiB...Gl2Pg==`,
	"index.js":   `LyoKIEFuZ3VsY...Hg7CiAgfQoKfQ==`,
}
```

## How to use it

```sh
go run genstatic.go --dir=www/ --package=statics > src/my-project/statics/files.go
```
