---
name: update-claude-md
description: Refresh this repository's CLAUDE.md so it matches the repo's current contents. Use this whenever the user asks to update, refresh, review, or "sync" CLAUDE.md, whenever new files or directories have been added to the repo since CLAUDE.md was last written, or before wrapping up a task that added/removed/renamed top-level files — even if the user only asked for the file change and didn't mention CLAUDE.md by name. This repo is a small personal sandbox with no build system, so CLAUDE.md is the only place that explains what each file is for; letting it drift out of date defeats its purpose.
---

# CLAUDE.mdをリポジトリの最新状態に同期する

このリポジトリ（`kamechan3815/test`）は個人的なテスト・サンドボックスで、ビルドツールもテストスイートもありません。`CLAUDE.md` は「このリポジトリに何が入っているか」を将来のClaudeセッションに伝える唯一の手がかりです。ファイルが増えたり消えたりしたのに`CLAUDE.md`が古いままだと、次にこのリポジトリを開いたセッションが誤った前提で作業してしまいます。だからこそ、リポジトリの中身が変わったら`CLAUDE.md`もそのつど追随させます。

## 手順

1. **現状のリポジトリ構成を確認する。** `git status`でリポジトリのルートにいることを確かめてから、トップレベルのファイル・ディレクトリを一覧する（`.git`は除く）。既存の`CLAUDE.md`があれば読み、そこに書かれている内容が今のリポジトリと一致しているか照らし合わせる。

2. **差分を洗い出す。**
   - `CLAUDE.md`に書かれているが、実際にはもう存在しないファイル・説明
   - リポジトリには存在するが、`CLAUDE.md`にまだ書かれていない新しいファイル・ディレクトリ
   - ファイルの中身が変わって説明が実態と合わなくなった箇所（例: 空だったファイルに内容が入った、スクリプトの用途が変わった、など）

3. **新規・変更されたファイルは中身を実際に読んでから書く。** 拡張子や名前だけで役割を推測しない。`.xlsx`や`.docx`のような単発の成果物（比較資料など）は、リポジトリのアーキテクチャの一部ではなく単なる出力物であることが多いので、CLAUDE.mdに含めるかどうかは「将来のセッションがこのファイルの存在を知っておく必要があるか」で判断する。

4. **`CLAUDE.md`を更新する。** このリポジトリの`CLAUDE.md`は日本語で書かれている（過去のユーザー指示による）。既存の文体・見出し構成（「# CLAUDE.md」前置き文、「## リポジトリ概要」「## このリポジトリでの作業」などの見出し）を踏襲し、以下は守る:
   - 冒頭は必ず次の2行から始める:
     ```
     # CLAUDE.md

     This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.
     ```
   - 存在しないビルドコマンドやテストコマンド、アーキテクチャをでっち上げない。このリポジトリに本当にないものは「ない」とそのまま書く。
   - 各ファイルの役割は1〜2文で簡潔に。ファイル一覧の再掲や自明な説明（「READMEはREADMEです」等）は避ける。

5. **変更を見せてから確認を取る。** `CLAUDE.md`の差分を提示し、ユーザーが求めていない限りコミット・プッシュは行わない。コミットする場合は、この時点で開いている作業ブランチ（現在は`claude/init-f4ngfk`）を使う。

## 注意点

- 目的は「リポジトリの説明を正確に保つ」ことであり、CLAUDE.mdを毎回書き直すことではない。差分がなければ「最新の状態です、変更不要でした」とだけ報告すればよい。
- このリポジトリはコードベースというより雑多な置き場なので、将来ファイルの性質が大きく変わった場合（例: 実際のビルド可能なアプリケーションになった場合）は、このSKILL.mdの前提（「ビルドツールなし」等）も合わせて見直すこと。
