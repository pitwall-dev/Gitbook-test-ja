---
description: 基本的な比較
---

# SnapView

## Overview

SnapViewは参照先ツールごとに3つの角度を提供することで、下記とインシデントを比較と分析するのに役立ちます。

下記と比較します。

1. ルックバック（過去の時点）
2. 過去のイベント
3. ベースライン機能

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

### ルックバック機能 <a href="#other-times" id="other-times"></a>

この機能では、対象データを、任意の時間帯で見ることができます。たとえば、あるダッシュボードをある時点で使用し、また、過去のある時点でも使用していた場合、 事前設定したルックバックオプションや特定時間の比較が可能です。

### 過去のイベント <a href="#past-evemts" id="past-evemts"></a>

対象の参照したい過去のイベント（アラート / インシデント）を見ることができます。例として、#125が分析の必要なイベントであった場合、それ以前のイベントも参照できます。

* \#125 - 対応対象のイベント
* \#120 - 確認対象の過去のイベント
* \#081 - 確認対象の過去のイベント

### ベースライン機能 <a href="#baselines" id="baselines"></a>

この機能では、機械学習とデータ（スクリーンショット）のセットが必要となりますが、トラブルシューティングに必要な情報をDevOpsチームに提供します。 \
この例ではAWS Synthetic Analysisにより分析をおこないます。具体的にはウエブサイトへ継続的にアクセスし、その応答時間にもとづいてベースラインを規定します。PITWALLでは、事前定義したスナップショット（ダッシュボード上のイメージ）を元に、これをおこないます。あるウエブサイトへ常時アクセスし、ベースラインを定義するために応答時間を記録しています。PITWALLは定義されたスナップショット（ダッシュボードイメージ）に対しこの機能を提供しています。

{% hint style="info" %}
ベースライン機能はロードマップに含まれており、2024年にリリースされる予定です。
{% endhint %}