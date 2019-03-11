# 助けて

`GO111MODULE=off`の状態で別途`go get`して、普通にビルドするとうまくいく

```sh
➜  go_mod_test git:(master) ✗ GO111MODULE=off go run main.go
[EUC-JP ISO-2022-JP Shift JIS]
```

`got mod`を使ってビルドしようとすると、`text/encoding`をライブラリとして扱おうとしている？

```sh
➜  go_mod_test git:(master) ✗ GO111MODULE=on go run main.go
go: finding golang.org/x/text/encoding/japanese latest
go: finding golang.org/x/text/encoding latest
build command-line-arguments: cannot load golang.org/x/text/encoding/japanese: cannot find module providing package golang.org/x/text/encoding/japanese
```
