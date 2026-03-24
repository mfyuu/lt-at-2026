---
theme: seriph
background: /bg-toda-blur-10.png
title: lt at 2026
drawings:
  persist: false
transition: slide-left
mdc: true
fonts:
  sans: UDEV Gothic 35JPDOC
  serif: Noto Serif JP
  mono: UDEV Gothic 35JPDOC
---

# Lightning Talks

<div class="fixed bottom-4 right-8 text-right">
    <p>2026-03-31</p>
    <p>kazuya suzuki</p>
</div>

---
layout: image-right
---

# プロフィール

<div class="h-8" />

### 鈴木 和哉

<div class="h-2" />

- 29歳/AB型
- 2019年入社
- ICT採用
- 2人+1匹暮らし

<img src="/undraw_base_family.png" class="w-1/2 fixed right-8 bottom-1/4" />

---
layout: image-right
---

# 社歴

<div class="h-8" />

- 2019年4月〜 首都土 / 管理部
- 2020年4月〜 本社 / デジタル企画部
- 2020年7月〜 本社 / DX推進室
- 2025年3月〜 本社 / デジタル変革実装室

<img src="/undraw_base_history.png" class="w-1/2 fixed bottom-1/8 right-8 scale-80" />

---
layout: image-right
---

# 普段やっていること

<div class="h-8" />

- フロントエンド領域
  - 開発
  - <span class="highlight">レビュー</span>
  - <span class="highlight">質問対応/コワークなどのサポート</span>
  - <span class="highlight">勉強会の開催</span>
    - Next.js Official Docs
    - JavaScriptの非同期処理
  - 気になる技術のキャッチアップ
    - フロントエンドのUIテスト
    - React Router v7 (Remix)

<img src="/undraw_base_work.png" class="w-1/2 fixed right-8 bottom-1/4" />

---

# 得意領域/苦手領域

<div class="h-8" />
<div class="grid grid-cols-2">
  <div class="space-y-4">
    <uim-check-circle class="text-blue-500" /> <span class="text-xl">分かること</span>

  - JS/TS
  - React <uim-star class="text-yellow-500" />
  - Next.js <uim-star class="text-yellow-500" />
  - その他React周辺ライブラリの話
  </div>

  <div class="space-y-4">
    <uim-times-circle class="text-red-500" /> <span class="text-xl">分からないこと</span>

  - Vueの込み入った話
  - Nuxt.js
  - バックエンドの込み入った話
  </div>
</div>

---

# 参加プロジェクト

<div class="h-8" />
<div class="grid grid-cols-2">
  <ProjectList :projects="[
    { name: 'TIP-Extra (file管理/CS)', users: ['mfyuu', 'katou000'] },
    { name: 'TIP-Extra (全件リプレイス)', users: ['mfyuu', 'katou000', 'mihoishige'] },
    { name: 'Cost Pilot', users: ['kokurimoto', 'mfyuu'] },
    { name: 'Booklift', users: ['kokurimoto', 'mfyuu', 'Yu2ki-TDX', 'ShunyaONO'] },
    { name: 'Koutei', users: ['mihoishige', 'kokurimoto', 'mfyuu'] },
    { name: '配送システム', users: ['shuichitamura', 'mfyuu', 'katou000', 'ShunyaONO'] },
  ]">
    <template #header>
      <div><uim-rocket class="text-green-600" /> 開発メイン</div>
    </template>
  </ProjectList>

  <ProjectList :projects="[
    { name: 'ニヤリポ（2期生DIP）', users: ['ishizuka-dx', 'kayano4', 'tdHiru', 'tdShiori', 'mihoishige', 'mfyuu'] },
  ]">
    <template #header>
      <div><uim-comment-dots class="text-green-600" /> レビュー / サポートメイン</div>
    </template>
  </ProjectList>
</div>

---
layout: center
---

# おわりに

<div class="h-4" />

#### フロントエンドで困り事あったら相談してください
