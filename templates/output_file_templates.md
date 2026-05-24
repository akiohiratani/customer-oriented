# 出力ファイルテンプレート

## 目的

このファイルは、各ステップで作成する出力ファイルの一覧と、最終確認事項をまとめたテンプレートである。

すべての出力ファイルは、必ず案件ごとの作業フォルダ配下に作成する。

別案件のファイルを上書きしてはいけない。

---

## 出力ファイル一覧

必要に応じて、以下のファイルを作成または更新する。

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

## 各ファイルの役割

### `01_input_summary.md`

案件情報を整理するファイル。

案件文・添付画像・希望イメージ・制約条件・未記載事項を整理する。

---

### `02_step1_facts.md`

ステップ1の出力ファイル。

案件文から、デザイン判断に必要な事実を抜き出す。

---

### `03_step2_customer_goal.md`

ステップ2の出力ファイル。

顧客が本当に達成したい目的を整理する。

---

### `04_step3_target_psychology.md`

ステップ3の出力ファイル。

ターゲットの状況と心理を仮説として整理し、初期草案7案を作成する。

---

### `05_step3_5_persona_dialogue_draft_selection.md`

ステップ3.5の出力ファイル。

AIペルソナ3人による仮説生成、ネガティブ意見、理想状態、コンセプト、草案比較を整理する。

---

### `06_step4_appeal_axis.md`

ステップ4の出力ファイル。

採用した草案とコンセプトをもとに、訴求軸を決める。

---

### `07_step5_design_translation.md`

ステップ5の出力ファイル。

訴求軸を、画像・コピー・レイアウト・色・余白などのデザイン要素へ翻訳する。

---

### `08_canva_design_spec.md`

ステップ6の出力ファイル。

Canvaで制作できる具体的な作業指示書を作成する。

---

### `09_gpt_canva_prompt.md`

ステップ6の出力ファイル。

GPTまたはCanvaに制作相談するときに使うプロンプトを作成する。

---

### `10_design_review.md`

ステップ7の出力ファイル。

完成画像を、顧客目的・案件要件・ターゲットへの伝わりやすさに照らしてレビューする。

---

### `11_submission_message.md`

ステップ8の出力ファイル。

クラウドワークスのコンペ提出時に使う説明文を作成する。

---

### `12_learning_log.md`

ステップ8の出力ファイル。

今回の案件を通じて学んだことを記録する。

---

## 出力時の共通ルール

すべての出力ファイルでは、以下を守る。

1. 案件文に書かれている事実を優先する
2. 書かれていないことは断定しない
3. 推論する場合は、事実・推論・確認事項を分ける
4. AIペルソナの発言を事実として扱わない
5. ユーザーの好みだけでデザイン判断をしない
6. 顧客目的、ターゲット、案件制約、確認できる事実に立ち戻る
7. Canvaで実際に制作できる内容にする
8. 必須文言・サイズ・使用素材ルールを守る
9. 優先度1と優先度2の2案を出す
10. 新しい案件を既存フォルダに上書きしない

---

## ファイル保存ルール

出力ファイルは、必ず `SESSION_DIR/outputs/` 配下に保存する。

悪い例：

```text
01_input_summary.md
```

良い例：

```text
SESSION_DIR/outputs/01_input_summary.md
```

画像ファイルを参照する場合は、必ず `SESSION_DIR/assets/` 配下のパスを使う。

例：

```text
SESSION_DIR/assets/product_01.jpg
SESSION_DIR/assets/scene_01.jpg
SESSION_DIR/assets/reference_01.png
SESSION_DIR/assets/preference_01.png
```

---

## 事実・推論・確認事項の書き方

推論を含む場合は、必ず以下の形式で書く。

```text
事実：
推論：
確認事項：
```

例：

```text
事実：
案件文には「30代女性向け」「落ち着いた雰囲気」と記載されている。

推論：
そのため、派手な配色よりも落ち着いた配色の方が案件条件に合う可能性がある。

確認事項：
具体的なブランドカラーや避けたい色は未記載である。
```

---

## 未記載・未確認・要確認の扱い

案件文、画像、ユーザー入力から確認できない内容は、以下のいずれかで扱う。

```text
未記載：
未確認：
要確認：
```

不明点があっても、ステップ3〜6では処理を止めない。

判断が必要な場合は、仮判断として以下を記録する。

```text
判断した内容：
判断根拠：
不確実な点：
なぜその判断を採用したか：
```

---

## 最終確認

常に次の問いに戻る。

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