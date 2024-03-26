# 3. ルックアップ

## 新規ルックアップを作成します。

1. 既存サイト / ツール / ダッシュボードから任意のURLを用意します。
2. 動的ルックアップメカニズムを準備するためにURLを設定します。
3. 画面キャプチャを取りたい場合はスクリーンショット機能を有効にします。

### サンプルURLを用意します。

ブラウザを開いて、トラブルシューティングやインシデント分析のためにお使いのツールへ移動します。

これはKibana/Opensearchダッシュボードを用いる例です。

まず、<mark style="color:blue;">**絶対的な形で時間範囲**</mark>を指定し、対象URLをコピーします。必ず次のように**いつから (From:)** と**いつまで (To:)** で絶対的な時間範囲をURLに指定してください。 例：Sep 23, 2023 @ 00:03:06 -> Sep 23, 2023 @ 01:03:06。

<figure><img src="../../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

コピーしたURLは以下のような形になります。\
\
`https://`_`yourtenant`_`.coralogix.com/#/app/kibana#/dashboard/d1afbef0-4906-11ec-8b23-b372b1e7ae1d?_g=(refreshInterval:(pause:!t,value:0),time:`**`(from:'2023-09-23T07:03:06.000Z',to:'2023-09-23T08:03:06.000Z')`**`)&_a=(description:'',filters:!(),fullScreenMode:!f,options:(hidePanelTitles:!f,useMargins:!t),panels:!((embeddableConfig:(),gridData:(h:27,i:'188b3cb8-1f32-488c-b44c-99c46ecaa2d1',w:48,x:0,y:0),id:'5ffed850-50c1-11ec-a30d-7fdab983d73c',panelIndex:'188b3cb8-1f32-488c-b44c-99c46ecaa2d1',type:visualization,version:'7.4.2')),query:(language:kuery,query:''),timeRestore:!f,title:'Unique%20User%20Count',viewMode:view)`



### 動的ルックアップメカニズムを準備するためにURLを設定します。

参照先URLボックスに、コピーしたURLを貼り付け、「**URLをカスタマイズする**」をクリックします。

URLから自動的にタイムスタンプを検出します。

{% hint style="info" %}
オプションで、どの値を動的にするかを指定することもできます。例えば、アラートのホスト名（$hostname）をクエリURLの一部として適用することが可能です。
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>



タイムスタンプがエンコードされたり、プレフィックスや形式（ISO,、epoch等）が異なったりすると、タイムスタンプが自動的に検知されない場合があります。その場合の解決策として以下の2つの方法があります。

1. メインメニューにある[pitwall-kuo-zhang-ji-neng.md](../../pitwall-kuo-zhang-ji-neng.md "mention")へ移動し自身の拡張機能を追加し正規表現を用いてタイムスタンプを定義します。また、拡張機能をPITWALLコミュニティに追加すると、誰でも使えるようになります。\

2. チャットにて連絡していただければ、拡張機能を有効にします。

### 3. スクリーンショットを有効にします。

スクリーンショットのキャプチャを取りたい場合、スクリーンショット機能を有効にします。

<figure><img src="../../../.gitbook/assets/image (61).png" alt=""><figcaption><p>Snapshot enabled alert in Slack.</p></figcaption></figure>

