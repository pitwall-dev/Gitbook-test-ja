---
description: インシデントが発生し、アラートがトリガーとなって、自動的に検索をします。
---

# 📪 アラート

## Overview

各シナリオでは、自動検索とスクリーンショットの取得が提供されます。これは、チームが調査をする又は様々なツールで調べる必要のあるアラートや状況毎に定義します。検索するツールが同じであれば、複数のアラートがある場合でも、異なるアラート間で同じシナリオを利用することができます。

<figure><img src="../../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

シナリオは3つの手順を踏むことで作成できます。

{% content-ref url="1-torig/" %}
[1-torig](1-torig/)
{% endcontent-ref %}

{% content-ref url="2-rukkuappu.md" %}
[2-rukkuappu.md](2-rukkuappu.md)
{% endcontent-ref %}

{% content-ref url="3.-tong-zhi-xian.md" %}
[3.-tong-zhi-xian.md](3.-tong-zhi-xian.md)
{% endcontent-ref %}

以下のチュートリアルでは、こちらの例を使用してシナリオを有効化します。\
監視ツール（Coralogix）によってアラートがトリガーされ、PITWALLによって作成されたシナリオに基づいて、ルックアップがつなぎ合わされ、Slack、MS Teams、Eメール等のツールでそれが受領されます。\
&#x20;

<figure><img src="../../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

それでは、ステップ毎に見ていきましょう。
