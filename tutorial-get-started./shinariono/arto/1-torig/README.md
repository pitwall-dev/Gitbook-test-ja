# 1. トリガー

## トリガーを設定する

本チュートリアルでは例を用いてシナリオを有効にするための手順を説明します。 監視ツール（Coralogix）からアラートがトリガーされ、PITWALLで作られたシナリオに基づき、ルックアップがつなぎ合わせられ、Slackに送信されます。\
&#x20;

<figure><img src="../../../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

シナリオに名前を付けた後、ソースを定義します。シナリオの種類はいくつかあります。アラートをきっかけとした動的シナリオを作るにはシナリオタイプから「**受信アラート**」を選択します。どの監視ツールからアラートが送信されるかを定義します。

{% tabs %}
{% tab title="アラート" %}
アラートシナリオはアラートをきっかけにトラブルシューティングと解析プロセスを開始します。複数のツールから必要な情報やデータを関連付けることができます。
{% endtab %}

{% tab title="インスタントルックアップ" %}
本機能は簡単かつ豊富な検索機能を提供しています。特殊なユースケースは[sekyuritike.md](../../../../use-cases/sekyuritike.md "mention")または[ke.md](../../../../use-cases/ke.md "mention")をご参照ください。また、これらのユースケースに加え、「Text in browser」シナリオの設定方法についてここをご参照ください。
{% endtab %}

{% tab title="スケジュール" %}
スケジュール監視により、定期的なリンク生成とスクリーンショットを撮ることができます
{% endtab %}
{% endtabs %}

<figure><img src="../../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
PITWALLでさまざまなツールに対応できるようにするために[ロードマップ](../../../../overview/rdomappu.md)の一部として「Alert Parser」をオープンソースにすることになっています。
{% endhint %}
