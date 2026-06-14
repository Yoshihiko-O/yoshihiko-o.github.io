# ☽ Dreave - Lucid Dream Inducer
## リブランド変更指示書
**LucidEngine → Dreave**

作成日：2026年5月　|　作成者：Yoshihiko　|　対象：LPデザイナー

---

## 1. リブランド概要

アプリ名を「LucidEngine」から「Dreave」に変更します。Bundle ID・App Store登録も新規で行うため、ランディングページ（LP）の全アセットをDreaveブランドに統一してください。

### 名前の由来

**Dreave = Dream（夢）+ Brave（勇敢）** の造語です。

「夢の中で意識を保ち続けることは、一種の勇気だ」というコンセプトがブランドの核心です。単なる睡眠アプリではなく、意識的に夢に挑む人のためのツールとして位置づけています。

### ブランド情報 新旧対照

| 項目 | 変更前（旧） | 変更後（新） |
|------|------------|------------|
| アプリ名 | LucidEngine | **Dreave** |
| サブタイトル | （なし） | Lucid Dream Inducer |
| キャッチコピー（日） | 明晰夢を、科学する。 | 明晰夢を、科学する。（変更なし） |
| キャッチコピー（英） | （なし） | **Dream Brave.** |
| サブコピー（英） | （なし） | The brave ones dream consciously. |
| Bundle ID | com.yoshihiko.LucidEngine | com.yoshihiko.Dreave |
| ロゴアイコン | ☽（三日月） | ☽（三日月）変更なし |

---

## 2. ブランドデザイン仕様

### 2-1. カラーパレット

LPの `style.css` にすでに定義されており、変更不要です。新規アセット作成時は必ずこのパレットを使用してください。

| カラー名 | HEX | 用途 |
|---------|-----|------|
| Cyan | `#59C7FA` | アクセント・CTAボタン・アイコン |
| Indigo | `#5957D6` | プライマリボタン・ナビゲーション |
| Aurora | `#8CF2BA` | チェックマーク・PRO機能強調 |
| Gold | `#F2BF4D` | PROバッジ・強調ラベル |
| BG Top | `#14142E` | ページ背景（上部） |
| BG Bot | `#261F4D` | ページ背景（下部） |
| Dark | `#0D0D2B` | セクション背景 |
| Muted | `#B0B8D8` | サブテキスト・説明文 |

### 2-2. タイポグラフィ

| 用途 | フォント | ウェイト | サイズ目安 |
|-----|---------|---------|----------|
| ページタイトル（H1） | Noto Sans JP / Inter | Bold 700 | 36–64px（clamp） |
| セクション見出し（H2） | Noto Sans JP / Inter | Bold 700 | 28–40px（clamp） |
| 本文・説明文 | Noto Sans JP / Inter | Regular 400 | 14–16px |
| ラベル・バッジ | Inter / system-ui | SemiBold 600 | 10–13px |
| カウントダウン数値 | Inter（tabular-nums） | Bold 700 | 42px |

### 2-3. ボイス・トーン

- **日本語**：簡潔・科学的・余白のある文体。過剰な感嘆符を避ける。
- **英語**：シンプル・力強い単語を選ぶ。"Dream Brave." のように短く断定的に。
- **ターゲット**：明晰夢に科学的アプローチで挑みたい、25〜40代の探求者。

---

## 3. 作業チェックリスト

### 3-1. HTMLファイル（全8ページ）— ✅ 完了済み

以下のHTMLファイルはすでにDreaveブランドに更新済みです。追加作業は不要ですが、念のため最終確認をお願いします。

| ステータス | ファイル名 | 確認ポイント |
|----------|----------|------------|
| ✅ 完了 | index.html | テキスト・メタタグがDreave表記になっていること |
| ✅ 完了 | features.html | 同上 |
| ✅ 完了 | pricing.html | 同上 |
| ✅ 完了 | science.html | 同上 |
| ✅ 完了 | journal-tips.html | 同上 |
| ✅ 完了 | privacy.html | 同上 |
| ✅ 完了 | terms.html | 同上 |
| ✅ 完了 | contact.html | 同上 |

### 3-2. 視覚アセット（新規作成が必要）— ✅ 完了済み

| ステータス | アセット | 仕様 |
|----------|--------|------|
| ✅ 完了 | og-image.png（OGP画像） | 1200×630px / PNG / `Dreave/og-image.png` に配置済み |
| ✅ 完了 | favicon.png / apple-touch-icon.png | 32×32px・180×180px（PNG運用。.ico は不使用） |
| ✅ 完了 | App Store アイコン | 1024×1024px / `Dreave/app-store-icon.png`（元データ：AppIcon_Source.png） |
| ✅ 完了 | App Store スクリーンショット | `Dreave/assets/AppStoreAssets/` に日英韓 各6枚 + プレビュー仕様書 |

### 3-3. ドキュメント・ファイル名変更 — ✅ 完了済み

| ステータス | 変更前 | 変更後 |
|----------|------|------|
| ✅ 完了 | LucidEngine_LP_デザイン仕様書.docx | Dreave_LP_デザイン仕様書.docx |
| ✅ 完了 | LucidEngine_コンテンツ仕様書.docx | Dreave_コンテンツ仕様書.docx |
| ✅ 完了 | フォルダ名：lucid-engine | Dreave（リネーム済み） |

### 3-4. GitHub Pages 親ページ更新 — ✅ 完了済み

| ステータス | ファイル | 対応内容 |
|----------|--------|--------|
| ✅ 完了 | yoshihiko-o.github.io/index.html | Dreave 表記・リンク先（`Dreave/`）更新済み |

---

## 4. OGP画像（og-image.png）デザイン仕様

SNSでシェアされた際に表示される画像です。Dreaveブランドの第一印象になるため、優先度が高いアセットです。

### 基本仕様

| 項目 | 仕様 |
|-----|------|
| ファイル名 | og-image.png |
| サイズ | 1200 × 630px（横長） |
| ファイル形式 | PNG（JPGも可） |
| 配置先 | lucid-engineフォルダ直下（index.htmlと同階層） |
| 最大ファイルサイズ | 1MB以下推奨 |

### デザイン要素

- **背景**：グラデーション `#14142E` → `#261F4D`（上から下）
- **アイコン**：☽ 三日月（カラー：`#59C7FA` / Cyan）
- **メインテキスト**：「Dreave」（白・Bold・大きめ）
- **サブテキスト**：「Lucid Dream Inducer」（`#B0B8D8` / Muted）
- **キャッチコピー**：「明晰夢を、科学する。」または「Dream Brave.」
- **右下に小さく**：「yoshihiko-o.github.io」

> 参考：index.htmlのheroセクションのデザインをベースにしてください。

---

## 5. App Storeアイコン仕様

| 項目 | 仕様 |
|-----|------|
| サイズ | 1024 × 1024px |
| ファイル形式 | PNG（透過なし・角丸はAppleが自動処理） |
| 背景 | `#14142E`（BG Top）単色またはグラデーション |
| メインモチーフ | ☽（三日月）+ 必要であれば「Dreave」のテキスト |
| アクセントカラー | `#59C7FA`（Cyan）を主軸に |
| 注意事項 | アルファチャンネル（透過）は使用不可 |

---

## 6. 対応優先順位 — ✅ 全タスク完了

> 2026-06-12 確認時点で、以下のすべてのタスクが完了しています。

| 優先度 | タスク | ステータス |
|------|------|------|
| 🔴 最優先 | og-image.png 作成 | ✅ 完了 |
| 🔴 最優先 | GitHub Pages 親ページ更新（LucidEngin→Dreave） | ✅ 完了 |
| 🔴 最優先 | favicon 作成 | ✅ 完了 |
| 🟡 高 | ファイル名変更（.docx 2件） | ✅ 完了 |
| 🟡 高 | App Storeアイコン作成 | ✅ 完了 |
| 🟢 中 | App Storeスクリーンショット作成 | ✅ 完了（日英韓 各6枚） |

---

## 7. 参考・連絡先

### 参考URL

- LP（現行）：https://yoshihiko-o.github.io/lucid-engine/index.html
- 親ページ：https://yoshihiko-o.github.io/index.html
- Apple HIG（アイコン）：https://developer.apple.com/design/human-interface-guidelines/app-icons

### 連絡先

- 制作者：Yoshihiko（kimuraenator@gmail.com）
- 質問・確認事項はメールまたはGitHub Issuesにてご連絡ください。

---

*— 以上 —*

---

**更新履歴**

- 2026-06-12：全引き継ぎ項目の完了をファイル実体・親ページHTMLで確認し、チェックリスト（3-2／3-3／3-4／6章）のステータスを ✅完了 に更新。なお、仕様書内に残る「LucidEngine」表記（`LucidEngineAudio` 等）はアプリ内製パッケージのコード識別子であり、リブランド対象外。
