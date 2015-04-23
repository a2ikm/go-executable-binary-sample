goでライブラリとバイナリをまとめる
==================================

http://stackoverflow.com/questions/14284375 に従って、

```
src/
  github.com/
    a2ikm/
      tar/
        main.go          # tar binary
        tar/
          tar.go         # tar libary
```

みたいな構造にしてある。

importするときには

```
import (
  "github.com/a2ikm/tar/tar"
)
```

のように参照する。

実行ファイルをインストールするときは

```
go get install github.com/a2ikm/tar
```

のようにする。

なお無闇にtarというリポジトリを作りたくなかった都合上、cloneするときには

```
git cloen github.com/a2ikm/go-executable-binary-sample tar
```

のようにディレクトリ名をライブラリ名のtarと同じにする必要がある。
