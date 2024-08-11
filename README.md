# fieldwork-app

## Branch, PR のルール

- Notion の課題の単位でブランチを切る。
- develop から branch を切る。
- 開発を行うときの branch 名は必ず `feature-` から始まるケバブケース (`feature-user-photos` のような形式) にする。
- develop に merge するときには必ず PR を作成する。
- PR では必ず 1 人以上のレビューをもらい、最後に commit した人が merge する。
- merge した branch は delete branch して、再利用しない。

## Commit のルール

- エラーが出ず動作する単位で commit する。
- commit の prefix は以下の通り。
  | Prefix | Description |
  | ---- | ---- |
  | `add:` | 機能の追加 |
  | `fix:` | 機能の変更または修正 |
  | `init:` | ライブラリなど開発環境の導入やバージョンアップ（この commit を cherrypick すれば 1 つのライブラリの導入が完了するようにする） |
  | `clean:` | 現在は使われていないファイルの削除など、動作に影響しない変更 |
  | `docs:` | README.md ファイルの変更のような、動作確認の必要のない変更 |
  | `remove:` | 機能の削除 |
- 1 行目に prefix つきのタイトル、3 行目に変更の内容を具体的に記載する。
  ```
  add: APIからの写真の取得

  ARビューのフォトフレームに、APIから取得した写真が表示されるようにする。
  ```