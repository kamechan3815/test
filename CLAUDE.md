# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## リポジトリ概要

これは個人的なテスト・サンドボックス用の小さなリポジトリ（`test`）であり、ビルド可能なアプリケーションではありません。パッケージマネージャー、ビルドツール、リンター、テストスイートは設定されていません。中身は互いに無関係な単独の成果物です。

- `index.html` — Bootstrap 4.5 を使った静的な HTML スニペット（CDN 経由で Bootstrap の CSS/JS と jQuery/Popper を `<link>`/`<script>` タグで読み込む）。`site.webmanifest` と `icon.png` を参照しているが、どちらもリポジトリ内には存在しない。開発サーバーやビルド手順はなく、ブラウザで直接開いて確認する。
- `test.java` — 単独の `HelloWorld` クラス。ビルドツールやパッケージ宣言なしで `javac test.java && java HelloWorld` によりコンパイル・実行できる。
- `test_sorce/` — 雑多な試し用の内容（例: 現在は空の `aaa.txt`）。

## このリポジトリでの作業

共通のビルド／テストツールが存在しないため、各ファイルは独立したものとして扱うこと。リポジトリ全体で使えるコマンドがあると想定せず、変更を加えたファイルごとに検証する（例: `.java` ファイルは `javac`/`java`、`index.html` はブラウザで直接開いて確認する）。
