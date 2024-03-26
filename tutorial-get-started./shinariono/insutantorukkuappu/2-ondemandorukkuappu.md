# 2. オンデマンドルックアップ

## 新規オンデマンドルックアップの作り方

ブラウザの拡張機能が1つまたは複数の単語を使って検索を行います。作成の過程は簡単なコピーペースト操作を含む２つのステップからなります。

ステップ 1 - 既存サイト / ツール / ダッシュボードから任意のURLを用意します。

ステップ 2 - アドホック検索の仕組みを準備するためにURLを設定します。

ステップ 3 - 設定した内容をブラウザの拡張機能で確認します。

### ステップ 1 - 既存サイト / ツール / ダッシュボードから任意のURLを用意します。

ブラウザを開いたうえで、お使いの任意のツールのページを開きます。

例として、インターネット上の、ハッカーやスパムなどの迷惑行為を対処するために立ち上げられたプロジェクトである AbuseIPDB ([https://www.abuseipdb.com/](https://www.abuseipdb.com/))を使います。 このサイトで IPレピュテーションやマルウエアを拡散するようなサイトかどうかなどを調べることができます。

ウエブサイトを開いて、ウエブサイトのURLをコピーする前に、必ず下記の通りに<mark style="color:blue;">**検索を実施してください**</mark>。

`https://www.abuseipdb.com/check/61.177.173.41`

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption><p>AbuseIPDB</p></figcaption></figure>

### ステップ 2 - アドホックルックアップの仕組みを準備するためにURLを設定します。

URLをパラメータ化するには、コピーしたURLを参照先URLボックスに張り付けて、「**URLをカスタマイズする**」をクリックします。

今回の例では、IPアドレス部分（61.177.173.41）をパラメータ化します。

元のURL -&#x20;

* `https://www.abuseipdb.com/check/61.177.173.41`

パラメータ化後のURL

* `https://www.abuseipdb.com/check/{$key}`

{% embed url="https://drive.google.com/file/d/1QZK9-UXLLiwMOD_CPuJ4X_6-TQ_7G3Dc/view?usp=sharing" %}

{% hint style="info" %}
studioが対象サイトを自動的に検知しなかった場合でも、機能的な影響はありません。\
しかし拡張機能を追加することでstudioを視覚的に拡充させます。

やり方は2つあります。

1. メインメニューへ移動し、「[拡張機能](../../pitwall-kuo-zhang-ji-neng.md#2.-adding-time-format-s-to-detect-timestamps-from-the-url-you-would-like-to-parameterize-in-the-stud-1)」でアイコンのイメージをアップロードすることで拡張機能を追加できます。また、拡張機能をPITWALLコミュニティに追加すると誰でも使えるようになります。
2. チャットにて連絡していただければ、拡張機能を有効にします。
{% endhint %}

### ステップ 3 - 設定した内容をブラウザの拡張機能で確認します。

ブラウザの拡張機能を開いて自身のアカウントでサインインします。

1. シナリオへ移動し、検索する任意のサイトを選択します。
2. 文字列（値）を選択し、**検索**をクリックします。
3. 報告などのために**スナップ**ボタンで画面キャプチャ（ダウンロード可能なPNG）を取ることもできます。

{% hint style="info" %}
プライベートアルファでは、スナップショット機能は備わっていませんが、ベータ向けにロードマップに含まれています。
{% endhint %}

{% embed url="https://drive.google.com/file/d/1Ig1Ci1rdBp79tPUWT5jyKBcSVFT_Z281/view?usp=sharing" %}

\
