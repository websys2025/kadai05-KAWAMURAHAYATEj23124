## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能
* エンドポイント：https://zipcloud.ibsnet.co.jp/api/search
機能：日本の郵便番号を入力すると、対応する住所を返す無料API。
* リクエストとレスポンスのフォーマット
https://zipcloud.ibsnet.co.jp/api/search?zipcode=1000001
{
  "message": null,
  "results": [
    {
      "zipcode": "1000001",
      "prefcode": "13",
      "address1": "東京都",
      "address2": "千代田区",
      "address3": "千代田",
      "kana1": "ﾄｳｷｮｳﾄ",
      "kana2": "ﾁﾖﾀﾞｸ",
      "kana3": "ﾁﾖﾀﾞ"
    }
  ],
  "status": 200
}
### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL
Agify API
参照URL： https://agify.io
* エンドポイントと機能
エンドポイント：https://api.agify.io/
機能：名前を指定すると、その名前を持つ人の平均年齢を推定して返すAPI。
* リクエストとレスポンスのフォーマット
https://api.agify.io/?name=Emily
{
  "name": "Emily",
  "age": 31,
  "count": 123456
}
### Q3-3. 感想
* 今回の課題で苦労したこと
非同期処理（async/await）の扱いや、JSONデータの解析方法に最初は戸惑いがあった。また、APIからのエラーレスポンス時の処理をどう書くかも悩みどころであった。
* 演習を通して理解できたこと
Web APIの使い方と、リクエスト〜レスポンスの一連の流れ。
fetchを使って非同期に外部リソースと通信する方法。
JSONの扱い方、エラー処理の基本。
* Web APIの利便性や課題など
APIを利用すれば、簡単に外部のデータを取得し、Webページを動的に変化させられるという強力な手段が得られる。しかし、APIの仕様変更や通信エラーなど、制御不能な問題もあるため、堅牢な実装と正確なドキュメントの読み込みが重要だと感じた。
