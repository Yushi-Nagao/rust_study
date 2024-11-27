# Rust

## Hello, Cargo!
- `cargo new`　を使ってプロジェクトを作成
```bash
cargo new project_name
```

- `cargo build` を使ってプロジェクトをビルドできる
```bash
cargo build
```

- `cargo run` を使うとプロジェクトのビルドと実行を1ステップで行える
```bash
cargo build
```

- `cargo check` を使うとバイナリを生成せずにプロジェクトをビルドして、エラーがないか確認できる
```bash
cargo check
```

- コーディング中は`cargo check`でコードがコンパイルできるか確かめると良い

- 実行ファイルを使いたい場合は`cargo build`でビルドすると良い

- Cargoは、ビルドの成果物をコードと同じディレクトリに保存するのではなく、`targe/debug`ディレクトリに格納する

- リリースできるようになったら`cargo build --release`を使い、最適化した状態でコンパイルできる。この場合は`target/release`に実行ファイルが格納される。コードの実行時間をベンチマークする場合は必ず`cargo build --release`を実行してリリース用実行ファイルでベンチマークをとること

- `rustup update`で最新の安定版のrustをインストールできる

## 数当てゲームのプログラミング

- Rustは最初に`cargo build`を実行したときにCargo.lockファイルを作成し、明示的にアップグレードするまでプロジェクトはCargo.lockに記載のバージョンでクレートを使用する

- クレートをアップグレードしたくなった場合、`cargo update`を使用する

- `cargo doc --open`を実行するとすべての依存クレートが提供するドキュメントをローカルでビルドしてブラウザで開ける

## 変数と可変性

- 変数を可変にしたい場合は`let mut hoge = ...`のように`mut`を使用する

- `let`をしようすればシャドーイングという同じ変数名で変数を宣言できる

- `const` は定数であり、常に不変であり、命名規則はすべて大文字でアンダースコアで単語区切りにである

- `let mut`では値は可変であるが、型は可変ではない