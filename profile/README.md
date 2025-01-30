# Boring-Biz 開発マニュアル
開発時の共有事項をこちらにまとめていきます。

## Gitについて
文字数カウンターをGithub上に上げる手順については、`character-counter`のディレクトリにて以下のコマンドを実行してください。
```bash
echo "# character-counter" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:boring-biz/character-counter.git
git push -u origin main
```

## 簡単な流れ
リモートにある最新のソースコードをローカルに同期させます。
```bash
git pull origin main
```

ブランチを切ります。
```bash
git checkout -b feature/add-test-function
```

変更をコミットします。(動く状態のものをチェックポイントとしてgit上に記録します)
""で囲まれたメッセージ部分は適切なものに置き換えてください。
```bash
git add .
git commit -m "ダークモードの切り替え機能の追加"
```

ローカルの変更をリモートへ反映させます
```bash
git push origin feature/add-test-function
```

Pull Requestsタブを押下します。
<img width="1498" alt="image" src="https://github.com/user-attachments/assets/7c8c1802-09dc-4af6-8092-b945e3ca0941" />

右にある緑色のNew Pull Requestボタンを押下します。
<img width="1504" alt="image" src="https://github.com/user-attachments/assets/3e4aea53-f223-4ca9-a36f-cb4557369caa" />

左側(向き先)をmainに、右側(反映元)を先ほどPUSHした`feature/add-test-function`に切り替え、Create Pull Requestボタンを押下します。
<img width="1293" alt="image" src="https://github.com/user-attachments/assets/cb53404d-2c5c-4f30-8da0-d4d6b718dcf2" />

タイトル/やったことなどを記載して`Create Pull Request`ボタンを押下します。
<img width="946" alt="image" src="https://github.com/user-attachments/assets/405f10e4-b2ff-415f-a25b-8b8826cf603f" />

必要であれば、Reviewersの設定アイコンを押下し、レビュアーを設定しましょう。
<img width="1307" alt="image" src="https://github.com/user-attachments/assets/b09cf2fa-b89f-4700-921a-55c1f6383f4f" />

