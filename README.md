# kensankai-slide 使い方メモ

## 開き方
- 通常：index.html をブラウザで直接開く
- S21を静止画にしたい場合：index.html?s21=photo をブラウザで開く

## スライド操作
- 進む：クリッカー（Kokuyo ELA-FP1）の進むボタン、または右矢印キー
- 戻る：クリッカーの戻るボタン、または左矢印キー
- 台本モード（誤入力防止）：L キーで ON/OFF

## GitHub との同期

### 日常の同期手順（VS Code）
1. ソース管理パネルを開く
2. コミットメッセージを入力して ✓（コミット）をクリック
3. ステータスバーの「Sync Changes」（⟳）をクリック

### Codex に任せる場合
Codex への指示の末尾に以下を添える：

> 変更が完了したら、diff の内容を要約した具体的なコミットメッセージ（日本語）で
> コミットし、GitHub に push してください。

### チームへの共有
GitHub Pages の URL をそのまま渡す。
S21 を静止画にしたい場合は URL の末尾に ?s21=photo を付ける。

## ファイル構成
主なファイルだけ記載する（node_modules などは省略）

```
kensankai-slide/
├── index.html            # スライド本体（全21スライド）
├── css/
│   └── slide.css         # スライドの配色・レイアウト用CSS
├── deck-stage.js          # スライド表示・操作用のWebコンポーネント
├── tweaks-panel.jsx       # 編集用調整パネル
├── assets/
│   ├── images/            # スライド内で使用する画像
│   ├── icons/              # アイコン素材
│   ├── videos/             # 動画素材
│   └── references/         # 参考資料
├── scripts/
│   └── export-slides.js   # スライドを画像として書き出すスクリプト
├── exports/
│   └── slides/             # 書き出し画像の出力先
├── package.json
└── README.md
```
