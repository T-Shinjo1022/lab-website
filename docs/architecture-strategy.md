# アーキテクチャとチーム開発の方針

## 1. 基本方針
初心者を含む5人での制作なので、「どこを編集すればよいか分かる」「変更が衝突しにくい」を優先する。
- GitHubリポジトリは1つに統一する。
- ページごとにHTMLファイルを分ける。
- 共通デザインとページ固有デザインを分ける。
- 担当者は担当ページのファイルを中心に編集する。
- 共通ファイルを変更する場合は事前にリーダーと相談する。

## 2. 推奨ディレクトリ構成
```text
nagatsu-lab-website/
├── index.html
├── about.html
├── members.html
├── events.html
├── join.html
├── access.html
├── seminar/
│   ├── index.html
│   ├── design.html
│   ├── vr.html
│   └── motion.html
├── css/
│   ├── common.css
│   ├── home.css
│   ├── about.css
│   ├── members.css
│   ├── events.css
│   ├── join.css
│   ├── access.css
│   └── seminar/
│       ├── seminar-common.css
│       ├── design.css
│       ├── vr.css
│       └── motion.css
├── js/
│   ├── common.js
│   └── paper-search.js
├── images/
│   ├── common/
│   ├── about/
│   ├── members/
│   ├── events/
│   └── seminar/
│       ├── design/
│       ├── vr/
│       └── motion/
└── docs/
```
既存の構成がある場合、リーダーが確認してから変更する。AIの判断だけで構成を変えない。

## 3. 共通部分と担当部分

### リーダーが管理
- `index.html`
- `css/common.css`
- `js/common.js`
- 共通ヘッダー・フッター・ナビゲーション
- ページ間リンクの最終確認、全体統合・公開

### 各担当者が管理
- 担当ページのHTML
- 担当ページ専用CSS
- 担当ページ専用画像
- 必要な場合のみページ専用JavaScript

担当者は共通ヘッダーやフッターを独自に作り直さない。共通部分の変更が必要な場合は相談する。

## 4. CSS衝突防止
- `common.css`はリーダーが管理する。
- 担当者は自分のページ専用CSSだけを編集する。
- ページ専用CSSのクラス名にはページ名を付ける（例：`.design-hero`、`.vr-card`、`.motion-gallery`）。
- ページ専用CSSで`body`、`header`、`footer`など全体に影響する指定をしない。
- 共通色や余白の変更はリーダーに提案する。

## 5. ページ共通ルール
- 共通ヘッダー・フッターを使用する。
- ページタイトルと現在位置が分かる。
- HOME・ナビゲーションから移動できる。
- PC・スマートフォンで表示が崩れない。
- 画像に内容を説明する`alt`を設定する。
- 仮情報・仮画像はコメント等で明示する。

## 6. AI利用
- `docs/ai-development-instructions.md`と担当ページ仕様をAIに渡す。
- 作業前に既存ファイルを確認させる。
- 指定された担当ファイル以外を変更させない。
- 共通CSS・共通JSを勝手に変更させない。
- 生成コードを本人が確認し、ブラウザで動作確認する。
- 理解できないコードはAIに説明を求めてから提出する。
- 架空の研究内容・実績・人物情報・住所・連絡先を作らない。

## 7. 分業の原則
ページごとの分業は、同じファイルを複数人が同時に編集しないためのもの。担当者は担当ページの完成に責任を持ち、全体のデザイン統一はリーダーが確認する。
