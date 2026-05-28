# Dreave App Store プレビューファイル仕様書

作成日: 2026-05-24  
対象: Dreave iOS v1.0 / 日本語ローカライズ  
対象ディレクトリ: `AppStoreAssets/iphone_65`  
目的: App Store Connect の「プレビューとスクリーンショット」に登録する画像・任意動画の制作仕様を定義する。

---

## 1. 前提と参照した仕様

### 1.1 アプリ仕様の要点

Dreave は、明晰夢トレーニングを習慣化するための夢日記アプリ。就寝前の準備、Night Mode、起床後の記録、夢日記、Reality Check、分析をひとつの流れとして提供する。

v1.0 は無料MVPとして出す。コア体験は無料で、DreamPass / Lucid Pro / HealthKit / Apple Watch / iCloud同期は訴求しない。医療・睡眠診断・治療・健康改善・明晰夢成功保証に見える表現も使わない。

主に訴求すべき体験:

- 起床直後に夢を素早く記録できる
- テキスト・音声・スケッチで夢を残せ
- Recall Score / Growth Index / 連続記録で習慣化を見える化できる
- Night Mode で就寝前から起床後の振り返りまで流れを作れる
- Reality Check 通知で日中の確認習慣を支援する
- 分析で夢の傾向、明晰夢フラグ、よく出るテーマを振り返れる

### 1.2 Apple 仕様

公式参照:

- App Store Connect Help: Screenshot specifications  
  https://developer.apple.com/help/app-store-connect/reference/app-information/screenshot-specifications
- App Store Connect Help: App preview specifications  
  https://developer.apple.com/help/app-store-connect/reference/app-information/app-preview-specifications
- App Store Connect Help: Upload app previews and screenshots  
  https://developer.apple.com/help/app-store-connect/manage-app-information/upload-app-previews-and-screenshots

このリリースでは、App Store Connect 画面で指定されている iPhone 6.5インチ用を主対象にする。

| 種別 | 必須 | 上限 | 形式 | サイズ |
| --- | --- | ---: | --- | --- |
| スクリーンショット | 1枚以上 | 10枚 | PNG / JPEG / JPG | 1242 x 2688 px portrait |
| App Preview動画 | 任意 | 3本 | MP4 / MOV / M4V, H.264 | 886 x 1920 px portrait が公式受理解像度。現状の 1242 x 2688 MP4 はアップロード前に要検証 |

補足:

- ユーザー提示のApp Store Connect画面では、6.5インチスクリーンショットとして `1242 x 2688px` が表示されている。
- App Preview動画はスクリーンショットより前に表示されるため、動画を置く場合は1本目のポスター frame が商品ページの第一印象になる。
- インストールシートでは最初の3枚が特に重要。AIDMAの Attention / Interest / Desire を最初の3枚に割り当てる。

---

## 2. 制作方針

### 2.1 基本方針

1. 画像は「広告バナー」ではなく、実際のアプリ体験が伝わるApp Storeスクリーンショットとして作る。
2. すべての画像にDreaveの画面モックまたは実画面相当UIを入れる。
3. v1.0で使えない機能、将来課金、Proロック、Apple Watch、HealthKit、DreamPass制限は出さない。
4. 医療・診断・睡眠改善・成功保証表現は避け、習慣化・記録・振り返り・支援・見える化に寄せる。
5. ブランド名は必ず `Dreave`。既存スクリプト内の `LucidDream` / `Lucid Engine` 表記は修正対象。

### 2.2 ブランドトーン

キーワード:

- 静か
- 夜
- 記録
- 習慣
- 夢の振り返り
- 科学的に見えるが、効果を断定しない

避ける印象:

- スピリチュアル過多
- 医療アプリ風
- 睡眠改善アプリ風の断定
- 課金誘導
- 派手なゲーム風ライフ制

### 2.3 ビジュアルルール

| 項目 | 指定 |
| --- | --- |
| 背景 | 深い夜色のグラデーション。既存トークン `lucidNight` に近い濃紺から紫 |
| アクセント | `lucidCyan`, `lucidIndigo`, `lucidAurora` |
| 文字 | 日本語はヒラギノ角ゴ系。大見出しは太め、本文は中太 |
| 端末モック | iPhone 6.5インチ想定。画面内UIが主役になる大きさ |
| ロゴ | AppIcon + `Dreave` |
| 角丸 | アプリ内の `LucidRadius` に合わせ、過度な丸みは避ける |
| 余白 | 上部に短い訴求、下部に端末画面。文字がノッチ・端末・安全領域と重ならないこと |

---

## 3. AIDMA設計

App Storeでは一覧・検索・インストールシートで最初の数枚だけが見られるため、AIDMAを以下の順に割り当てる。

| 順序 | AIDMA | 役割 | 狙い |
| ---: | --- | --- | --- |
| 1 | Attention | 何のアプリか一瞬で伝える | 夢記録・明晰夢習慣のアプリだと即理解させる |
| 2 | Interest | 入力の手軽さを見せる | 起きた直後でも声や文字で残せると伝える |
| 3 | Desire | 明晰夢に近づく習慣を見せる | Reality Check / Night Mode で「続けられそう」と感じさせる |
| 4 | Memory | 夢日記として残る価値を見せる | カレンダー・一覧・詳細で振り返れる印象を残す |
| 5 | Action | 具体的な次の行動を見せる | 就寝前にNight Modeを開始する行動を想起させる |
| 6 | Memory / Action | 分析で継続価値を補強 | 記録がスコアや傾向に変わることを見せる |

---

## 4. スクリーンショット構成

制作枚数は6枚を推奨する。既存の5枚構成は概ね使えるが、v1.0仕様とAIDMAに合わせて「WakeUp / Night Mode開始導線」を追加し、順序を調整する。

### 01_attention_home.png

| 項目 | 内容 |
| --- | --- |
| AIDMA | Attention |
| 画面 | Dashboard |
| 大見出し | `夢を記録して、明晰夢の習慣へ` |
| サブコピー | `Recall Score と連続記録で、毎朝の夢を振り返れます。` |
| 画面内で見せる要素 | 今日のRecall Score、Growth Index、連続記録、最近の夢、夢記録ボタン |
| 意図 | 商品ページの1枚目で「夢日記 + 明晰夢トレーニング」だと理解させる |

注意:

- 「明晰夢を見られる」「明晰夢になる」など成功保証に見える表現は使わない。
- 既存の `LucidDream` ロゴは `Dreave` に修正する。

### 02_interest_record.png

| 項目 | 内容 |
| --- | --- |
| AIDMA | Interest |
| 画面 | Dream Entry |
| 大見出し | `起きた直後に、すばやく残す` |
| サブコピー | `文字・音声・スケッチで、夢の断片まで記録できます。` |
| 画面内で見せる要素 | テキスト入力、録音ボタン、感情タグ、明晰夢フラグ、スケッチ導線 |
| 意図 | 夢を忘れる前に記録できる手軽さを伝える |

注意:

- 音声認識はApple Speech利用なので「AIが音声を解析」のような誤解を避ける。
- 夢本文は架空データを使い、個人情報に見える内容は入れない。

### 03_desire_reality_check.png

| 項目 | 内容 |
| --- | --- |
| AIDMA | Desire |
| 画面 | Reality Check |
| 大見出し | `日中の確認を、夢の中の気づきへ` |
| サブコピー | `通知でReality Checkを続け、気づく習慣を育てます。` |
| 画面内で見せる要素 | 今日の達成数、通知回数、確認セッション、過去ログ |
| 意図 | 明晰夢トレーニングらしい差別化を見せる |

注意:

- 「夢の中で必ず気づく」は禁止。
- 通知許可が必要な機能だとわかるが、強制感は出さない。

### 04_memory_journal.png

| 項目 | 内容 |
| --- | --- |
| AIDMA | Memory |
| 画面 | Dream Journal |
| 大見出し | `夢日記で、記憶を育てる` |
| サブコピー | `一覧・カレンダー・タグで、夢の変化をあとから見返せます。` |
| 画面内で見せる要素 | 日付グループ、カレンダー、検索/フィルター、夢詳細カード |
| 意図 | 夢を記録し続ける理由を残す |

注意:

- 既存スクリプトの2枚目は記録入力とカレンダーが混在している。記録入力は2枚目に寄せ、4枚目は日記閲覧に特化する。

### 05_action_night_mode.png

| 項目 | 内容 |
| --- | --- |
| AIDMA | Action |
| 画面 | Night Mode Setup / WakeUp |
| 大見出し | `眠る前から、起きた後まで` |
| サブコピー | `就寝時刻を設定し、朝の振り返りと夢記録へつなげます。` |
| 画面内で見せる要素 | 就寝時刻、REM推定、刺激予定、環境音、開始ボタン、WakeUp後の夢記録導線 |
| 意図 | アプリをインストールした後の具体的な使い始め方を想像させる |

注意:

- 40Hz刺激は「明晰夢を発生させる」と断定しない。
- 睡眠改善・治療効果に見える文言は避ける。

### 06_memory_analytics.png

| 項目 | 内容 |
| --- | --- |
| AIDMA | Memory / Action |
| 画面 | Analytics |
| 大見出し | `記録が、傾向に変わる` |
| サブコピー | `スコア推移、明晰夢率、よく出るテーマを振り返れます。` |
| 画面内で見せる要素 | Recall Score推移、夢記録数、明晰夢数、感情分布、ドリームサイン |
| 意図 | 継続利用の価値を最後に補強する |

注意:

- AI分析を出す場合は「AIによる傾向コメント」程度に留める。
- 「広告を見てAI分析を更新」はv1.0で存在する可能性があるが、初回スクリーンショットでは前面に出さない。無料MVPの説明と混乱しやすいため。

---

## 5. 任意App Preview動画仕様

### 5.1 位置づけ

App Preview動画は任意。初回リリースでは、静止画6枚が完成してから追加する。動画を入れる場合、スクリーンショットより先に表示されるため、動画のポスター frame は `01_attention_home.png` と同じ訴求にする。

### 5.2 推奨構成

| 秒数 | 内容 |
| ---: | --- |
| 0-3 | Dreaveロゴ + Dashboard。夢記録と明晰夢習慣のアプリだと示す |
| 3-7 | Dream Entry。音声/文字/タグで記録する |
| 7-11 | Reality Check。日中の確認習慣を見せる |
| 11-15 | Night Mode。就寝前設定からWakeUp導線へ |
| 15-18 | Analytics。記録がスコアと傾向になる |

推奨長さ: 15-20秒。  
ファイル名: `app_preview_6_5inch.mp4`

### 5.3 技術要件

| 項目 | 指定 |
| --- | --- |
| codec | H.264 |
| frame rate | 30 fps |
| pixel format | yuv420p |
| container | mp4 |
| 音声 | 原則なし。App Store Connectで弾かれる場合のみ無音AACトラックを追加 |
| 解像度 | Apple公式のApp Preview受理解像度に合わせるなら 886 x 1920 portrait。現状の 1242 x 2688 はアップロード前に検証する |

---

## 6. 既存資産の評価と修正対象

既存:

- `AppStoreAssets/iphone_65/01_hero_dream_record.png`
- `AppStoreAssets/iphone_65/02_dream_journal.png`
- `AppStoreAssets/iphone_65/03_reality_check.png`
- `AppStoreAssets/iphone_65/04_rem_cycle.png`
- `AppStoreAssets/iphone_65/05_dream_analysis.png`
- `AppStoreAssets/iphone_65/app_preview_6_5inch.mp4`
- `AppStoreAssets/iphone_65/preview_contact_sheet.png`

現状確認:

- PNGはすべて `1242 x 2688` で6.5インチスクリーンショット要件に合っている。
- MP4は H.264 / 1242 x 2688 / 30fps / 18秒 / yuv420p。
- 既存スクリプト `scripts/generate_appstore_assets.py` は日本語・英語セットを生成できる。

修正対象:

1. ブランド表記を `LucidDream` から `Dreave` に変更する。
2. Contact Sheetタイトルも `Dreave App Store Screenshot Preview` に変更する。
3. 画像内の画面タイトル・文言をv1.0仕様に合わせる。
4. `02_dream_journal.png` は「記録入力」に寄せ、別途「夢日記閲覧」画像を追加する。
5. `04_rem_cycle.png` はNight Mode / WakeUp文脈を強め、REM推定だけの理屈説明にならないようにする。
6. `05_dream_analysis.png` はProや広告を連想させない表現にする。
7. 英語版 `AppStoreAssets/iphone_65_en` は日本語版確定後に同じ構成で更新する。

---

## 7. コピーライティング基準

### 7.1 使ってよい表現

- `夢を記録する`
- `明晰夢の習慣を育てる`
- `眠る前後の習慣を整える`
- `夢の記憶を振り返る`
- `Recall Scoreで見える化`
- `Reality Checkを続ける`
- `REM推定タイミングを確認`
- `傾向を振り返る`

### 7.2 避ける表現

- `明晰夢を必ず見られる`
- `睡眠の質が改善する`
- `睡眠を治す`
- `睡眠状態を診断`
- `科学的に証明`
- `脳を変える`
- `成功率を上げる` の断定
- `HealthKit連携`
- `Apple Watch対応`
- `Proで解放`
- `DreamPass`

### 7.3 訴求コピー候補

| 用途 | コピー |
| --- | --- |
| 1枚目 | `夢を記録して、明晰夢の習慣へ` |
| 2枚目 | `起きた直後に、すばやく残す` |
| 3枚目 | `日中の確認を、夢の中の気づきへ` |
| 4枚目 | `夢日記で、記憶を育てる` |
| 5枚目 | `眠る前から、起きた後まで` |
| 6枚目 | `記録が、傾向に変わる` |

---

## 8. 生成・検収条件

### 8.1 ファイル出力

推奨出力:

```text
AppStoreAssets/iphone_65/
  01_attention_home.png
  02_interest_record.png
  03_desire_reality_check.png
  04_memory_journal.png
  05_action_night_mode.png
  06_memory_analytics.png
  preview_contact_sheet.png
  app_preview_6_5inch.mp4
```

既存ファイル名を維持する場合:

```text
01_hero_dream_record.png
02_dream_record.png
03_reality_check.png
04_dream_journal.png
05_night_mode.png
06_dream_analysis.png
```

### 8.2 画像検収

必須チェック:

- `sips -g pixelWidth -g pixelHeight AppStoreAssets/iphone_65/*.png` で全スクリーンショットが `1242 x 2688`。
- RGB PNG。透過なし。
- 画面内にDreaveの実機能と一致するUIが入っている。
- 1枚目から3枚目だけを見ても、アプリの用途・価値・使い方が伝わる。
- すべての文字が端末モック、ノッチ、画面端、安全領域と重ならない。
- 小さな文字もApp Store表示で読める。重要コピーは大きく短くする。
- 医療、診断、治療、保証、未実装機能、課金誘導がない。

### 8.3 動画検収

必須チェック:

```sh
ffprobe -v error \
  -show_entries stream=codec_name,width,height,r_frame_rate,duration,pix_fmt \
  -show_entries format=duration,format_name,size \
  -of default=noprint_wrappers=1 \
  AppStoreAssets/iphone_65/app_preview_6_5inch.mp4
```

確認項目:

- codec_name: `h264`
- r_frame_rate: `30/1`
- duration: `15` から `30` 秒の範囲
- pix_fmt: `yuv420p`
- App Store Connectで受理される解像度か事前確認する

---

## 9. 実装メモ

既存の `scripts/generate_appstore_assets.py` をベースに改修するのが最短。

改修ポイント:

1. `draw_brand()` の固定文字列を `Dreave` に変更する。
2. `preview_contact_sheet()` のタイトルを `Dreave App Store Screenshot Preview` に変更する。
3. `ja_specs` を6枚構成に変更する。
4. 画面生成関数を以下に整理する。
   - `dashboard_screen()`
   - `dream_record_screen()`
   - `reality_check_screen()`
   - `dream_journal_screen()`
   - `night_mode_screen()`
   - `analytics_screen()`
5. `app_preview_video()` はApple公式App Preview受理解像度への書き出しオプションを追加検討する。

---

## 10. 次工程

1. この仕様書に沿って `scripts/generate_appstore_assets.py` を改修する。
2. 日本語版6枚を生成する。
3. Contact Sheetで一覧確認する。
4. `sips` / `ffprobe` でサイズ検証する。
5. 画像内文言をApp Storeメタデータと突き合わせる。
6. 必要なら英語版も同構成で更新する。
