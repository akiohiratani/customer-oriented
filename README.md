# 顧客志向学習エージェント 使い方

## 概要

このリポジトリは、クラウドワークスの実案件を教材にして、顧客志向をステップバイステップで学ぶための作業環境です。

目的は、単にバナーを作ることではありません。

案件文・添付画像・制約条件をもとに、以下を学びます。

- 案件文から重要な事実を抜き出す
- 顧客が本当に達成したい目的を考える
- 広告を見るターゲットの状況や心理を考える
- 複数の草案を比較する
- AIペルソナ対話でコンセプトを作る
- 訴求軸を決める
- Canvaで制作できるデザイン指示書に落とし込む
- 制作物をレビューする
- 提出文と学習ログを作る

---

## 事前準備

Codexを起動する前に、このフォルダに `AGENTS.md` があることを確認します。

```text
crowdworks-customer-thinking/
  AGENTS.md
  README.md
```

PowerShell またはターミナルで、このフォルダへ移動します。

```powershell
cd crowdworks-customer-thinking
```

Codexを起動します。

```powershell
codex
```

---

## 基本の流れ

### 1. 学習を開始する

Codexに以下を入力します。

```text
顧客志向学習開始
```

すると、Codexが案件ごとの作業フォルダを作成します。

```text
sessions/YYYYMMDD_HHMM_new_case/
  README.md
  assets/
  outputs/
```

以後、その案件の画像や出力ファイルは、このフォルダ内で管理します。

---

## 作業フォルダの構成

案件ごとに、以下のようなフォルダが作成されます。

```text
sessions/YYYYMMDD_HHMM_案件名/
  README.md
  assets/
  outputs/
```

画像ファイルは `assets/` に保存します。

```text
sessions/YYYYMMDD_HHMM_案件名/assets/product_01.jpg
sessions/YYYYMMDD_HHMM_案件名/assets/scene_01.jpg
sessions/YYYYMMDD_HHMM_案件名/assets/reference_01.png
sessions/YYYYMMDD_HHMM_案件名/assets/preference_01.png
```

分析結果や制作指示書は `outputs/` に保存されます。

```text
sessions/YYYYMMDD_HHMM_案件名/outputs/01_input_summary.md
sessions/YYYYMMDD_HHMM_案件名/outputs/02_step1_facts.md
sessions/YYYYMMDD_HHMM_案件名/outputs/03_step2_customer_goal.md
```

---

## 2. 案件情報を入力する

Codexが入力テンプレートを表示したら、クラウドワークスの「仕事の詳細」と、添付画像の情報を貼ります。

入力の先頭には、以下を付けます。

```text
案件情報入力
```

例：

```text
案件情報入力

【案件基本情報】
案件名：Rollite多機能バッグ 広告用バナー制作
案件URL：
依頼形式：コンペ
カテゴリ：広告用バナー
報酬：1枚 2,000円（税込）
締切：未記載

【仕事の詳細】
依頼内容全文または要約：
40〜50代向けの多機能バッグ「Rollite多機能バッグ」の広告用バナー画像を制作する案件。
Meta（Instagram／Facebook）広告用の正方形バナー。
商品の一番の訴求ポイントは「容量が変わる」こと。
派手すぎず、ナチュラルでおしゃれ、落ち着いた印象が求められている。

【制作物】
制作物の種類：広告用バナー
使用用途：Meta広告、Instagram広告、Facebook広告
サイズ指定：1080px × 1080px
静止画・動画の別：静止画
納品形式：JPGまたはPNG、RGBカラー

【使用素材】
添付画像の有無：あり
画像ファイル名：
- sessions/YYYYMMDD_HHMM_案件名/assets/product_01.jpg：商品単体画像
- sessions/YYYYMMDD_HHMM_案件名/assets/scene_01.jpg：利用シーン画像
- sessions/YYYYMMDD_HHMM_案件名/assets/preference_01.png：希望イメージのスクショ

画像使用ルール：
- 利用シーン画像1枚のみ
- 物撮り画像1枚のみ
- 利用シーン1枚＋物撮り1枚
- 複数画像の詰め込みNG
- 矢印やイラスト追加OK

【バナー内に入れる文言】
メインキャッチコピー：行きは身軽に、帰りは大容量で。
サブコピー：-5way・軽量・撥水・多収納-
必須文言：上記2つ
任意文言：未記載
CTA文言：未記載

【商品・サービス情報】
商品名：Rollite多機能バッグ
商品ページURL：
商品の特徴：5way、軽量、撥水、多収納、容量が変わる
一番訴求したい特徴：容量が変わる
ターゲット：40〜50代の男女
見た人に取ってほしい行動：広告から販売ページへ興味を持ってもらうこと

【デザイン条件】
希望イメージ・トンマナ：
派手すぎず、ナチュラルでおしゃれ。
40〜50代男女向けの落ち着いた印象。
文字は見やすさ重視。

避けたい表現：
派手すぎる表現。
複数画像を詰め込むこと。

色・フォントの希望：未記載

希望イメージの指定：
- 単色寄り
- シンプル寄り
- 気軽寄り
- やや高級寄り
- 伝統的と先進的の中間
- 女性的と男性的の中間

参考URL・参考画像：

【権利・注意事項】
著作権譲渡の有無：採用されたバナーは著作権を依頼主に譲渡
ポートフォリオ掲載可否：未記載
禁止事項・注意事項：
- 複数画像の詰め込みNG
- 著作権譲渡に同意できる方のみ応募

【今回の学習目的】
この案件を通じて特に学びたいこと：
案件文と添付画像から、顧客が求める広告バナーの方向性を読み解き、Canvaで制作できる形に落とし込む練習をしたい。
```

Codexは、案件情報を整理して以下のファイルを作成します。

```text
SESSION_DIR/outputs/01_input_summary.md
```

---

## 3. ステップ1：案件文から事実を抜き出す

Codexに以下を入力します。

```text
ステップ1へ
```

ここでは、ユーザー自身が案件文から重要だと思う事実を3〜5個選びます。

例：

```text
1. 40〜50代男女向け
2. Meta広告用バナー
3. 1080px × 1080px
4. 「容量が変わる」が一番の訴求ポイント
5. 派手すぎず、ナチュラルでおしゃれ
```

Codexは、ユーザーの回答とAIの補足を整理して、以下のファイルを作成します。

```text
SESSION_DIR/outputs/02_step1_facts.md
```

---

## 4. ステップ2：顧客の目的を考える

Codexに以下を入力します。

```text
ステップ2へ
```

ここでは、顧客が本当に達成したい目的を考えます。

例：

```text
顧客は、おしゃれな画像が欲しいだけではなく、Meta広告を見た40〜50代に「このバッグなら外出や旅行で荷物が増えても困らなそう」と感じてもらい、販売ページへの興味を高めたいのだと思います。
```

Codexは、顧客目的の仮説を整理して、以下のファイルを作成します。

```text
SESSION_DIR/outputs/03_step2_customer_goal.md
```

---

## 5. ステップ3〜6をノンストップで実行する

ステップ2が終わったら、以下のどちらかを入力します。

```text
ステップ3へ
```

または、

```text
ノンストップ実行
```

ここからは、Codexがユーザー確認なしでステップ3〜6をまとめて実行します。

実行される内容は以下です。

```text
ステップ3：ターゲットの状況と心理を考える
ステップ3.5：AIペルソナ対話で草案を比較・採用する
ステップ4：訴求軸を決める
ステップ5：訴求をデザイン要素へ翻訳する
ステップ6：Canva制作指示書を作る
```

作成されるファイルは以下です。

```text
SESSION_DIR/outputs/04_step3_target_psychology.md
SESSION_DIR/outputs/05_step3_5_persona_dialogue_draft_selection.md
SESSION_DIR/outputs/06_step4_appeal_axis.md
SESSION_DIR/outputs/07_step5_design_translation.md
SESSION_DIR/outputs/08_canva_design_spec.md
SESSION_DIR/outputs/09_gpt_canva_prompt.md
```

チャットには全文ではなく、作成ファイル一覧と、優先度1・優先度2の方向性だけが表示されます。

---

## 6. Canvaで制作する

Canva制作時は、以下のファイルを見ながら作ります。

```text
SESSION_DIR/outputs/08_canva_design_spec.md
```

基本の流れは以下です。

```text
1. Canvaを開く
2. 「カスタムサイズ」を選ぶ
3. 案件指定サイズを入力する
4. 空白デザインを作成する
5. assets内の画像をアップロードする
6. 優先度1デザイン案を先に作る
7. 余裕があれば優先度2デザイン案も作る
8. PNGまたはJPGで書き出す
```

制作途中で迷ったら、以下のファイルにあるプロンプトをChatGPTに貼って相談します。

```text
SESSION_DIR/outputs/09_gpt_canva_prompt.md
```

---

## 7. 制作物をレビューする

Canvaで作成した画像を、案件フォルダの `assets/` に保存します。

例：

```text
SESSION_DIR/assets/draft_01.png
SESSION_DIR/assets/draft_02.png
```

その後、Codexに以下を入力します。

```text
レビュー開始
```

Codexは、完成画像を顧客目的・バナーコンセプト・AIペルソナのニーズに照らしてレビューします。

作成されるファイルは以下です。

```text
SESSION_DIR/outputs/10_design_review.md
```

---

## 8. 提出文と学習ログを作る

最後に、Codexへ以下を入力します。

```text
提出文作成
```

Codexは、クラウドワークス提出用の文章と、学習ログを作成します。

作成されるファイルは以下です。

```text
SESSION_DIR/outputs/11_submission_message.md
SESSION_DIR/outputs/12_learning_log.md
```

---

## よく使うコマンド一覧

```text
顧客志向学習開始
案件情報入力
ステップ1へ
ステップ2へ
ステップ3へ
ノンストップ実行
レビュー開始
提出文作成
```

---

## 出力ファイル一覧

```text
SESSION_DIR/outputs/01_input_summary.md
SESSION_DIR/outputs/02_step1_facts.md
SESSION_DIR/outputs/03_step2_customer_goal.md
SESSION_DIR/outputs/04_step3_target_psychology.md
SESSION_DIR/outputs/05_step3_5_persona_dialogue_draft_selection.md
SESSION_DIR/outputs/06_step4_appeal_axis.md
SESSION_DIR/outputs/07_step5_design_translation.md
SESSION_DIR/outputs/08_canva_design_spec.md
SESSION_DIR/outputs/09_gpt_canva_prompt.md
SESSION_DIR/outputs/10_design_review.md
SESSION_DIR/outputs/11_submission_message.md
SESSION_DIR/outputs/12_learning_log.md
```

---

## 運用上の注意

新しい案件を始めるときは、必ず新しい作業フォルダを作成します。

```text
sessions/YYYYMMDD_HHMM_案件名/
```

別案件のファイルを上書きしないように注意します。

同じ案件の続きを行う場合は、既存の `SESSION_DIR` を使います。

どのフォルダを使うべきか分からない場合は、Codexに確認します。

```text
現在の作業フォルダを確認してください。
```

---

## 学習で意識すること

常に次の問いに戻ります。

```text
1. これは顧客の目的に合っているか
2. これはターゲットに伝わるか
3. 案件文のどの事実が根拠か
4. 自分の好みだけで決めていないか
5. AIペルソナの意見を事実として扱っていないか
6. ネガティブからポジティブへの変化が分かりやすいか
7. Canva上で実際に作れる形に翻訳できているか
8. 優先度1と優先度2の2案を出せているか
9. 判断に迷った場合、コンセプトとAIペルソナのニーズで判断できているか
10. 新しい案件を既存フォルダに上書きしていないか
```
