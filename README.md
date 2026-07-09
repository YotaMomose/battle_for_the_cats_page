# にゃんこホイホイ! 公式Webページ（GitHub Pages用）

App Store申請に必要な「プライバシーポリシー」「利用規約」「お問い合わせ」ページ一式です。

## 構成
```
index.html            ← トップ / お問い合わせ
privacy-policy.html   ← プライバシーポリシー
terms.html             ← 利用規約
style.css             ← 共通スタイル
assets/                ← ロゴ・猫画像
```

## 公開前にやること（必須）
1. **メールアドレスの差し替え**
   `your-email@example.com` を実際の問い合わせ先メールアドレスに変更してください。
   （`index.html` / `privacy-policy.html` / `terms.html` の3箇所）
2. **開発者名の確認**
   現在「Yota」を開発者名として記載しています。個人名を出したくない場合は、
   屋号やペンネームに差し替えてください。
3. 内容は一般的なひな形です。実際の実装（データの取り扱い等）と齟齬がないか、
   可能であれば一度目を通してください。特にアプリ内課金を実際に導入したタイミングで、
   プライバシーポリシー・利用規約の該当箇所（「予定」という表現）を更新してください。

## GitHub Pagesでの公開手順
1. GitHubに新しいリポジトリを作成（例: `nekosodatsusen-legal`）
2. このフォルダの中身（index.html, style.css, assets/ など）をリポジトリ直下にpush
   ```bash
   git init
   git add .
   git commit -m "Add legal pages"
   git branch -M main
   git remote add origin https://github.com/ユーザー名/リポジトリ名.git
   git push -u origin main
   ```
3. GitHubのリポジトリページ → **Settings** → **Pages**
4. 「Build and deployment」の **Source** を `Deploy from a branch` に設定
5. **Branch** を `main` / `/(root)` に設定して **Save**
6. 数分後、`https://ユーザー名.github.io/リポジトリ名/` で公開されます
   - プライバシーポリシー: `https://ユーザー名.github.io/リポジトリ名/privacy-policy.html`
   - 利用規約: `https://ユーザー名.github.io/リポジトリ名/terms.html`
   - お問い合わせ: `https://ユーザー名.github.io/リポジトリ名/index.html`

## App Store Connect / Google Play Console への登録
- **App Store Connect**：「プライバシーポリシーURL」欄に `privacy-policy.html` のURLを入力
- 審査中もURLが生きている必要があるため、**申請前に必ず公開状態を確認**してください（審査に最大1週間ほどかかる点にご注意）
- サポートURL（お問い合わせ）には `index.html` のURLを入力
