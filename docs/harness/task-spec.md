# タスク仕様書: cpsc-proposal リニューアル + ポートフォリオ更新

## 目的
2026年3月29日の旧CPSC対応提案書は「Item Specifics変更」「EAGLE参考ID」等のシステム対応策に焦点を当てていたが、その後のリサーチで「自作CPCは不可能」「アパレルにも注意が必要」という新しい論点が判明した。この新しい知見を反映した公開資料を作成し、既存の cpsc-proposal リポジトリを更新する。あわせて、ポートフォリオの該当プロジェクトの説明文を新内容に合わせて更新する。

## 変更対象ファイル

1. **`/Users/naokijodan/Desktop/cpsc-proposal/index.html`**（新規内容で完全置換）
2. **`/Users/naokijodan/Desktop/cpsc-proposal/legacy.html`**（新規ファイル、旧index.htmlをここに退避）
3. **`/Users/naokijodan/Desktop/プロジェクト/portfolio/index.html`**（cpsc-proposal プロジェクトの description のみ更新）

## 参考資料（必ず読むこと）

- `/Users/naokijodan/Desktop/cpsc-proposal/docs/harness/research-report.json`（玩具・フィギュア編）
- `/Users/naokijodan/Desktop/cpsc-proposal/docs/harness/research-report-apparel.json`（アパレル編）

## cpsc-proposal/index.html の仕様

### タイトル
**「7月以降の新品玩具・フィギュア販売をどうするか — CPSC新規制の考察」**

ブラウザタブ用: `7月以降の新品玩具・アパレル販売 — CPSC新規制の考察`

### 構成（6セクション + フッター）

```
[ヘッダー]
  タイトル（上記）
  サブタイトル: 「2026年7月8日 CPSC新規制を前にしたリサーチと考察」
  公開日: 2026年4月8日
  作成者: naokijodan

[セクション1] 背景 — 何が起きるのか
  ・2026年7月8日、米国CPSCが製品安全書類の電子申告（eFiling）を義務化
  ・対象: 子ども向け製品（CPC必要）、特定アパレル（GCC必要）、一般規制対象品（GCC必要）
  ・違反リスク: 通関で保留・発送不可・米国販売権限停止・アカウント制限

[セクション2] 最初に考えた案
  ・新品の玩具（シルバニア等）を米国で売る場合、「コレクターズアイテム扱い」にするのはグレー
  ・ならば、自作ツールでCPC書類を作れないか？と考えた
  ・旧提案書（legacy.html）ではItem Specifics変更やEAGLE参考ID設定を検討していた

[セクション3] 調べてわかったこと（リサーチ結果）

  3-1. 玩具・フィギュア編
    ・書類（CPC）自体は自作可能だが、その根拠となる試験結果は CPSC認定第三者試験所のものが必須
    ・公開情報やメーカーのウェブ情報では代用できない
    ・玩具は複数規則が同時適用: ASTM F963、鉛塗料、フタル酸、総鉛、小部品、磁石等
    ・1SKUあたり試験費用 500〜1,500 USD（約7万〜22万円）
    ・小規模事業者免除（SBM）でも化学試験は免除されない
    ・シルバニア・トミカ等は客観的に「子ども向け」と判定される
    ・「17歳以上向け」と虚偽ラベルは意図的規制回避とみなされるリスク

  3-2. アパレル編
    ・大人用アパレルはGCCで済む（自己認証可、第三者試験不要）
    ・免除素材: ポリエステル、ウール、ナイロン、アクリル、モダクリル、オレフィン（100%または混紡）
    ・免除基準: 平織りで2.6oz/平方ヤード（約88.2g/㎡）以上の生地は素材問わず免除
    ・要注意: 薄手綿（薄いTシャツ、浴衣）、薄手シルク（スカーフ、着物）、起毛素材
    ・子ども用アパレルはCPC必要（第三者試験必須）
    ・子ども用パジャマ・寝巻きは最高リスク（16 CFR 1615/1616）
    ・中古アパレルは Disclaimer B (Code 130.006) で申告

[セクション4] カテゴリ別リスク表

  表形式で、玩具・フィギュア・アパレル・中古品を横断して、
  - 証明書の種類（CPC/GCC/なし/Disclaimer）
  - 第三者試験の要否
  - 中古免除の可否
  - 備考
  を一覧できる表を掲載する

  主要行:
  - 大人用一般アパレル（ポリエステル・ウール・厚手綿）
  - 子ども用アパレル
  - 子ども用パジャマ・寝巻き
  - 着物・浴衣（大人用）
  - ヴィンテージ古着
  - スカーフ、帽子、手袋
  - 新品玩具（シルバニア、トミカ等）
  - 中古玩具
  - フィギュア・人形の服
  - 大人向けコレクターエディション玩具

[セクション5] 今後の選択肢（4つ）

  順序:
  1. 中古品に絞る — CPC義務から免除（Exclusion Code申告のみ）
  2. 新品を「箱なし中古」として出品 — 開封・箱処分でUsed扱い（ただしグレーゾーン）
  3. 新品はコレクター用（14歳以上対象）と明確に記載 — 客観的特徴を備えた商品のみ
  4. メーカー仕入れルートの開拓 — 正規卸から試験レポートを入手できる関係を作る

  補足: 米国市場撤退 + EU/UK/AUへのシフトも選択肢として言及

[セクション6] 参考資料・出典

  ・CPSC公式:
    - eFiling: https://www.cpsc.gov/eFiling
    - 第三者試験必要規則リスト: https://www.cpsc.gov/Business--Manufacturing/Testing-Certification/Lab-Accreditation/Rules-Requiring-Third-Party-Testing
    - Secondary Market Resellers: https://www.cpsc.gov/Business--Manufacturing/Business-Education/Secondary-Market-Resellers-Thrift-Stores-and-Relief-Organizations
    - CPSC認定試験所検索: https://www.cpsc.gov/cgi-bin/labsearch/
    - Clothing guidance: https://www.cpsc.gov/Business--Manufacturing/Business-Education/Business-Guidance/Clothing
  ・eCFR 連邦規則:
    - 16 CFR Part 1107 (Testing and Labeling)
    - 16 CFR Part 1110 (Certificates of Compliance)
    - 16 CFR Part 1200 (Children's Product Definition)
    - 16 CFR Part 1250 (Children's Toys / ASTM F963)
    - 16 CFR Part 1303 (Lead in paint)
    - 16 CFR Part 1307 (Phthalates)
    - 16 CFR Part 1610 (Wearing apparel flammability)
    - 16 CFR Part 1615/1616 (Children's sleepwear)
    - 16 CFR Part 1109 (Component Part Testing)
  ・旧提案書（検討経緯）: legacy.html へのリンク
  ・詳細リサーチデータ:
    - 玩具編: docs/harness/research-report.json
    - アパレル編: docs/harness/research-report-apparel.json

[フッター]
  ・免責事項: 「本資料はリサーチに基づく考察であり、法的助言ではない。最終判断は公式情報と専門家に確認のこと。」
  ・公開日と更新履歴
  ・リポジトリリンク: https://github.com/naokijodan/cpsc-proposal
```

### デザイン方針

- **単一HTML、外部依存なし**（GitHub Pagesで即公開可能）
- **スクロール2〜3画面で読み終わる分量を想定**（詳細はリンク先で）
- **レスポンシブ**（スマホ表示対応）
- **読みやすさ優先**:
  - サンセリフフォント（-apple-system, 'Noto Sans JP'等）
  - 本文幅 max-width 720px（デスクトップ時）
  - 左右パディング、セクション間の余白を十分に確保
  - 見出し階層を明確に
- **色**: 落ち着いた配色（白背景 + 濃いグレー文字 + アクセント色1〜2色）
- **カテゴリ別リスク表**: シンプルなテーブル、モバイルで横スクロール可能に
- **コールアウト**: ⚠️（赤系）で Red Flags を強調
- **リンク**: 外部リンクは新しいタブで開く（target="_blank" rel="noopener noreferrer"）
- **絵文字は最小限**（セクションタイトルには使わない、警告記号のみ許可）

### 禁止事項（実装側）

- 外部CSS/JSライブラリの読み込み禁止（Tailwind、Bootstrap等）
- CDNからのフォント読み込み禁止（システムフォントのみ）
- トラッキングスクリプト（GA等）禁止
- HTMLファイルサイズは30KB以内を目安
- 「素晴らしい」「完璧」等の過度な賞賛表現禁止
- 事実と推測を混在させない（断定口調を避ける、推測は「〜と考えられる」等）

## legacy.html の仕様

旧 index.html の内容をそのまま移す。ファイル先頭にメモとして以下を追加:
```html
<!-- このページは 2026年3月29日 時点での旧提案書です。現在の考察は index.html を参照してください。 -->
```

ページ内にも上部にバナーで「この提案書は旧版です。最新版はこちら → [index.html]」というリンクを追加する。

## portfolio/index.html の更新仕様

### 変更箇所（1箇所のみ）

cpsc-proposal プロジェクトの description を以下に更新:

**旧**:
```
CPSC対応提案書 — eBay出品における米国製品安全規制（2026年7月施行）への対応方針。API調査に基づく3パターンの解決策を提示
```

**新**:
```
2026年7月CPSC新規制の考察 — 新品玩具・フィギュア・アパレルの米国販売をどうするか。書類自作の可否、中古シフト、免除素材の判定など、リサーチに基づく現実的な選択肢を整理
```

それ以外のHTML構造・スタイルは一切変更しない。

## 受け入れ基準

1. ✅ cpsc-proposal/index.html が新構成（6セクション）で書かれている
2. ✅ 玩具編・アパレル編の両方のリサーチ内容が反映されている
3. ✅ カテゴリ別リスク表が存在し、主要行が含まれている
4. ✅ 4つの選択肢が明記されている
5. ✅ 参考資料リンクがCPSC公式・eCFR・詳細リサーチJSONを含む
6. ✅ legacy.html が作成され、旧index.htmlの内容が退避されている
7. ✅ legacy.html の上部にバナーが追加されている
8. ✅ portfolio/index.html の該当description が新内容に更新されている
9. ✅ 外部CSS/JS依存がない（単一HTML）
10. ✅ モバイル表示で読みやすい
11. ✅ 事実と推測が区別されている
12. ✅ HTMLファイルサイズが30KB以内
13. ✅ 免責事項（法的助言ではない旨）が記載されている

## 実装後のレポート

完了したら `/Users/naokijodan/Desktop/cpsc-proposal/docs/harness/implementation-report.json` に以下を書く:

```json
{
  "session_type": "implement",
  "task_id": "cpsc-proposal-renewal",
  "status": "complete",
  "timestamp": "ISO8601",
  "summary": "cpsc-proposal/index.html 新規作成、legacy.html退避、portfolio description更新",
  "files_changed": [
    "/Users/naokijodan/Desktop/cpsc-proposal/index.html",
    "/Users/naokijodan/Desktop/cpsc-proposal/legacy.html",
    "/Users/naokijodan/Desktop/プロジェクト/portfolio/index.html"
  ],
  "file_sizes": {
    "index.html": "XX KB",
    "legacy.html": "XX KB",
    "portfolio/index.html": "XX KB"
  },
  "acceptance_criteria_status": {
    "1": "PASS/FAIL",
    "2": "PASS/FAIL"
  },
  "notes": "実装時の判断や懸念事項"
}
```

## 禁止事項（子A実装セッション）

- **git commit, git push 禁止** — 子Cの役割
- **ブラウザでの動作確認以外の外部アクセス禁止**
- **仕様の勝手な変更禁止** — 疑問点はimplementation-reportのnotesに書く
- **docs/harness/配下のJSON・ルールファイルの改変禁止**
