# WebChatUI-MarkedSample
このサンプルコードを用いることで、Web Chatにおいて file:// からはじまる文字列に対してハイパーリンクを設定することができます。

# 背景
Web ChatのUIを制御しているデフォルトのエンジンとして、markdown-itというものが使用されています。Web Chatでは、markdown-itの初期設定において file:// から始まる文字列を、セキュリティの問題から、単なる文字列として出力することになっています(QnA Makerで登録したマークダウンが file:// に対しては適応されません)。そのため、file:// に対してWeb Chat上でハイパーリンクを付ける場合には、レンダリングエンジンの設定を変える必要があります。

# 本サンプルについて
このサンプルではレンダリングエンジンとして、Markedを採用しています。また、サニタイジング処理も書かれています。ローカルファイルやファイルサーバ上のファイルリンクを特別な都合上ボットに載せたいという要求がある時のみ使用すべきサンプルと考えて頂き、セキュリティの管理に関しては、ご使用者様のご責任でお願いいたします。

# 動作環境
Google Chrome, Microsoft Edge, Internet Explorer 11 で動作を確認済みです。

# 使用方法
1. Azureポータルでボットのチャネル設定から、Direct Lineを選択し、発行されるキーをコピーしてください。

<a href="https://imgur.com/uRmoMkQ"><img src="https://i.imgur.com/uRmoMkQ.png" title="source: imgur.com" /></a>

2. index.htmlの28行目 YOUR_SECRET_KEY を消し、コピーしたキーを貼り付けてください。

<a href="https://imgur.com/EdEj6Fj"><img src="https://i.imgur.com/EdEj6Fj.png" title="source: imgur.com" /></a>

3. 動作をローカル環境でご確認後、Azure Web Appのwwwroot配下に作成したindex.htmlを配置してください。

<a href="https://imgur.com/D4PoTCY"><img src="https://i.imgur.com/D4PoTCY.png" title="source: imgur.com" /></a>

4. 動作確認をお願いします。

# 留意事項
本サンプルを用いることで file:// に対してもWeb Chatでハイパーリンク表示をさせることができますが、その後ユーザがファイルを直接ダウンロードできるかどうかの設定はブラウザ側の設定になります。Chromeではローカルファイルをダウンロードするための拡張機能が提供されておりますが、セキュリティの都合上採用できないという場合には、ボット側のUIで、ユーザにリンクをコピーすることを促すようなデザインを作る必要があるかと思います。

# Special Thanks
This sample code was created by William-san(https://github.com/compulim), a software engineer developing Web Chat. Corina-san(https://github.com/corinagum) also gave us some advice and it was really helpful. Thank you so much!
