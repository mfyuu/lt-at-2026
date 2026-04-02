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

# 16Personalities

<div class="flex justify-center mt-4">
  <img src="/screenshots/16personalities.png" class="rounded-lg w-4/5" />
</div>

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

# デザイン

<div class="grid grid-cols-5 gap-4 h-4/5 place-content-center">
  <div class="col-span-3 grid grid-cols-2 gap-4">
    <div v-for="item in [
      { src: '/designs/icon.png', caption: 'くろねこイラスト' },
      { src: '/designs/dx-leader.png', caption: 'DX Leader バッジ' },
      { src: '/designs/koutei.png', caption: 'Koutei アイコン' },
      { src: '/designs/biimo.png', caption: 'BiiMo ロゴ' },
    ]" :key="item.src" class="flex items-center justify-center">
      <img :src="item.src" class="h-28 rounded-lg object-contain" />
    </div>
  </div>
  <div class="col-span-2 flex items-center justify-center my-auto">
    <img src="/designs/hiyarepo-poster.png" class="rounded-lg object-contain h-80" />
  </div>
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
<p class="text-sm">フロントエンド領域を中心に 開発 / レビュー / コワークなどのサポート<br />一部バックエンド領域も担当</p>
<div class="h-4" />
<div class="grid grid-cols-2 gap-x-4 gap-y-8">
  <ProjectList :projects="[
    { name: 'TIP-Extra (ファイル管理/CS)', users: ['Yasuki-Satou-TODA', '1100220', 'Kouichi-Miyazaki-TODA', 'mfyuu', 'katou000'] },
    { name: 'TIP-Extra (全件リプレイス)', users: ['Yasuki-Satou-TODA', '1100220', 'Kouichi-Miyazaki-TODA', 'm-furuno', 'mfyuu', 'katou000', 'mihoishige'] },
    { name: 'Cost Pilot', users: ['kokurimoto', 'mfyuu'] },
    { name: 'Booklift', users: ['kokurimoto', 'mfyuu', 'Yu2ki-TDX', 'ShunyaONO'] },
  ]" />
  <ProjectList :projects="[
    { name: 'Koutei', users: ['mihoishige', 'kokurimoto', 'mfyuu'] },
    { name: '配送システム', users: ['shuichitamura', 'mfyuu', 'katou000', 'ShunyaONO'] },
    { name: 'ニヤリポ（2期生DIP）', users: ['ishizuka-dx', 'kayano4', 'tdHiru', 'tdShiori', 'mihoishige', 'mfyuu'] },
    { name: 'Frontend Meetup（有志勉強会）', users: ['mfyuu', 'tdShiori', 'tdHiru', 'ishizuka-dx'] },
  ]" />
</div>

---
layout: image
image: /screenshots/tip-extra-dev.png
backgroundSize: contain
---

---

# 業務割合
<p class="text-sm">直近4ヶ月くらいのざっくり</p>
<div class="h-4" />

<PieChart variant="percent" :segments="[
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
    { icon: '/services/arc.svg', name: 'Arc', cat: 'ブラウザ', desc: 'Chrome → Brave → Arc' },
    { icon: '/services/ghostty.svg', name: 'Ghostty', cat: 'ターミナル', desc: 'GPU描画で高速・軽量' },
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

# 休日の過ごし方

<div class="grid grid-cols-[auto_1fr] gap-4">
  <PieChart unit="h" :size="340" hide-legend :segments="[
    { label: '映画/MLB/ゲーム', value: 5, color: '#ef4444' },
    { label: '睡眠', value: 7, color: '#334155' },
    { label: 'ご飯', value: 1, color: '#22c55e' },
    { label: '昼寝', value: 2, color: '#f59e0b' },
    { label: '映画/ゲーム', value: 3, color: '#8b5cf6' },
    { label: 'ご飯', value: 1, color: '#22c55e' },
    { label: '映画/コード書く', value: 3, color: '#3b82f6' },
    { label: '風呂', value: 1.5, color: '#06b6d4' },
    { label: 'コード書く', value: 0.5, color: '#3b82f6' },
  ]" />
  <div class="flex flex-col gap-4 text-sm">
    <div><mdi-weather-night class="text-indigo-400" /> どちらかと言えば夜型</div>
    <div><mdi-bathtub-outline class="text-cyan-400" /> 1hくらい湯船に浸かる</div>
    <div><mdi-terminal class="text-blue-400" /> 自分用に書くけど一応OSSとして公開はしてる</div>
    <img src="/screenshots/github-pinned-repos.png" class="rounded-lg mt-2" />
  </div>
</div>

---

# ちょっと前にハマってたこと

<div class="grid grid-cols-2 gap-4 mt-2" style="height: 400px">
  <div class="flex flex-col gap-10">
    <div class="bg-white/5 border border-white/10 rounded-lg p-4">
      <div class="text-lg font-bold mb-2"><mdi-console-line class="text-green-400" /> シェルの起動速度チューニング</div>
      <p class="text-sm opacity-80">ターミナルを開いてからコマンドが打てるようになるまでの時間を短縮。<br />プラグインの遅延読み込みやキャッシュの活用で定点観測しながらチューニング。<br />0.3s → 0.03s（x10）</p>
    </div>
    <div class="bg-white/5 border border-white/10 rounded-lg p-4">
      <div class="text-lg font-bold mb-2"><mdi-github class="text-purple-400" /> GitHubのプロフィール</div>
      <p class="text-sm opacity-80">コントリビューショングラフをパクパク食べるやつ。<br />GitHub Actionsで自動生成。</p>
    </div>
  </div>
  <div class="flex flex-col gap-0 overflow-hidden">
    <img src="/screenshots/shell-startup-time.png" class="rounded-lg block w-full" />
    <img src="https://raw.githubusercontent.com/mfyuu/mfyuu/output/github-contribution-grid-snake.svg" class="rounded-lg block w-full" />
  </div>
</div>

---
layout: center
---

# おわりに

<div class="h-4" />

#### フロントエンドで困り事あったら相談してください
