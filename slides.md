---
theme: seriph
background: /bg/bg-toda-blur-10.png
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

<img src="/illustrations/undraw_swipe-profiles.svg" class="w-1/2 fixed right-8 bottom-1/4" />

---
layout: image-right
---

# 社歴

<div class="h-8" />

- 2019年4月〜 首都土 / 管理部
- 2020年4月〜 本社 / デジタル企画部
- 2020年7月〜 本社 / DX推進室
- 2025年3月〜 本社 / デジタル変革実装室

<img src="/illustrations/undraw_tabs.svg" class="w-1/2 fixed bottom-1/8 right-8 scale-80" />

---

# 犬より猫派

<div class="flex items-center justify-center gap-12 h-4/5">
  <PhotoMagazine src="/photos/cat_1.jpg" caption="アメリカンショートヘア" />
  <PhotoMagazine src="/photos/cat_2.png" caption="先日(3/18)で3歳になった" />
</div>

---

# ISTP-A（巨匠）

<p class="text-sm opacity-70">
巨匠は独創的かつ現実的です。新しいことを試すのが大好きで、どんなツールでも使いこなせます。
</p>

<div class="text-sm mb-8">-A（自己主張型）は-T(慎重型)と違って楽観的でストレス耐性が高い（らしい）</div>

> ISTP型の人たちは自分のルールで自由に生きるタイプといえます。社会的な常識に縛られず、何よりも自分の自主性を大切にし、独自の道を切り開いていきます。一般的な価値観とは異なる道のりかもしれませんが、そこに独自の視点の強みと美しさがあるのです。自由や個人の空間、予測不可能性への欲求を理解してくれる人々と共存できる環境を見つけることで、ISTPは充実した人生を送れるでしょう。
>
> <cite class="text-xs opacity-50 block text-right">via 16personalities.com</cite>

<p class="py-8">これからも自由に生きていくので、それなりに理解してお付き合いください</p>

---

# 普段やっていること

<div class="grid grid-cols-5 gap-4 h-4/5">
<div class="col-span-2">

- フロントエンド領域
  - 開発
  - <span class="highlight">レビュー</span>
  - <span class="highlight">質問対応/コワークなどのサポート</span>
  - <span class="highlight">フロントエンド勉強会の開催</span>
  - 技術のキャッチアップ

</div>
<div class="col-span-3 bg-contain bg-center bg-no-repeat" style="background-image: url('/screenshots/daily-work.png')" />
</div>


---

# 得意領域/苦手領域

<div class="h-6" />
<div class="flex gap-12">
  <div class="space-y-4">
    <mdi-check-all class="text-blue-500" /> <span class="text-lg">得意</span>

  - JS/TS <mdi-star class="text-yellow-500" />
  - React <mdi-star class="text-yellow-500" />
  - Next.js <mdi-star class="text-yellow-500" />
  - SSRの認証実装
  - React周辺ライブラリ
  </div>

  <div class="space-y-4">
    <mdi-check class="text-green-500" /> <span class="text-lg">サポートできる</span>

  - Vue
  - Svelte
  - Tanstack Start
  - Hono(OpenAPI連携など)
  </div>

  <div class="space-y-4">
    <mdi-help class="text-red-400" /> <span class="text-lg">他の人に聞いた方が速い</span>

  - Python
  - インフラ / DB設計
  - 社内調整など
  </div>
</div>

---

# 参加プロジェクト

<div class="h-8" />
<div class="grid grid-cols-2">
  <ProjectList :projects="[
    { name: 'TIP-Extra (ファイル管理/CS)', users: ['Yasuki-Satou-TODA', '1100220', 'Kouichi-Miyazaki-TODA', 'mfyuu', 'katou000'] },
    { name: 'TIP-Extra (全件リプレイス)', users: ['Yasuki-Satou-TODA', '1100220', 'Kouichi-Miyazaki-TODA', 'm-furuno', 'mfyuu', 'katou000', 'mihoishige'] },
    { name: 'Cost Pilot', users: ['kokurimoto', 'mfyuu'] },
    { name: 'Booklift', users: ['kokurimoto', 'mfyuu', 'Yu2ki-TDX', 'ShunyaONO'] },
    { name: 'Koutei', users: ['mihoishige', 'kokurimoto', 'mfyuu'] },
    { name: '配送システム', users: ['shuichitamura', 'mfyuu', 'katou000', 'ShunyaONO'] },
  ]">
    <template #header>
      <div><uim-rocket style="color: #3354BB" /> 開発メイン</div>
    </template>
  </ProjectList>

  <div>
    <ProjectList :projects="[
      { name: 'ニヤリポ（2期生DIP）', users: ['ishizuka-dx', 'kayano4', 'tdHiru', 'tdShiori', 'mihoishige', 'mfyuu'] },
    ]">
      <template #header>
        <div><uim-comment-dots style="color: #3354BB" /> レビュー / サポートメイン</div>
      </template>
    </ProjectList>
    <div class="h-8" />
    <ProjectList :projects="[
      { name: 'Frontend Meetup（有志勉強会）', users: ['mfyuu', 'tdShiori', 'tdHiru', 'ishizuka-dx'] },
    ]">
      <template #header>
          <uim-user-arrows style="color: #3354BB" />
          その他
      </template>
    </ProjectList>
  </div>
</div>

---

# 業務割合
<p class="text-sm">ここ半年くらいのざっくり</p>
<div class="h-4" />

<PieChart :segments="[
  { label: 'TIP-Extra (ファイル管理/CS/全リプレイス)', value: 60, color: '#3b82f6' },
  { label: 'Koutei', value: 14, color: '#22c55e' },
  { label: 'Booklift', value: 10, color: '#ef4444' },
  { label: 'Cost Pilot', value: 5, color: '#f59e0b' },
  { label: '配送システム', value: 4, color: '#8b5cf6' },
  { label: 'Frontend Meetup (有志勉強会)', value: 3, color: '#06b6d4' },
  { label: 'Niyarepo', value: 3, color: '#ec4899' },
  { label: 'Make-Minutes', value: 1, color: '#6b7280' },
]" />

---

# 開発環境+α

<div class="grid grid-cols-3 mt-4">
  <div v-for="tool in [
    { icon: '/services/mac-os.svg', name: 'macOS', cat: 'OS', desc: '' },
    { icon: '/services/ghostty.svg', name: 'Ghostty', cat: 'ターミナル', desc: 'GPU描画で高速・軽量' },
    { icon: '/services/cursor.png', name: 'Cursor', cat: 'エディタ', desc: '' },
    { icon: '/services/fonts.png', name: 'Udev Gothic NFLG', cat: 'フォント', desc: 'BIZ UDゴシック + JetBrains Mono' },
    { icon: '/services/claude.svg', name: 'Claude Code', cat: 'AIエージェント', desc: 'CodexやCopilotも少々' },
    { icon: '/services/slidev.svg', name: 'Slidev', cat: 'スライド作成', desc: 'Markdown +αで書ける' },
    { icon: '/services/clean-shot-x.png', name: 'CleanShot X', cat: 'スクショ / 録画', desc: 'macOSなら一択' },
    { icon: '/services/run-cat.png', name: 'RunCat', cat: 'システム監視', desc: '猫が走っててかわいい' },
    { icon: '/services/auto-raise.png', name: 'AutoRaise', cat: 'ウィンドウ管理', desc: 'ホバーでウィンドウ切替' },
  ]" :key="tool.name" class="flex items-center gap-2 px-2 py-4 rounded-lg bg-white/5 border border-white/10">
    <img :src="tool.icon" class="w-10 h-10 rounded-md object-contain shrink-0" />
    <div>
      <div class="text-sm font-bold">{{ tool.name }}</div>
      <div class="text-xs opacity-50">{{ tool.cat }}</div>
      <div class="text-xs opacity-70 mt-0.5">{{ tool.desc }}</div>
    </div>
  </div>
</div>

<div class="my-8
">気になるものあれば調べてみてください</div>
---
layout: image
image: /screenshots/github-repo.png
backgroundSize: contain
---

---
layout: center
---

# おわりに

<div class="h-4" />

#### フロントエンドで困り事あったら相談してください
