# メモ（gb-01-tooling）

次の 3 つの問いに、自分の言葉で答える。各問いの下の一次情報を開いて読んでから書く。
既に知っている JS（npm）や Java（Maven）の道具と、どこが同じでどこが違うかを書く。

## 1. go.mod は何を記録するファイルか

- 一次情報: https://go.dev/ref/mod#go-mod-file （2026-10-09 取得）
- 対比: npm の package.json（https://docs.npmjs.com/cli/v11/configuring-npm/package-json ）、Maven の pom.xml（https://maven.apache.org/pom.html ）

<!-- ここに書く -->
@go.mod はパッケージ情報を管理するためのファイル。
ここに書いてあるものがインポートで使える。バージョンの固定もする。

## 2. go.sum は何を記録するファイルか

- 一次情報: https://go.dev/ref/mod#go-sum-files （2026-10-09 取得）
- 対比: npm の package-lock.json（https://docs.npmjs.com/cli/v11/configuring-npm/package-lock-json ）

<!-- ここに書く -->
これは正直わからないが、大半のところにpackage-lock.jsonが書いているので、バージョンの固定をするためのファイルか。
モジュールの中身について、最初にインポートしたときとビルドしたときとの差分を取るための中身のハッシュを取得しているもの。
これにより、版が同じだけど中身が異なるような場合を防げるので、同じバージョンを使っているのにこっちで動かない、あっちで動かないみたいなのが防げる。

## 3. go.mod の go 行と toolchain 行は、それぞれ何を決めるか

- 一次情報: https://go.dev/doc/toolchain （2026-10-09 取得）

<!-- ここに書く -->
ツールチェーンは本当にわからないが、関連ソースがまとめられたものということか。
Go行はこれを使う人のGoのバージョンを指定する。
Toolchain行は自分の実行環境におけるGoのバージョンを指定する。
