# 映画構造解体室 / Structural Autopsy — サイト

GitHub Pages で公開する静的サイト。ビルド不要(素のHTML/CSS)。

## 構成
- `index.html` — トップ(ブランド・タグライン・5切り口カテゴリ・引用ルール・記事/診断への導線)
- `bugonia.html` — 解体 #01『ブゴニア』(記事v5＋図3点)
- `dock.html` — 脚本ドック(有料診断)の案内
- `style.css` — 共有スタイル
- `assets/` — 図(chart1〜3.png)

## 公開手順(GitHub Pages)
1. GitHubで新規リポジトリを作る。
   - ユーザーサイトにするなら `structuralautopsy.github.io`(公開URL = https://structuralautopsy.github.io )
   - プロジェクトサイトでも可(公開URL = https://<user>.github.io/<repo>/ )
2. この `site/` の中身をリポジトリ直下に push(index.html がルートに来るように)。
3. リポジトリの Settings → Pages → Source を「Deploy from a branch」、Branch を `main` / `/(root)` に設定。
4. 数分後に公開URLで表示される。

## 記事の追加手順
1. `pipeline/` で新作を計測 → 記事mdを作成(仕様は `../ループ仕様書_評価基準.md`)。
2. `pandoc 記事.md -t html5` で本文を変換し、`bugonia.html` と同じテンプレ(ヘッダ/フッタ)で挟む。
3. 図を `assets/` に置き、`index.html` の「解体した作品」に1枚カードを追加。

## メモ
- 独自ドメインを使う場合は `CNAME` ファイルを追加し、Settings → Pages でドメインを設定。
- `*.pdf` は `.gitignore` 済み(ローカル変換の残骸を除外)。
