# FXmonitor

使わなくなったiPhoneへUSD/JPYを大きく常時表示するためのGitHub Pagesです。

## 仕様

- データ: Coinbase Exchange Rates API
- 更新間隔: 60秒
- APIキー、口座登録、サーバー: 不要
- 表示: USD/JPYの数値のみ
- 通信失敗時: 最後に取得できた値をオレンジ色で表示

CoinbaseのAPIが返す現在のUSD基準レートからJPYを表示します。これは参考レートであり、
特定のFX会社で実際に約定できるBid/Ask価格ではありません。

## 公開

```powershell
git add index.html README.md
git commit -m "Use current Coinbase exchange rates"
git push origin main
```

GitHub Pagesのデプロイ完了後、次を開きます。

```text
https://kaico-hub.github.io/FXmonitor/
```

## iPhoneへ設置

1. SafariでGitHub Pagesを開きます。
2. Safariの共有ボタンを押します。
3. `ホーム画面に追加`を選択します。
4. 追加されたFXmonitorを起動します。
5. 画面を一度タップし、Screen Wake Lockを有効にします。
6. iPhoneを充電器へ接続し、画面輝度を低めにします。

端末やiOSの設定によって画面が消える場合は、`設定` → `画面表示と明るさ` →
`自動ロック`を`なし`にします。低電力モード中は`なし`を選択できない場合があります。

## 表示の意味

- 白い数値: 正常に更新中
- オレンジの数値: 更新に失敗し、最後に取得できた値を表示中
- `ERROR`: 最初の価格を取得できなかった

週末など市場が閉じている時間は、最後の参考レートが表示される場合があります。
