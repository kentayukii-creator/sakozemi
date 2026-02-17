# 迫ゼミナール | Sako Seminar

広島修道大学の迫ゼミナール（迫教授のゼミナール）公式サイトです。

**Website:** https://kentayukii-creator.github.io/sakozemi/

---

## 概要 | About

迫ゼミナールは、広島修道大学で**社会保障・ライフデザイン論**を研究する研究室です。社会の諸問題を学生の視点でデザインし、理論と実践の往復から未来を切り拓く力を育成しています。

### 研究テーマ
- **社会保障** Social Security System
- **ライフデザイン論** Life Design Theory

### 特徴
- 全学年合同で学ぶコミュニティ活動
- 縦のつながり（先輩後輩）を重視
- 就職支援とキャリア開発（100% 就職率）
- 理論と実践の継続的なアプローチ

---

## コンテンツ | Contents

このサイトでは以下の情報を提供しています：

- **ホーム** - ゼミナールの基本情報と最新ニュース
- **ニュース＆アクティビティ** - イベント報告と活動記録
- **哲学** - ゼミナールの基本理念
- **アバウト** - 研究テーマと特徴
- **メンバー** - 教員と学生の紹介
- **コンタクト** - 問い合わせ先

---

## 技術スタック | Tech Stack

- **フロントエンド**: HTML5, Tailwind CSS (CDN)
- **言語**: JavaScript (Vanilla)
- **ホスティング**: GitHub Pages
- **CI/CD**: GitHub Actions
- **デプロイメント**: peaceiris/actions-gh-pages
- **アクセシビリティ**: WCAG 準拠

---

## ページ最適化 | Performance & Optimization

- ✅ モバイルレスポンシブ対応
- ✅ WCAG アクセシビリティ準拠
- ✅ SEO 最適化（Open Graph, メタタグ）
- ✅ 軽量で高速（CDN 資源）
- ✅ スムーズなアニメーション＆インタラクション
- ✅ モーダルイメージギャラリー
- ✅ スクロール Reveal アニメーション

---

## 開発 | Development

### ローカルで実行

```bash
# リポジトリをクローン
git clone https://github.com/kentayukii-creator/sakozemi.git
cd sakozemi

# ローカルサーバーを起動（Python）
python -m http.server 8000

# ブラウザで開く
open http://localhost:8000
```

### ファイル構造

```
sakozemi/
├── index.html              # メインページ
├── images/                 # ニュース・イベント画像
│   ├── seminar.jpg         # 公開ゼミナール集合写真
│   └── interseminar.jpg    # インターゼミナール大会
├── robots.txt              # 検索エンジン設定
├── sitemap.xml             # サイトマップ
├── .github/
│   └── workflows/
│       └── deploy-pages.yml    # GitHub Actions 設定
├── README.md               # このファイル
└── .gitignore              # Git 除外設定
```

---

## デプロイ | Deployment

このサイトは GitHub Actions を使用して自動デプロイされます。

### デプロイプロセス

1. **main ブランチ**にコミットを push
2. **GitHub Actions** が自動実行
3. 約 1-2 分で **gh-pages** ブランチにビルド・デプロイ
4. **GitHub Pages** で自動公開

### トリガー
- `main` ブランチへの push
- 手動トリガー（GitHub Actions UI から）

---

## ニュース管理 | News Management

NEWS & ACTIVITIES セクションにニュースを追加する手順：

### 1. テキストのみのニュース

```html
<div class="news-item group py-8 flex flex-col md:flex-row gap-4 md:gap-12">
    <div class="md:w-32 flex flex-col">
        <span class="text-[13px] font-mono font-bold text-black/40">YYYY.MM.DD</span>
        <span class="text-[10px] font-bold text-black border border-black inline-block px-1.5 py-0.5 mt-2 w-fit">INFO</span>
    </div>
    <div class="flex-grow">
        <h4 class="text-xl font-bold">ニュースタイトル</h4>
    </div>
    <div class="hidden md:flex items-center opacity-0 group-hover:opacity-100 transition-opacity"><span class="text-2xl">→</span></div>
</div>
```

### 2. 画像付きニュース（モーダル表示）

```html
<div class="news-item group py-8 flex flex-col md:flex-row gap-4 md:gap-12 cursor-pointer" onclick="openModal('unique_id')">
    <div class="md:w-32 flex flex-col">
        <span class="text-[13px] font-mono font-bold text-black/40">YYYY.MM.DD</span>
        <span class="text-[10px] font-bold text-black border border-black inline-block px-1.5 py-0.5 mt-2 w-fit">ACTIVITY</span>
    </div>
    <div class="flex-grow">
        <h4 class="text-xl font-bold">イベント名</h4>
        <button type="button" class="text-sm text-black/60 mt-2 underline hover:text-black transition-colors">CLICK TO VIEW IMAGE</button>
    </div>
    <div class="hidden md:flex items-center opacity-0 group-hover:opacity-100 transition-opacity"><span class="text-2xl">→</span></div>
</div>
```

その後、JavaScript の `openModal` 関数に以下を追加：

```javascript
} else if(imageId === 'unique_id'){
    title.textContent = 'イベント名';
    img.src = 'images/image-filename.jpg';
    img.alt = '画像の説明';
}
```

---

## ライセンス | License

© 2025-2026 迫ゼミナール / Hiroshima Shudo University. All rights reserved.

This website is open source for educational and informational purposes.

---

## お問い合わせ | Contact

ご質問やご不明な点は、[コンタクトフォーム](https://kentayukii-creator.github.io/sakozemi/#contact)からお気軽にお問い合わせください。

---

**Last Updated**: February 17, 2026

**Repository**: https://github.com/kentayukii-creator/sakozemi

**Maintained by**: 迫ゼミナール / GitHub Pages
