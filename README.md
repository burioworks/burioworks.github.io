# Burioworks developer site

このリポジトリは、BurioworksのGitHub Pagesサイトです。

- 公開URL: <https://burioworks.github.io/>
- Banso法務ページ: <https://burioworks.github.io/banso-legal/>
- app-ads.txt: <https://burioworks.github.io/app-ads.txt>

## ディレクトリ構成

```text
.
├─ index.html
├─ styles.css
├─ favicon.ico
├─ favicon.png
├─ app-ads.txt
├─ README.md
├─ assets/
│  └─ brand/
│     └─ burioworks/
│        ├─ docs/
│        ├─ icons/
│        ├─ logo/
│        ├─ reference/
│        ├─ web/
│        └─ README.md
└─ banso-legal/
   ├─ index.html
   ├─ privacy-policy.html
   ├─ terms-of-service.html
   ├─ data-storage-and-deletion.html
   └─ assets/
      └─ css/
         └─ style.css
```

## ブランドアセット

Burioworksの承認済みブランドキットは`assets/brand/burioworks/`で管理します。Webページから使用する場合は、`/assets/brand/burioworks/`から始まるルート相対URLで参照します。ブランドの使用規則と原本ファイルは、同ディレクトリ内の`README.md`を参照してください。

`app-ads.txt`は、AdMobがBurioworksのアプリ広告販売者情報を確認するためのファイルです。更新時はAdMob管理画面に表示される正式な1行だけを使用し、ダミー値、説明、コメントは追加しません。

## GitHub Pages

公開元は`main`ブランチの`/ (root)`です。

```text
Settings
→ Pages
→ Source: Deploy from a branch
→ Branch: main
→ Folder: / (root)
```

## 旧Banso法務Pagesからの移行

1. このリポジトリの変更を`main`へマージし、上記設定で新サイトを公開します。
2. <https://burioworks.github.io/>と<https://burioworks.github.io/app-ads.txt>を確認します。
3. 旧`burioworks/banso-legal`のPagesは稼働させたまま、<https://burioworks.github.io/banso-legal/>が引き続き表示できることを確認します。
4. 新リポジトリに法務ページ一式が含まれ、ローカル検証が完了していることを確認してから、旧`burioworks/banso-legal`の`Settings → Pages → Unpublish site`を手動で実行します。
5. 旧Pages停止後、同じ法務URLがHTTP 200で表示され、プライバシーポリシー、利用規約、CSS、リンクに問題がないことを再確認します。

旧リポジトリ自体は削除・アーカイブしません。Pagesの反映待ちやキャッシュの影響がある場合も、公開元の切り替えを確認するまで旧リポジトリを維持します。

## 公開後の手動作業

- Play Consoleのデベロッパーウェブサイトを<https://burioworks.github.io/>に設定します。
- Play ConsoleのプライバシーポリシーURLは<https://burioworks.github.io/banso-legal/>のまま変更しません。
- <https://burioworks.github.io/app-ads.txt>へ直接アクセスできることを確認し、AdMobでapp-ads.txtの更新確認を実行します。
