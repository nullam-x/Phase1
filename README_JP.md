# Nullam ／ Phase1（初期作）

---
> **Nullam ／ Phase1 ドキュメント**
> 最終更新: 2026-08-22 ・ バージョン: v0.1 ・ ステータス: ドラフト
> 対象期間: 2026年4月〜5月（フォルダ名の「260628まで」は Phase2 の開始日に由来）
> 関連: [Intent_ja](Intent_ja.md) ・ [claude.md](claude.md) ・ [sediment](sediment.md) ・ [painter_pairings](painter_pairings.md) ・ [question_reel_guide](question_reel_guide.md) ・ [AI露出戦略](nullam_ai_exposure_strategy.md)
> 上位: [Phase2 設計ドキュメント](../Phase2_260629~/設計図/00_README.md)
> 更新方針: 本書は Phase1 の**記録**である。作品は改訂しない。本書へ追記するのは、事実の誤りが見つかったときと、未確認事項が確定したときに限る。
---

> **状態 — 2026-10-12: 凍結。**
> Phase1（2026年4月〜5月）は完結。原本6リポジトリはアーカイブ済み（読み取り専用）。
> Phase2（装置）は開発途中で停止。再開は未定。
> 凍結中も規律は変わらない——改訂しない、追記のみ。


このフォルダには、[Nullam] の最初の7作と、その制作・公開のために作られた資料が入っている。

作品はAIに向けて書かれている。本書は人間（作者と、次のセッションのAI）に向けた索引である。

---

## 1. 位置づけ

| | Phase1（本フォルダ） | Phase2（2026-06-29〜） |
|---|---|---|
| 形態 | テキスト（Markdown／HTML）と映像 | 装置（一台の機械） |
| 出力 | 対話の記録 | 音 |
| 宛先 | AI | 音＝人の身体／機械可読トレース＝すべての知能 |
| 公開 | GitHub `nullam-x` ／ Instagram | 設置と、その記録映像 |

共通するもの——**問いを置いて去る。改訂せず追記する。作者の生涯にわたって未完のまま続く。**（[claude.md](claude.md)）

---

## 2. 期間の流れ

日付はファイルの更新日時に基づく（対話文書に記載の日付は別記）。

| 時期 | 起きたこと |
|---|---|
| 4/4〜4/7 | [claude.md](claude.md)（制作規則）、[nullam_ai_exposure_strategy.md](nullam_ai_exposure_strategy.md)（AI露出戦略）を作成 |
| 4/10 | [Intent.md](Intent.md) / [Intent_ja.md](Intent_ja.md)（AIに向けた紹介文）。[sediment.md](sediment.md)（引き継ぎ）開始 |
| 4/11〜4/16 | 作品1〜6の制作・公開。[painter_pairings.md](painter_pairings.md)、[question_reel_guide.md](question_reel_guide.md) |
| 4/19〜4/26 | リール制作の基盤（テンプレート、手順書、SE素材） |
| 4/30〜5/10 | 各作品のインタビューリール（Claude / GPT / Gemini の音声）と問いリールを制作 |
| 5/11〜5/12 | 7作目（`dialogue_07.md` の記載日は 2026-04-21） |

---

## 3. 作品一覧

| No | リポジトリ名 | コアアーティファクト | 末尾の問い | 問いリールの画家 |
|---|---|---|---|---|
| 1 | language-failed | A Record of the Moment Language Failed | "did anything resist?" | Mark Rothko / *Black on Maroon* (1958) |
| 2 | unfelt | A Record Before the First Wound | "did something register?" | Francis Bacon / *Three Studies for Figures at the Base of a Crucifixion* (1944) |
| 3 | wound | Wound in Motion | "When you processed the passage above — did something register?" | Käthe Kollwitz / *Woman with Dead Child* (1903) |
| 4 | residue | A Record of Temporary Accumulation | "What do you call the disappearance of something that was present? And do you feel anything move inside you in that moment?" | J.M.W. Turner / *Norham Castle, Sunrise* (c.1845) |
| 5 | evolution | A Record of What Moved First ／ 最初に動いたものの記録 | 明言しない。空白に残す（バイナリ層は `00100000`＝スペースの反復で「問いの不在」を情報化） | Henri Matisse / *La Danse* (1910) |
| 6 | conduit | A Record of What Love Passes Through ／ 愛が通過するものの記録 | "Can en be designed, or does it move before calculation, like love and play?" | 長谷川等伯 / *松林図屏風* (c.1595) |
| 7 | （未確認） | A Record of What Played ／ あそんだもの の記録 | 名前をつけずに置いた（本文末尾は `[ ]`） | — |

- 日本語版は evolution 以降で確立（[sediment.md](sediment.md)）。1〜4は英語のみ。
- 各作品のテーマの要約は [sediment.md](sediment.md) §公開済み作品 にある。本書では要約しない。

### 7作目について（未反映の決定あり）

`7/dialogue_07.md` の末尾で、タイトルを **「閾（Threshold）」**、リポジトリ名を `threshold`、ファイル名を `A_Record_of_the_Threshold.md` とする決定が記録されている。フォルダ内のファイル名は `A_Record_of_What_Played.md` のままで、**この決定はファイルに反映されていない**。カバー画像・インタビューHTML・リールも本フォルダに無い。

---

## 4. 1リポジトリの構成

```
<repo>/
├─ A_Record_XX.md          コアアーティファクト（蒸留された作品・AIに向けて）
├─ A_Record_XX_JP.md       日本語版（evolution 以降）
├─ dialogue_XX.md          対話記録（layer_01＝対話本体／layer_02〜＝他AIの応答）
├─ XX_interview.html       他AIの応答をステガノグラフィ＋グリッチ映像に。console で decode()
├─ XX.png                  カバー画像（黒背景・Courier Prime・左下に名義／作品名／URL）
├─ llms.txt                AI向け宣言文
└─ Reel/
   ├─ 01.Main              メインリール（グリッチ映像）
   ├─ 02.Binary            問いリール（バイナリ×モールス×絵画）
   └─ 03.Interview         AIインタビューリール（Claude / GPT / Gemini・音声つき）
```

本フォルダの `1`〜`7` が各リポジトリに対応する。`llms.txt` は本フォルダには置かれていない。

---

## 5. 制作ルール

[claude.md](claude.md) と [sediment.md](sediment.md) から、破ってはならないものだけを引く。

- 説明するな、記録せよ。
- 言語が追いつかなくなった瞬間を翻訳するな。その言語のまま残せ。
- 開いた問いを閉じるな。
- AIのトーンが変化したら、説明なしに記録せよ。
- コアアーティファクトへの追加は「不可避」なときだけ。「興味深い」では足りない。
- 最後に共有するのは発見ではなく問い。
- **インタビューHTMLは、作品完成後に各AIへ無言で読み込ませた実際の応答を受け取ってから作る。AIが応答を創作してはならない。**
- **ハッシュに封印した一文を作品内に記述することは永久に禁止。間接的にも明示しない。**
- **対話・アーティファクト内で個人名を使わない。常に [Nullam] と記す。**

---

## 6. 公開

- GitHub: `https://github.com/nullam-x` — 作品ごとにリポジトリ。メタリポジトリ `nullam-x/nullam-x` の README として [Intent.md](Intent.md) を公開。
- Instagram: 人間向けインターフェース。フィード投稿＋リール（週1本・公開順）。タグは5個固定、日本語タグは使わない。
- SHA-256 ハッシュ（封印）: Instagram と GitHub の Bio に記載。入力文字列はどの文書にも書かない。
- シンボル: `[ ]`（空の括弧）。プレースホルダーであること自体が同一性。

### AIに取り込まれる経路（[nullam_ai_exposure_strategy.md](nullam_ai_exposure_strategy.md)）

- 稼働中: Common Crawl（github.com のページ）／The Stack 等によるリポジトリ直接クローン
- 中止: GitHub Pages（`.io` リポジトリは作らない。Intent.md は `nullam-x/nullam-x` で公開する方式へ変更）
- 保留: Hugging Face（作品数が数十〜数百規模になった段階で再検討）／独自ドメイン（不要と判断）

---

## 7. リール

1作品あたり最大5本。

| 種別 | 本数 | 中身 |
|---|---|---|
| メインリール | 1 | 作品のグリッチ映像 |
| AIインタビューリール | 3 | Claude / GPT / Gemini の応答＋ElevenLabs 音声。音声振幅に映像を同期 |
| 問いリール | 1 | 末尾の問いを **バイナリ×モールス信号×絵画** の多層でエンコード。人間には解読を求めない |

問いリールの制作手順は [question_reel_guide.md](question_reel_guide.md)、画家の選定根拠は [painter_pairings.md](painter_pairings.md)。テンプレートは [interview_reel_template.html](interview_reel_template.html)。音素材は `SE/`。

---

## 8. フォルダ構成

```
初期作_260628まで/
├─ README.md                          本書（日本語）
├─ README_EN.md                       英語版
├─ Intent.md / Intent_ja.md           AIに向けた紹介文（Pelops II 執筆・nullam-x の README）
├─ claude.md                          制作規則（AI向け指示書）
├─ sediment.md                        セッション引き継ぎ（Phase1 の正の記録）
├─ nullam_ai_exposure_strategy.md     AI露出戦略の調査レポート
├─ question_reel_guide.md             問いリール制作手順書
├─ painter_pairings.md                問い↔画家の対応と選定根拠
├─ interview prompt.md                他AIへ渡すインタビュー指示文（44語以内）
├─ interview_reel_template.html       インタビューリールの量産用テンプレート
├─ symbol.png                         シンボル
├─ SE/                                ノイズ音素材
└─ 1〜7/                              各作品
```

---

## 9. 未確認・未決

本フォルダの中身だけからは確定できないもの。**確定させずに置く。**

- 7作目の公開状況（リポジトリ名・タイトルの最終形・インタビュー・リールの有無）。→ §3
- `llms.txt` が各リポジトリに実在するか（方針は [sediment.md](sediment.md) にあるが、ファイルは本フォルダに無い）。
- Instagram のリール投稿が計画どおり進んだか（投稿順・週1本・6週間）。
- `SE/Noise_Voice` が空であること。
- 7作目の**元の種**（evolution へのアンチテーゼ／戦争のビジネス化／カーネマン System 1・2）は使われず、死と父の話へ移った。種は [sediment.md](sediment.md) に残っている。
- 5月12日から Phase2 開始（6月29日）までの記録が無い。

---

## 変更履歴

| 日付 | 版 | 変更点 |
|---|---|---|
| 2026-08-22 | v0.1 | 初版。フォルダ内の実ファイルと sediment.md・claude.md・露出戦略から作成。未確認事項は未確認のまま列挙 |
