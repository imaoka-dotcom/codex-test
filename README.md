diff --git a/README.md b/README.md
index 5d329221f03bc325fdc202d7fd5522e82bb50ddd..ef2b2cc09d7e5c00ef4bfc14ffba568533658a4c 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,31 @@
-# codex-test
\ No newline at end of file
+# codex-test
+
+## 在庫確認デモ（ローカル検証用）
+
+このページは「自分だけで動作確認する」ための在庫検索デモです。`index.html` 単体で動きます。
+
+### 仕様
+- ダミー在庫データ 100 件を JavaScript 内で自動生成
+- データ項目: `jan`, `name`, `stock`, `price`, `updated_at`
+- JAN は 13 桁の連番（重複なし）
+- JAN 入力で部分一致検索、13 桁の完全一致なら詳細カード表示
+- 在庫 0 は警告表示
+- 最終更新日を表示
+- 登録/編集/削除・localStorage 保存は本デモでは未使用
+
+## ローカルでの確認手順
+### 1) もっとも簡単な方法（ダブルクリック）
+1. `index.html` をダウンロード（またはローカルに保存）します。
+2. `index.html` をダブルクリックしてブラウザで開きます。
+3. JAN 入力欄に数字を入れて、検索結果が絞り込まれることを確認します。
+4. 「リセット」ボタンで入力がクリアされることを確認します。
+
+### 2) うまく動かない場合（簡易ローカルサーバ）
+1. ターミナルで `index.html` があるフォルダへ移動します。
+2. 次のコマンドを実行します。
+   ```bash
+   python3 -m http.server 8000
+   ```
+3. ブラウザで `http://localhost:8000/index.html` を開きます。
+
+> 参考: Python が `python3` ではなく `python` の環境では `python -m http.server 8000` を利用してください。

