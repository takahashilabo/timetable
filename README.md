# timetable
大学等で時間割を検討するときに役立つかもしれないツールです。教務委員の１つの仕事として時間割作成がありまして、その個人的な仕事を効率化したくて自分のために作成しました。マウスで移動もできませんし重複チェックなどもできませんが、とりあえず目視で配置や干渉をチェックすることはできます。公開するつもりは毛頭ありませんでしたが、最近、使わせてくれ、という問合せが学内でありまして、意外とこんなツールでも役に立つのかもなぁ。。。と思って晒すことにしました。お役に立てれば幸いです。プルリクは受け付けません。もし必要であれば、各自で勝手にフォークして差分開発してください☺️

## 準備
- GoogleアカウントでGoogleドライブにログインして、Googleスプレッドシートを作成してください。
- A1セルからI1セルまで「NO&#009;科目名&#009;開講学年&#009;開講時期&#009;曜日&#009;時限&#009;担当者&#009;教室&#009;必修」を貼り付けてください。[こちら](https://docs.google.com/spreadsheets/d/1KM2iRnmxFxJgd-yuOjVpIFYick4ME_hR6781UZDTVrA/edit?usp=sharing)にテンプレートファイルを用意しました。コピーして使用していただければと思います。　
- [ツール] - [スクリプトエディタ] を選択します。
- このリポジトリ内のコード.gsの内容を、コード.gsに全て貼り付けてください。
- スクリプトエディタ上で、[ファイル] - [New] - [HTMLファイル] を選択して、「index.html」 という名前でファイルを作成します。
- このリポジトリ内のindex.htmlの内容を、index.htmlに全て貼り付けてください。
- 最後に、スクリプトエディタ上で [公開] - [ウェブアプリケーションとして導入] を選択し、表示されたダイアログの一番したの 「Who has access to the app」 を各自の要件に合わせて選択してください。例えば、Googleにログインさせずに誰でも閲覧させたいなら 「Anyone, even anonymous」 を選択して 「Deploy」 ボタンを押します。許可を確認するように指示されますので許可します。最後に表示された URL をメモっておきます。このアドレスにアクセスすると時間割がみれます。ちなみにChrome推奨です。

## 使い方
Googleスプレッドシートにデータを入力して、上記でDeployしたときに表示されたURLにアクセスします。その操作をひたすら繰り返します。各項目の内容を以下に書きます。

### NO
スクリプトでは使用しません。単にスプレッドシート内でデータをソートするときに使います。例えば、学則などで科目の並び順が決まっていると思います。その番号を入れておくと、あれこれいじっても戻すことができます。そんな感じで私は使っています。

### 科目名
科目名です。

### 開講学年（入力必須）
1〜4です。当然ですが。。。半角数字で入力してください。

### 開講時期（入力必須）
「前」か「後」です。セメスター制の場合はコードを書き換えてください。。。あくまで個人ツールなので。

### 曜日（入力必須）
月〜金です。

### 時限（入力必須）
1〜5です。当然ですが。。。半角数字で入力してください。

### 担当者
入力された文字列をそのまま表示しますので、複数人での担当の場合は、「A,B,C」などと書いていただければそのまま表示されます。

### 教室
上記の担当者と同じ感じになります。

### 必修
同時間帯での必修科目の干渉チェックは重要ですよね？ということで、私はここに★を記入して、横並びで見たときにぶつかっていないか確認します。不要であれば入力しなくても構いません。

以上でーす。


