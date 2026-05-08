# 工作流程

- 完成程式或內容修改後，主動執行 `git add` → `git commit` → `git push`，不需再詢問。
- 在同一個任務中若有多次修改，等任務完成再一起 commit，不要每次小編輯都 commit。
- commit message 沿用本 repo 既有風格：`feat:` / `fix:` / `chore:` 等前綴 + 中文簡述。
- 若遇到衝突、pre-commit hook 失敗、或變更包含可疑檔案（`.env`、密鑰等），停下來回報，不要強推。
