# 報告用リポジトリのテンプレート

`AtelierZeek/Nocvelle-feedback`（公開・Issue専用）へ置く、Issueフォームの下書き。アプリの「不具合を報告」（`BugReport`）が開く `bug_report.yml` と、空のIssueを止める `config.yml`。

- `feature_request.yml` は、アプリの「要望を送る」が開く要望フォーム（バージョンだけを事前入力）。
- フォームの項目 `version`・`build`・`environment` の `id` が、アプリが事前入力するURLのクエリ名と対応している。名前を変えるときは、`BugReport.issueUri` も合わせる。
- Issueフォームの入力欄には、読み取り専用の指定がない。事前入力した項目（`version`・`build`・`environment`）は、書き換えられるため、欄の説明に「そのまま変更しないでください」と書いている（Issue #80）。
- 開発リポジトリのPRに `Fixes AtelierZeek/Nocvelle-feedback#N` と書くと、既定ブランチへのマージ時に、公開Issueがクローズされる。
