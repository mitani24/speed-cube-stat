# speed-cube-stat

> Speed Cube のデータ分析環境です

## コンテナの起動・終了

```sh
# 起動
docker compose up --detach

# 終了
docker compose down
```

## Jupyter Notebook へのアクセス

ブラウザで http://localhost:8889/ へアクセスする。

## データの取得

### OLL

[OLL trainer](https://bestsiteever.ru/oll/) を使用する。  
少なくとも 500 以上ソルブしたい。 ソルブ数を確認するには開発者ツールのコンソールに以下の JavaScript を貼り付けて実行すると便利。

```js
const data = localStorage.getItem("olltimesarray");
JSON.parse(data).length;
```

サイトへアクセスし localStorage の `olltimesarray` のデータをコピーし `/workdir/data/oll/yyyy-MM-dd.json` として保存する。

### PLL

[PLL trainer](https://bestsiteever.ru/pll/) を使用する。  
少なくとも 300 以上ソルブしたい。 ソルブ数を確認するには開発者ツールのコンソールに以下の JavaScript を貼り付けて実行すると便利。

```js
const data = localStorage.getItem("plltimesarray");
JSON.parse(data).length;
```

サイトへアクセスし localStorage の `plltimesarray` のデータをコピーし `/workdir/data/pll/yyyy-MM-dd.json` として保存する。
