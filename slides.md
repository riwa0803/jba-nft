---
marp: true
theme: default
paginate: true
style: |
  section {
    display: flex;
    flex-direction: column;
    justify-content: flex-start !important;
    padding-top: 50px;
  }
  section.lead {
    justify-content: center !important;
    padding-top: 0;
    background: white !important;
    color: black;
  }
  section.lead h1 {
    font-size: 3em;
    margin-bottom: 0.5em;
  }
  section.lead h2 {
    font-size: 1.5em;
    opacity: 0.9;
  }
  h1 {
    margin-top: 0;
  }
  .two-columns {
    display: flex;
    align-items: flex-start;
    gap: 2rem;
    height: 100%;
  }
  .left-column {
    flex: 1;
  }
  .right-column {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
  }
  .float-right {
    float: right;
    margin-left: 2rem;
    margin-bottom: 1rem;
  }
  .image-container {
    float: right;
    width: 45%;
    margin-left: 2rem;
  }
  .image-container img {
    width: 100%;
    display: block;
    margin-bottom: 1rem;
  }
  .image-container-responsive {
    width: 100%;
    max-width: 600px;
    height: 300px;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 1rem auto;
  }
  .image-container-responsive img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
  .fixed-image-container {
    position: relative;
    width: 100%;
    height: 720px;
  }
  .image-box {
    position: absolute;
    width: 600px;
    height: 300px;
    overflow: hidden;
    background: #f0f0f0;
    left: 50%;
    transform: translateX(-50%);
  }
  .image-box:nth-child(1) {
    top: 60px;
  }
  .image-box:nth-child(2) {
    top: 390px;
  }
  .image-box img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
  .image-container-fixed {
    width: 600px;
    height: 240px;
    overflow: hidden;
    margin: 0 auto 1rem auto;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #f0f0f0;
  }
  .profile-left .image-container-fixed {
    margin: 2rem 0 0 0;
    background: none;
    justify-content: flex-start;
    width: 100%;
  }
  .profile-left .image-container-fixed img {
    width: auto;
    max-width: 100%;
    object-fit: contain;
  }
  .image-container-fixed img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
  /* ワークショップ用の小さめ画像コンテナ */
  .workshop-image {
    width: 500px;
    height: 200px;
    overflow: hidden;
    margin: 0 auto 0.5rem auto;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #f0f0f0;
  }
  .workshop-image img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
  
  /* プロフィール専用レイアウト */
  .profile-layout {
    display: flex;
    align-items: flex-start;
    gap: 2rem;
    height: 100%;
  }
  .profile-left {
    flex: 0 0 30%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
  }
  .profile-right {
    flex: 0 0 70%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
  }
  
  /* 章タイトルデザイン候補 */
  
  /* 候補1: プログレスバー付き */
  .chapter-progress {
    justify-content: center !important;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
  }
  .progress-container {
    width: 80%;
    margin: 2rem auto;
  }
  .progress-bar {
    width: 100%;
    height: 8px;
    background: rgba(255,255,255,0.3);
    border-radius: 4px;
    overflow: hidden;
  }
  .progress-fill {
    height: 100%;
    background: white;
    border-radius: 4px;
    transition: width 0.3s ease;
  }
  .chapter-number {
    font-size: 1.2em;
    opacity: 0.9;
    margin-bottom: 1rem;
  }
  
  /* 候補2: カード形式 */
  .chapter-cards {
    justify-content: flex-start !important;
    background: #f8f9fa;
    color: #333;
  }
  .cards-container {
    display: flex;
    justify-content: center;
    gap: 1rem;
    margin: 2rem 0;
    flex-wrap: wrap;
  }
  .chapter-card {
    background: white;
    border-radius: 8px;
    padding: 1rem;
    min-width: 150px;
    text-align: center;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    border: 2px solid transparent;
  }
  .chapter-card.current {
    border-color: #667eea;
    background: #667eea;
    color: white;
  }
  .card-icon {
    font-size: 2em;
    margin-bottom: 0.5rem;
  }
  .card-title {
    font-size: 0.9em;
    font-weight: bold;
  }
  
  /* 候補3: ミニマル - シンプル版 */
  .chapter-minimal {
    justify-content: center !important;
    background: #ffffff;
    color: #2c3e50;
  }
  .chapter-minimal h1 {
    font-size: 3.5em;
    font-weight: 300;
    margin-bottom: 0.5rem;
  }
  .chapter-number-large {
    font-size: 8rem;
    font-weight: 100;
    color: rgba(44, 62, 80, 0.1);
    line-height: 0.8;
    margin-bottom: 1rem;
  }
  .chapter-subtitle {
    font-size: 1.2em;
    opacity: 0.7;
    font-weight: 300;
    text-align: center;
    margin-bottom: 2rem;
  }
  .chapter-toc-inline {
    display: flex;
    justify-content: center;
    gap: 2rem;
    margin-top: 3rem;
  }
  .toc-item-inline {
    padding: 0.5rem 1rem;
    border-radius: 6px;
    font-size: 0.9rem;
    color: #7f8c8d;
    border: 2px solid transparent;
    text-align: center;
    min-width: 100px;
  }
  .toc-item-inline.current {
    background: #3498db;
    color: white;
    border-color: #2980b9;
    font-weight: 500;
  }
  .toc-number {
    display: block;
    font-weight: 600;
    margin-bottom: 0.2rem;
  }
  .toc-title-small {
    font-size: 0.8rem;
  }
  
  /* 候補4: 左右分割デザイン */
  .chapter-split {
    justify-content: flex-start !important;
    background: #ecf0f1;
    color: #2c3e50;
    display: flex !important;
    flex-direction: row !important;
    align-items: center !important;
  }
  .split-left {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #3498db;
    color: white;
    height: 100vh;
    font-size: 10rem;
    font-weight: 100;
  }
  .split-right {
    flex: 2;
    padding: 4rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .split-right h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
    font-weight: 300;
  }
  .split-right p {
    font-size: 1.3rem;
    opacity: 0.8;
    line-height: 1.6;
  }
  
  /* 候補5: ドット形式 */
  .chapter-dots {
    justify-content: center !important;
    background: #34495e;
    color: white;
  }
  .dots-container {
    display: flex;
    justify-content: center;
    gap: 1rem;
    margin: 2rem 0 3rem 0;
  }
  .chapter-dot {
    width: 16px;
    height: 16px;
    border-radius: 50%;
    background: rgba(255,255,255,0.3);
  }
  .chapter-dot.current {
    background: #3498db;
    box-shadow: 0 0 20px rgba(52,152,219,0.8);
  }
  .chapter-dots h1 {
    font-size: 3em;
    font-weight: 300;
    margin-bottom: 1rem;
  }
---

<!-- _paginate: false -->
<!-- _class: lead -->

# NFTの真実
## 〜技術と文脈が生み出す価値〜

---

# 自己紹介

<div class="profile-layout">
<div class="profile-left">

## double jump.tokyo 株式会社
# 岩崎 理久郎 

<div class="image-container-fixed">
<img src="profile.jpg" alt="Profile Photo">
</div>

</div>
<div class="profile-right">

### 主な経歴
**2018** The University of Auckland 卒業

**2019** 株式会社 Branding Engineer 入社

**2021** double jump.tokyo 株式会社 入社
         NFT販売やウォレット開発などに携わる

### ユーザーとしては2018年から活動

</div>
</div>

---

# 目次

### 第1部：基礎理解
### 第2部：現状と歴史
### 第3部：NFTと法律
### 第4部：実用と技術
### 第5部：余談
### 第6部：ワークショップ

---

<!-- _class: chapter-minimal -->

<div class="chapter-number-large">01</div>

# 基礎理解

<div class="chapter-subtitle">NFTとは何か、どう捉えるべきか</div>

<div class="chapter-toc-inline">
<div class="toc-item-inline current">
<span class="toc-number">01</span>
<span class="toc-title-small">基礎理解</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">02</span>
<span class="toc-title-small">現状と歴史</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">03</span>
<span class="toc-title-small">実用と技術</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">04</span>
<span class="toc-title-small">NFTと法律</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">05</span>
<span class="toc-title-small">余談</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">06</span>
<span class="toc-title-small">WS</span>
</div>
</div>

---

# よく言われるNFTの定義

> 「代替不可能なデータ」
> 「唯一性が証明できる」

### でも現実は...
- 偽物が横行している
- 詐欺も多発している

**なぜこのギャップが生まれるのか？**

---

# NFTは何でないのか

❌ **オリジナルであることが保証されたデータ**
→ 「オリジナルであること」は定義しきれない

❌ **コピー不可能なデータ**
→ 画像などのコンテンツはコピー可能

❌ **所有権を示すもの**
→ 法的な所有権とは別物

❌ **金融商品**
→ 投機対象ではなく技術。金融商品にも使うことはできる

---

# NFTはよく紙と表現される

### なぜ「紙」なのか
- NFT = 情報を書くための土台、そのものに価値はない
- 重要なのは「何が書かれているか」「誰が発行したか」「何に使えるか」

### この「紙」に書かれているもの
- **所有者アドレス**（誰が持っているか）
- **トークンID**（どの資産か）
- **メタデータ参照**（詳細情報へのリンク）
- **どのように作られたか**（コントラクトアドレス）

---

# Metadata.jsonはOpenSeaスタンダードを使うのが一般的

<div class="two-columns">
<div class="left-column">

### OpenSea Metadata Standard
- NFTマーケットプレイスのデファクトスタンダード
- 多くのプラットフォームで対応

### 重要性
- **相互運用性**: 複数のプラットフォームで表示可能
- **標準化**: 統一されたデータ形式

</div>
<div class="right-column">

### 基本的な構造
```json
{
  "name": "My NFT",
  "description": "This is my NFT",
  "image": "https://example.com/image.png",
  "attributes": [
    {"trait_type": "Color", "value": "Blue"},
    {"trait_type": "Rarity", "value": "Common"}
  ]
}
```

</div>
</div>

---

# NFTの範囲

<div class="two-columns">
<div class="left-column">

### 3つのレイヤー

1. **デジタルトークン**
   チェーン+コントラクトアドレス+トークンID

2. **デジタルトークン + Metadata.json**
   トークン情報と属性データ

3. **デジタルトークン + Metadata.json + Image**
   画像まで含めた全体

**技術的にはレイヤー1のみがNFT**

</div>
<div class="right-column">

<h3>一般的な構成</h3>

<div class="image-container-fixed">
<!-- ![width:100%](image.png) -->
<img src="image.png" alt="NFT Structure">
</div>

</div>
</div>

---

# 偽物・詐欺の事例

<div class="two-columns">
<div class="left-column">

### 偽物NFTの手口
- 人気プロジェクトの画像をコピー
- 類似名でコレクション作成、安く販売

### ラスメモの偽物事例
- 「ラストメモリーズ」NFTに偽物出現
- 公式と同じ画像・名前だが別コントラクト

</div>
<div class="right-column">

<div class="image-container-fixed">
<!-- ![width:100%](last-memories-nft.png) -->
<img src="last-memories-nft.png" alt="Last Memories NFT">
</div>

</div>
</div>

---

# NFTの正しい定義と理解

- NFTは世界に「一つしかない組み合わせ」の情報を持ったデータ
  - チェーン、コントラクトアドレス、トークンID
- NFTそれぞれが持っている情報全てがユニークなわけではない
- 一意性を持つのはブロックチェーンに書き込まれた情報のみ
- 「偽物のNFT」はオンチェーン情報を偽装しているわけではない

---

# NFTは何が嬉しいのか？

### 外部からも自由に参照可能
- **オープン性**: 誰でもアクセス可能なパブリックブロックチェーン
- **透明性**: データの改ざんが困難
- **検証可能性**: 第三者による独立した確認が可能

### アセットに紐づく歴史が見える
- **取引履歴**: 全ての所有者変更が記録
- **出所の証明**: 元の発行者まで遡れる
- **価格履歴**: 過去の取引価格が公開

---

# NFTの作り方

1. **チェーン選択**: Ethereum、Polygon等
2. **規格選択**: ERC721、ERC1155等
3. **コントラクト作成**: スマートコントラクトをデプロイ
4. **トークン発行**: mint関数でNFT生成

### カスタマイズ例
- 転送機能を外す（会員権用途）
- 条件付き転送

---

# ERC721規格とは

### 概要
- 2018年1月承認、NFTの標準規格
ー　他にも拡張規格があるが、一般的に「NFT」とだけ言う場合はこれ
- 各トークンが一意のIDを持つ
ー　発行や転送など、基本的な一連の機能が定義されている

### 主要機能
- **ownerOf**: 所有者確認
- **transferFrom**: 移転
- **approve**: 移転許可
- **balanceOf**: 所有数確認

### 重要性
- **相互運用性**: どこでも取引可能
- **標準化**: 統一的な扱い
- **安全性**: 検証済み実装

---

<!-- _class: chapter-minimal -->

<div class="chapter-number-large">02</div>

# 現状と歴史

<div class="chapter-subtitle">NFTの現在地、バブルと詐欺の実態</div>

<div class="chapter-toc-inline">
<div class="toc-item-inline">
<span class="toc-number">01</span>
<span class="toc-title-small">基礎理解</span>
</div>
<div class="toc-item-inline current">
<span class="toc-number">02</span>
<span class="toc-title-small">現状と歴史</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">03</span>
<span class="toc-title-small">実用と技術</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">04</span>
<span class="toc-title-small">NFTと法律</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">05</span>
<span class="toc-title-small">余談</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">06</span>
<span class="toc-title-small">WS</span>
</div>
</div>

---

# NFTの現在地

<div class="two-columns">
<div class="left-column">

### 現在の位置：**幻滅期**

- ピーク時の過度な期待が崩壊
- 実用的な価値の模索段階
- 投機から実用へのシフト

### 検索トレンドも低下

- 2022年1月をピークに90%以上減少
- 一般的な関心は薄れている
- しかし技術開発は継続中

</div>
<div class="right-column">

<div class="image-container-fixed">
<!-- ![width:100%](gartnar-japan-infra-hype.png) -->
<img src="gartnar-japan-infra-hype.png" alt="Gartner Hype Cycle">
</div>

<div class="image-container-fixed">
<!-- ![width:100%](nft-search-trends.png) -->
<img src="nft-search-trends.png" alt="NFT Search Trends">
</div>

</div>
</div>

---

# NFTの歴史と具体的事例1：バブル

<div class="two-columns">
<div class="left-column">

### バブルのピークと崩壊
- **21-22年バブル**: 週10億ドル前後
- **2022年11月ごろ**: 週1.5億ドル程度まで現象
- **現在**: 1億ドルにも満たない

</div>
<div class="right-column">

<div class="image-container-fixed">
<!-- ![width:100%](nft-trade-volume-by-chain.png) -->
<img src="nft-trade-volume-by-chain.png" alt="NFT Trade Volume">
</div>

</div>
</div>

---

# NFTの歴史と具体的事例2：高額NFT

<div class="two-columns">
<div class="left-column">

### ジャック・ドーシーの初ツイート
- 落札額：約3.2億円
- "just setting up my twttr"
- 現在の価値：ほぼ無価値

### CryptoPunks #5822
- 最高額：約27億円
- 2017年無料配布→億単位の取引へ
- Web3の象徴的存在

</div>
<div class="right-column">

<div class="image-container-fixed">
<!-- ![width:100%](jack-dorsey-first-tweet.png) -->
<img src="jack-dorsey-first-tweet.png" alt="Jack Dorsey Tweet">
</div>

<div class="image-container-fixed">
<!-- ![width:100%](cryptopunks-5822.png) -->
<img src="cryptopunks-5822.png" alt="CryptoPunks">
</div>

</div>
</div>

---

<!-- _class: chapter-minimal -->

<div class="chapter-number-large">03</div>

# NFTと法律

<div class="chapter-subtitle">法的権利とリスクの理解</div>

<div class="chapter-toc-inline">
<div class="toc-item-inline">
<span class="toc-number">01</span>
<span class="toc-title-small">基礎理解</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">02</span>
<span class="toc-title-small">現状と歴史</span>
</div>
<div class="toc-item-inline current">
<span class="toc-number">03</span>
<span class="toc-title-small">NFTと法律</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">04</span>
<span class="toc-title-small">実用と技術</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">05</span>
<span class="toc-title-small">余談</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">06</span>
<span class="toc-title-small">WS</span>
</div>
</div>

---

# NFTと法的権利

### よくある誤解
「NFTを買う = その画像の所有権も取得」
→ **これは間違い**

### 実際の購入内容
- ブロックチェーン上のトークンの所有権
- プロジェクトが定める利用権（ライセンス）
- 著作権等とは **別物**

**購入前に権利関係の確認が重要。サービス設計もこれを念頭に**

---

# 日本法での電子データと所有権

### 民法上の所有権
- **有体物**（物理的な物）にのみ成立
- 電子データは「有体物」ではない
- NFTも厳密には所有権の対象外

**「デジタル所有権」は発展途上の概念**

---

# 事例1：CryptoPunksの権利変遷

<div class="two-columns">
<div class="left-column">

### NFT保有者に画像の使用権利を付与
- Yuga Labsが権利取得
- NFT所有者に商用利用権を付与
- 明確なライセンス設定

### 現在の権利
- **個人利用**: 自由
- **商用利用**: 年収10万ドルまで可能
- **制限**: ヘイト・暴力的コンテンツ禁止

---

# 事例2：Not a Hotelの権利設計

### 不動産をNFT化し、所有者に宿泊権を付与

### 明確な権利設計
- **NFT所有者**: 年間一定日数の宿泊権
- **利用方法**: 専用プラットフォームで予約
- **転売**: NFTと共に宿泊権も移転

### 法的な工夫
- 宿泊権を**サービス利用権**として定義
- 物理的所有権とは分離
- 契約で権利関係を明確化

---

# ⚠️ NFTと賭博該当リスク

### ランダムガチャのリスク
- **有料ガチャ**: お金を払ってランダムにNFTを獲得
- **レアリティ設定**: 確率によって価値の異なるNFTが出る
- **二次流通**: 即座に換金が可能

### ゲーム内実装の注意点
- **有料参加**: 有料NFTが実質的参加料とならないよう注意
- **報酬設定**: NFT/FTともに換金性があるため、財物となりえる

**気になる場合は法律の会で聞いてください**

---

<!-- _class: chapter-minimal -->

<div class="chapter-number-large">04</div>

# 実用と技術

<div class="chapter-subtitle">NFTの実用性と技術概要</div>

<div class="chapter-toc-inline">
<div class="toc-item-inline">
<span class="toc-number">01</span>
<span class="toc-title-small">基礎理解</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">02</span>
<span class="toc-title-small">現状と歴史</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">03</span>
<span class="toc-title-small">NFTと法律</span>
</div>
<div class="toc-item-inline current">
<span class="toc-number">04</span>
<span class="toc-title-small">実用と技術</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">05</span>
<span class="toc-title-small">余談</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">06</span>
<span class="toc-title-small">WS</span>
</div>
</div>

---

# NFTのユースケース例

- **会員権**: コミュニティアクセス、特典付与
- **チケット**: イベント入場券、転売防止
- **証明書**: 卒業証書、資格証明
- **ゲーム**: アイテム所有権、相互運用性
- **DeFi**: 金融ポジションの表現
- **アート**: デジタル作品の真正性証明

---

# 現在のメジャーユースケース1：ブロックチェーンゲーム

### MyCryptoHeroes（国内BCGの先駆け）
- キャラと装備がNFT、MMORPGのRMT型P2Eの初期モデル

### エグリプト（国内最大の成功事例）
- 基本は普通のスマホゲーム、たまにNFTキャラ出現、ゲーム性最優先

### Axie Infinity（P2Eの創始者）
- ポケモン風バトル、キャラ交配でNFT増殖、独自トークンがデファクトに

---

# 現在のメジャーユースケース2：Courtyard

<div class="two-columns">
<div class="left-column">

### 概要
スニーカーやトレカなど高額コレクタブルをNFT化して安全に取引

### 仕組み
1. **預託**: 物理商品をCourtyardに送付 → NFT発行
2. **取引**: NFTの売買で所有権が即座に移転
3. **交換**: いつでもNFTと現物を交換可能

</div>
<div class="right-column">

<div class="image-container-fixed">
<!-- ![width:100%](courtyard-pokemon-card.png) -->
<img src="courtyard-pokemon-card.png" alt="Courtyard Pokemon Card">
</div>

</div>
</div>

---

# 現在のメジャーユースケース3：TripleS

<div class="two-columns">
<div class="left-column">

### 概要
ファンがNFTを通じてアイドルグループの活動に直接参加

### NFT活用
- **Objekts**: メンバーのフォトカードNFT
- **COMO**: ガバナンストークン機能
- **投票権**: メンバー選抜、楽曲選択、活動方針

</div>
<div class="right-column">

<div class="image-container-fixed">
<!-- ![width:100%](triples-como-stats.png) -->
<img src="triples-como-stats.png" alt="TripleS COMO Stats">
</div>

</div>
</div>


---

# 現在のメジャーユースケース4：DeFiポジション

<div class="two-columns">
<div class="left-column">

### UniswapやAerodromeの事例
- 流動性提供ポジションをNFT化
- ポジション情報をMetadataに記載
- 簡単に情報参照可能

</div>
<div class="right-column">

<div class="image-container-fixed">
<!-- ![width:100%](nft-3-layer-diagram.svg) -->
<img src="nft-3-layer-diagram.svg" alt="Uniswap Position NFT">
</div>

</div>
</div>

---

<!-- _class: chapter-minimal -->

<div class="chapter-number-large">05</div>

# 余談

<div class="chapter-subtitle">よく言われることと反論</div>

<div class="chapter-toc-inline">
<div class="toc-item-inline">
<span class="toc-number">01</span>
<span class="toc-title-small">基礎理解</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">02</span>
<span class="toc-title-small">現状と歴史</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">03</span>
<span class="toc-title-small">NFTと法律</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">04</span>
<span class="toc-title-small">実用と技術</span>
</div>
<div class="toc-item-inline current">
<span class="toc-number">05</span>
<span class="toc-title-small">余談</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">06</span>
<span class="toc-title-small">WS</span>
</div>
</div>

---

## 「NFTには価値がない」

### 批判
ただのJPEG画像に価値はない

### 反論
**1000円札も紙に数字と人の顔が書かれただけ**

- 価値は社会的文脈が生み出す
- 希少性、信頼、コミュニティが価値の源泉
- 技術は価値を記録・移転する手段

---

## 「代替不可能って言うけど偽物できてるじゃん」

### 批判
コピーできるので唯一性に意味がない

### 反論
**オンチェーンレベルでは偽造できていない**

- ブロックチェーン上の記録は改ざん不可能
- 「偽物」は別の場所にある「似たもの」
- 検証ツールで簡単に判別可能

---

## 「NFTは終わった」

### 批判
バブル崩壊で価値が暴落、もう終わり

### 反論
**ドットコムバブルでインターネットは終わったか？**

- 投機バブルが終わっただけ
- 技術の実用化は着実に進行中
- ゲーム、DeFi、会員権で実用例多数

---

# おまけ：オンチェーンデータだけがNFTと捉えるとできること

### 例：トークンAの多面性
- ゲームXでは：最強のキャラクター
- ゲームYでは：最弱のキャラクター  
- ゲームZでは：ありふれた武器

### Lootの事例
- テキストのみのNFT
- コミュニティが独自に解釈・活用
- 複数のゲームやプロジェクトで利用

---

# おまけ：NFTはマスアダプションするのか？

### 可能性1：データ主権への意識

#### 現在の動き
- Kindle本の「購入」vs「無期限レンタル」論争
- サービス終了によるデータ消失リスク
- 真の所有権への需要

#### NFTの役割
- デジタルデータの真の所有を可能に
- サービスに依存しない永続性

---

### 可能性2：自由に参照可能という利便性

#### 既存の需要
- オタク部屋、祭壇文化
- SNSでのコレクション自慢
- デジタルアイデンティティ表現

#### NFTの優位性
- 公式グッズの証明が容易
- 転売ヤー購入でないことも証明可能
- AIの時代に真正性がより重要に

---

# Googleログインの便利さがNFTの良さを奪う

### 新たな問題：ウォレットの分離
- **カストディアルウォレット**: サービス運営企業が代理でウォレットを作成・管理
- **データの分断**: 自分のウォレットとサービス用ウォレットが別々に
- **資産の分散**: NFTが複数のウォレットに散在
- **移転の困難**: サービス間でのNFT移動が複雑

### 結果として失われるNFTの価値
- **相互運用性**: 異なるサービス間で使えない
- **真の所有権**: 実質的にサービスに預けている状態
- **ポータビリティ**: 自由な移動ができない

**便利さと引き換えに、NFTの本質的価値を犠牲にしている**

---


<!-- _class: chapter-minimal -->

<div class="chapter-number-large">06</div>

# ワークショップ

<div class="chapter-subtitle">実際にNFTを発行してみよう</div>

<div class="chapter-toc-inline">
<div class="toc-item-inline">
<span class="toc-number">01</span>
<span class="toc-title-small">基礎理解</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">02</span>
<span class="toc-title-small">現状と歴史</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">03</span>
<span class="toc-title-small">NFTと法律</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">04</span>
<span class="toc-title-small">実用と技術</span>
</div>
<div class="toc-item-inline">
<span class="toc-number">05</span>
<span class="toc-title-small">余談</span>
</div>
<div class="toc-item-inline current">
<span class="toc-number">06</span>
<span class="toc-title-small">WS</span>
</div>
</div>

---


# 1. Thirdwebにログイン

### https://thirdweb.com/login

---

# 2. アカウントを作成

<div class="two-columns">
<div class="left-column">

### アカウント作成

</div>
<div class="right-column">

<div class="image-container-fixed">
<img src="workshop-sepolia-deploy.png" alt="Account Creation">
</div>

</div>
</div>

---

# 3. プロジェクト作成

<div class="two-columns">
<div class="left-column">

### プロジェクト作成

</div>
<div class="right-column">

<div class="workshop-image">
<img src="workshop-create-project.png" alt="OpenSea Display">
</div>

<div class="workshop-image">
<img src="create-project2.png" alt="Create Project">
</div>

</div>
</div>

---

# 4. コントラクトデプロイに進む

<div class="two-columns">
<div class="left-column">

### コントラクトデプロイに進む

</div>
<div class="right-column">

<div class="image-container-fixed">
<img src="workshop-deploy-contract.png" alt="Contract Deploy">
</div>

</div>
</div>

---

# 5. 「NFT Collection」を選択

<div class="two-columns">
<div class="left-column">

### 「NFT Collection」を選択

</div>
<div class="right-column">

<div class="image-container-fixed">
<img src="workshop-select-template.png" alt="NFT Collection">
</div>

</div>
</div>

---

# 6. Sepoliaを選択してデプロイ

<div class="two-columns">
<div class="left-column">

### Sepoliaを選択してデプロイ

</div>
<div class="right-column">

<div class="image-container-fixed">
<img src="workshop-select-chain.png" alt="Sepolia Deploy">
</div>

</div>
</div>

---

# 7. チェックリストに従ってNFTをMint

<div class="two-columns">
<div class="left-column">

### 画像入れておくのがおすすめ

</div>
<div class="right-column">

<div class="workshop-image">
<img src="workshop-metamask-thirdweb.png" alt="Mint NFT">
</div>

<div class="workshop-image">
<img src="workshop-contract-deploy.png" alt="Contract Checklist">
</div>

</div>
</div>

---

# 8. MintしたNFT

<div class="two-columns">
<div class="left-column">

### OpenSea Testnetサイトでも表示される

### https://testnets.opensea.io/ja

### 送付、販売もできます

</div>
<div class="right-column">

<!-- 画像なし -->

</div>
</div>

---


<!-- _class: lead -->

# Thank you!

## Let's make the world trustless and fair.

**質問・相談があれば**  
**JBA等経由でお気軽にお声がけください**