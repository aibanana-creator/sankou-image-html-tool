# CSS Image Motion Lab — Vercel Static Site

HTML/CSSのみで作られた、画像モーション・エフェクト・画像間トランジション・画像境界・レイヤーモーションのサンプルサイトです。**ビルド不要・JavaScript不要・環境変数不要**で、そのままVercelへデプロイできます。

## 構成

| ファイル／フォルダ | 用途 |
| --- | --- |
| `index.html` | 全サンプルを集約したメインページ |
| `transitions.html` | トランジション／レイヤーモーションに絞ったページ |
| `assets/` | デモ用画像8点 |
| `favicon.svg` / `logo.svg` | サイトアイコンとロゴ |
| `vercel.json` | 静的ホスティング用ヘッダー設定 |

## Vercel Dashboardからデプロイする方法

1. このフォルダをGitHub・GitLab・Bitbucketの新規リポジトリにプッシュします。
2. Vercelで **Add New → Project** を選び、該当リポジトリをImportします。
3. **Framework Preset** は `Other` を選択します。
4. **Build Command** と **Output Directory** は空欄のままにします。ルート直下の `index.html` がそのまま配信されます。
5. **Deploy** を実行します。

デプロイ後の主なページは以下です。

- `/` — 統合ギャラリー
- `/transitions.html` — トランジション／レイヤーモーションページ

## Vercel CLIからデプロイする方法

Node.jsが使える環境で、展開したフォルダ内から実行します。

```bash
npx vercel
```

本番へ直接出す場合は、次を使います。

```bash
npx vercel --prod
```

## ローカル確認

Node.js不要で確認する場合は、Pythonの簡易サーバーを使えます。

```bash
python3 -m http.server 3000
```

`http://localhost:3000/` を開いてください。

## 注意事項

- デモ画像はサンプル用途です。商用公開・本番利用時は、利用条件を確認したうえで自社の画像へ差し替えてください。
- `AUTO PLAY` はCSSのチェックボックス制御で、JavaScriptは使用していません。
- `prefers-reduced-motion: reduce` に対応しており、OS側で動きを減らす設定の場合はアニメーションが抑制されます。
