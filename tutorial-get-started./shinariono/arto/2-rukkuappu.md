# 2. ルックアップ

## 新規ルックアップ（送信先）を作成します。

本手順ではインシデントとイベント発生時・解析時に、確認および解析の対象情報を設定する、シナリオの主要な部分を説明します。

3つのステップで設定します。簡単なコピーペースト操作で行います。

ステップ 1 - 既存サイト / ツール / ダッシュボードから任意のURLを用意します。

ステップ 2 - 動的ルックアップメカニズムを準備するためにURLを設定します。

ステップ 3 - 事前、定期的、またはその両方でサイト / ツール / ダッシュボードのスクリーンショットを取りたい場合、スナップショット機能を有効にします。



### ステップ 1 - 既存サイト / ツール / ダッシュボードから任意のURLを用意します。

ブラウザを開き、トラブルシューティングやインシデント分析のためにお使いのツールへ移動します。

例として、Coralogixが提供している（可視化のためによく使われているオープンソースの）Kibanaのダッシュボードを使います。

ダッシュボードを開いた後、URLをコピーする前にまず<mark style="color:blue;">**手動で時間範囲を設定する必要があります**</mark>。\
お使いのツールでは、"直近の15分間"のような相対的な時間範囲の指定になる場合、必ず具体的な**いつから (from:)** と**いつまで (to:)** を次のように絶対的な形で指定してください。Sep 23, 2022 @ 00:03:06 -> Sep 23, 2022 @ 01:03:06。このように設定することでPITWALLが動的にダッシュボードの時刻とインシデントの発生時刻と合わせられるようになります。

<figure><img src="../../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

コピーしたURLは以下のような形になります。\
\
`https://`_`yourtenant`_`.coralogix.com/#/app/kibana#/dashboard/d1afbef0-4906-11ec-8b23-b372b1e7ae1d?_g=(refreshInterval:(pause:!t,value:0),time:`**`(from:'2022-09-23T07:03:06.000Z',to:'2022-09-23T08:03:06.000Z')`**`)&_a=(description:'',filters:!(),fullScreenMode:!f,options:(hidePanelTitles:!f,useMargins:!t),panels:!((embeddableConfig:(),gridData:(h:27,i:'188b3cb8-1f32-488c-b44c-99c46ecaa2d1',w:48,x:0,y:0),id:'5ffed850-50c1-11ec-a30d-7fdab983d73c',panelIndex:'188b3cb8-1f32-488c-b44c-99c46ecaa2d1',type:visualization,version:'7.4.2')),query:(language:kuery,query:''),timeRestore:!f,title:'Unique%20User%20Count',viewMode:view)`



### ステップ 2 - 動的ルックアップメカニズムを準備するためにURLを設定します。

送信先のURLボックスに、コピーしたURLを貼り付け、"**URLをカスタマイズする"**をクリックします。自動的にURLからタイムスタンプを検知し、どの値を動的にするかを指定することもできます。例えば、アラートのホスト名（$hostname）をクエリURLの一部として適用することが可能です。

<figure><img src="../../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (24).png" alt=""><figcaption><p>URL customization</p></figcaption></figure>

タイムスタンプがエンコードされたり、プレフィックスや形式（ISO,、epoch等）が異なったりすると、タイムスタンプが自動的に検知されない場合があります。その場合の解決策として以下の2つの方法があります。

1. メインメニューにある[pitwall-kuo-zhang-ji-neng.md](../../pitwall-kuo-zhang-ji-neng.md "mention")へ移動し自身の拡張機能を追加し正規表現を用いてタイムスタンプを定義します。\
   また、拡張機能をPITWALLコミュニティに追加すると、誰でも使えるようになります。
2. チャットにて連絡していただければ、拡張機能を有効にします。

### ステップ 3 - 事前、定期的、またはその両方でサイト / ツール / ダッシュボードのスクリーンショットを取りたい場合、スナップショット機能を有効にします。

アラートを受信する際に、事前に取ったスクリーンショットを添付したい場合、スナップショットを有効にしてください。

&#x20;

<figure><img src="../../../.gitbook/assets/image (61).png" alt=""><figcaption><p>Snapshot enabled alert in Slack.</p></figcaption></figure>

