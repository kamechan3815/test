# test

個人用のテスト・共有リポジトリ。特定のプロダクトやアプリケーションではなく、断片的なサンプルファイルを置く場所。

## 構成

- `index.html` — Bootstrap 4 (CDN読み込み) を使った静的HTMLのサンプル
- `test.java` — Java の Hello World サンプル (`HelloWorld` クラス)
- `test_sorce/` — 空のテキストファイルなど雑多な置き場

## 注意点

- ビルドシステム・パッケージマネージャ・テストフレームワークは導入されていない
- `index.html` は外部CDN (jQuery, Bootstrap, Popper.js) に依存しており、ローカルサーバー不要でブラウザで直接開ける
- `test.java` を実行する場合は `javac test.java && java HelloWorld`
