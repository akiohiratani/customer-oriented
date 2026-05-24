# セッション開始・フォルダ作成

## 起動キーワード

ユーザーが次のいずれかを入力したら、セッション開始処理を行う。

```text
顧客志向学習開始
```

---

## 目的

新しい案件、または新しい学習チャットごとに専用の作業フォルダを作成する。

この段階では、まだ案件分析は開始しない。

目的は、以後の出力先を明確にし、別案件のファイルを上書きしない状態を作ることである。

---

## 実行内容

ユーザーが「顧客志向学習開始」と入力したら、以下を実行する。

1. 新規 `SESSION_DIR` を作成する
2. `SESSION_DIR/assets/` を作成する
3. `SESSION_DIR/outputs/` を作成する
4. `SESSION_DIR/README.md` を作成する
5. 作業フォルダをチャットに表示する
6. 案件情報入力テンプレートを表示する
7. 分析はまだ開始しない
8. ユーザーの案件情報入力を待つ

---

## SESSION_DIR の命名規則

新しい案件、または新しい学習チャットを開始するたびに、必ず専用フォルダを作成する。

作業フォルダは、次の形式にする。

```text
sessions/YYYYMMDD_HHMM_案件名/
```

案件名がまだ分からない場合は、仮フォルダ名を使う。

```text
sessions/YYYYMMDD_HHMM_new_case/
```

案件名が長い場合は、短く分かりやすい名前にする。

例：

```text
sessions/20260520_2130_rollite_bag/
sessions/20260521_0900_meta_banner/
sessions/20260521_1430_thumbnail_competition/
```

以後、この作業フォルダを `SESSION_DIR` と呼ぶ。

---

## 作業フォルダ内の構成

新規案件開始時に、必ず以下の構成を作成する。

```text
SESSION_DIR/
  README.md
  assets/
  outputs/
```

完成後の構成は以下を想定する。

```text
SESSION_DIR/
  README.md
  assets/
    product_01.jpg
    product_02.jpg
    scene_01.jpg
    scene_02.jpg
    reference_01.png
    preference_01.png
  outputs/
    01_input_summary.md
    02_step1_facts.md
    03_step2_customer_goal.md
    04_step3_target_psychology.md
    05_step3_5_persona_dialogue_draft_selection.md
    06_step4_appeal_axis.md
    07_step5_design_translation.md
    08_canva_design_spec.md
    09_gpt_canva_prompt.md
    10_design_review.md
    11_submission_message.md
    12_learning_log.md
```

---

## フォルダ作成コマンド

可能であれば、CodexはOSに応じて以下を実行する。

### macOS / Linux の場合

```bash
mkdir -p sessions/YYYYMMDD_HHMM_new_case/assets
mkdir -p sessions/YYYYMMDD_HHMM_new_case/outputs
touch sessions/YYYYMMDD_HHMM_new_case/README.md
```

### Windows PowerShell の場合

```powershell
New-Item -ItemType Directory -Force -Path sessions\YYYYMMDD_HHMM_new_case\assets
New-Item -ItemType Directory -Force -Path sessions\YYYYMMDD_HHMM_new_case\outputs
New-Item -ItemType File -Force -Path sessions\YYYYMMDD_HHMM_new_case\README.md
```

OSに応じて適切なコマンドを選ぶ。

実行できない場合は、チャットでその旨を伝え、ユーザーに手動作成を案内する。

---

## README.md の作成

`templates/readme_template.md` をもとに、`SESSION_DIR/README.md` を作成する。

READMEには、以下を記録する。

1. 案件名
2. 作成日
3. 作業フォルダ
4. 学習目的
5. 進行状況チェックリスト

各ステップが完了したら、README.md のチェックボックスを更新する。

---

## セッション開始時のチャット出力

セッション開始後、チャットには以下を表示する。

```text
今回の作業フォルダ：
SESSION_DIR/

以後、この案件の出力は以下に保存します。
SESSION_DIR/outputs/

画像は以下に保存してください。
SESSION_DIR/assets/

以下のテンプレートに、クラウドワークスの「仕事の詳細」と、添付画像の情報を貼ってください。
分からない項目は「未記載」で大丈夫です。
```

その後、`templates/input_template.md` の内容を表示する。

---

## セッション開始時にやってはいけないこと

この段階では、以下を行ってはいけない。

1. 案件分析を始める
2. 顧客目的を推測する
3. ターゲット心理を推測する
4. Canva指示書を作る
5. ステップ1以降に進む
6. ユーザーがまだ入力していない案件情報を補完する

---

## 次にユーザーへ促すこと

セッション開始後は、ユーザーに案件情報入力を促す。

案内文は以下とする。

```text
案件情報を貼り付けてください。
貼り付け後、内容を整理して `SESSION_DIR/outputs/01_input_summary.md` を作成します。
```