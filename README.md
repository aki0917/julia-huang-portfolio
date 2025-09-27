# Julia Huang Portfolio

Figmaデザインカンプを基に作成された、Julia Huangのポートフォリオサイトです。

## 📋 プロジェクト概要

このプロジェクトは、Figmaの「Julia Huang」デザインカンプをピクセル一致で実装したレスポンシブなポートフォリオサイトです。PC、タブレット、スマートフォンに対応したモバイルファーストデザインを採用しています。

## 🎨 デザイン仕様

### レイアウト構成
- **PC (1025px+)**: 3カラムグリッドレイアウト (565px / 330px / 448px)
- **タブレット (769px-1024px)**: 2カラムレイアウト
- **スマートフォン (768px-)**: 1カラムレイアウト

### カラーパレット
- 背景色: `#F9F1F0`
- カード背景: `#FADCD9`
- アクセントカラー: `#F8AFA6`
- テキスト: `#000000`
- ホワイト: `#FFFFFF`

### タイポグラフィ
- **見出し・太字**: Poppins (Google Fonts)
- **本文**: Roboto (Google Fonts)

## 🛠 技術スタック

- **HTML5**: セマンティックマークアップ
- **SCSS**: CSSプリプロセッサ
- **CSS Grid**: レイアウトシステム
- **Flexbox**: 内部コンポーネントレイアウト
- **BEM**: CSS命名規則

## 📁 ファイル構成

```
figma#7/
├── index.html              # メインHTMLファイル
├── assets/
│   ├── css/
│   │   ├── style.scss      # SCSSソースファイル
│   │   └── style.css       # コンパイル済みCSS
│   └── img/                # 画像ファイル
│       ├── flower-icon.svg
│       ├── arrow-work.svg
│       ├── circle-icon.svg
│       ├── arrow-contact.svg
│       └── portrait.png
└── README.md               # このファイル
```

## 🚀 セットアップ

### 前提条件
- Node.js (Sassコンパイル用)
- またはSass CLI

### インストール手順

1. リポジトリをクローン
```bash
git clone [repository-url]
cd figma#7
```

2. Sassをインストール（必要な場合）
```bash
npm install -g sass
```

3. SCSSをコンパイル
```bash
sass assets/css/style.scss assets/css/style.css
```

4. ブラウザでindex.htmlを開く

## 📱 レスポンシブ対応

### ブレークポイント
```scss
$breakpoints: (
  "sp": "(max-width: 768px)",           // スマートフォン
  "tab": "(min-width: 769px) and (max-width: 1024px)", // タブレット
  "pc": "(min-width: 1025px)"           // PC
);
```

### レイアウト詳細

#### PC (1025px+)
- 3カラムグリッド: `565px 330px 448px`
- ギャップ: `24px`
- 最大幅: `1391px`
- グリッドエリア:
  ```
  "head     portrait work"
  "about    contact work"  
  "about    contact socials"
  ```

#### タブレット (769px-1024px)
- 2カラムグリッド: `1fr 1fr`
- グリッドエリア:
  ```
  "head     portrait"
  "work     work"
  "about    contact"
  "socials  socials"
  ```

#### スマートフォン (768px-)
- 1カラムグリッド
- グリッドエリア:
  ```
  "head"
  "portrait"
  "work"
  "about"
  "contact"
  "socials"
  ```

## 🎯 セクション構成

### 1. ヘッダー
- ロゴ（テキストのみ）
- ナビゲーションメニュー

### 2. Slogan
- メインタイトル
- フラワーアイコン

### 3. Portrait
- プロフィール画像

### 4. Work
- 作品紹介（Musea、Elara、Verve、Zephyr）
- 各作品の画像とタイトル

### 5. About
- 自己紹介テキスト
- サークルアイコン

### 6. Contact
- コンタクト情報
- アローアイコン

### 7. Socials
- ソーシャルメディアリンク

## 🎨 デザインシステム

### スペーシング
```scss
$spacing-xs: 8px;
$spacing-sm: 16px;
$spacing-md: 24px;
$spacing-lg: 32px;
$spacing-xl: 48px;
$spacing-xxl: 64px;
```

### ボーダーラディウス
```scss
$radius: 20px;      // メイン
$radius-sm: 16px;   // 小さい要素
```

### フォントサイズ
```scss
$fs-xs: 15px;
$fs-sm: 16px;
$fs-md: 20px;
$fs-lg: 25px;
$fs-xl: 55px;
$fs-xxl: 56px;
```

## 🔧 開発ガイドライン

### BEM命名規則
```scss
.block {}
.block__element {}
.block--modifier {}
```

### レスポンシブ対応
- モバイルファーストアプローチ
- `@mixin mq($breakpoint)` を使用したメディアクエリ

### 画像最適化
- `aspect-ratio` プロパティで比率固定
- `object-fit: cover` で画像フィット

## 📝 開発履歴

- **v1.0.0**: 初期実装
  - Figmaカンプのピクセル一致実装
  - レスポンシブ対応
  - 画像最適化
  - アクセシビリティ対応

## 🐛 既知の問題

現在、特に問題は報告されていません。

## 🤝 コントリビューション

1. このリポジトリをフォーク
2. フィーチャーブランチを作成 (`git checkout -b feature/amazing-feature`)
3. 変更をコミット (`git commit -m 'Add some amazing feature'`)
4. ブランチにプッシュ (`git push origin feature/amazing-feature`)
5. プルリクエストを作成

## 📄 ライセンス

このプロジェクトはMITライセンスの下で公開されています。

