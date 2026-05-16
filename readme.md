# 作成方法メモ

Github+Cloudflareを使用する方法メモ

1. Githubにファイルアップロード
    * Githubでプロジェクト作成
    * Githubにファイルアップロード
1. Cloudflareでアプリケーション作成
    * CloudflareでWorkers&Pages > アプリケーションを作成 > 下のPagesを導入しようとお考えですか？始める　をクリック
    * 既存のGitリポジトリをインポートする
1. データベース作成
    * クイック検索で「D1」と検索、データベースを作成
    * テスト用のデータを追加してみる
        * コンソールに以下を1行ずつ実行
            ```
            CREATE TABLE test_table(id INT, title VARCHAR(100))
            INSERT INTO test_table(id, title) VALUES (0, "テスト1")
            INSERT INTO test_table(id, title) VALUES (1, "テスト2")
            INSERT INTO test_table(id, title) VALUES (2, "テスト3")
            SELECT * FROM test_table
            ```
1. PagesとD1を連携させる
    * Workers&Pages > 概要 > バインディングを追加 > D1データベース　を選択し、バインディングを追加
