# gopkg

A Caddy plugin to add gopkg-like functionality to your own web sites.

# Usage

`gopkg [path] [repo-uri]`

```
zikes.me {
  gopkg /multistatus https://github.com/zikes/multistatus
  gopkg /chrisify https://github.com/zikes/chrisify
}
```

The above would make the two repos go get-able via `go get zikes.me/chrisify`
and `go get zikes.me/multistatus`.

If the urls are visited normally the browser will be redirected to the repo uri.

Once implemented, `go get` can enforce your import paths with
[import path checking](https://golang.org/cmd/go/#hdr-Import_path_checking).
