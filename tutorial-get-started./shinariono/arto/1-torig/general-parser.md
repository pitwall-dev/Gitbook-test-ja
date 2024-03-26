# ℹ️ General Parser

### Overview

General Parser機能にて、カスタムWebhookによるアラートの受信が可能です。\
この機能は社内監視ツールや、アラートのデフォルトのペイロードを持たないツールに適しています。

### セットアップ

1.  トリガーとして”General Parser”を選択します。\


    <figure><img src="../../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>
2.  "Manage Alert"をクリックします。\




    <figure><img src="../../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>



    <figure><img src="../../../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>
3.  前提条件を確認し、カスタムペイロードを作成します。\
    &#x20;

    | KEY         | VALUE  | NOTE                                                                |
    | ----------- | ------ | ------------------------------------------------------------------- |
    | timestamp   | string | <p>Unix time in msec.</p><p>(ex.) “1695256040174”</p>               |
    | alertUrl    | string | URL format                                                          |
    | alertId     | string |                                                                     |
    | description | string |                                                                     |
    | severity    | string | <p>Available options<br>DEBUG | INFO | WARN | ERROR | CRITICAL </p> |
    | title       | string |                                                                     |

#### サンプルペイロード

"timestamp", "alertId", "title", "severity", "alertURL"は必須Keyです。

```
{
  “timestamp”: “1695256040174”,
  “alertId”: “1234567890abcd”,
  “title”: “Dummy Alert”,
  “severity”: “INFO”,
  “alertUrl”: “https://xxx.com/alert?id=0123456789abcd”,
  “hostname”: “abc.xxx.com”,
  “ip”: “10.10.10.10”,
  “customFields”: [
    {
      “key”: “incidentTitle”,
      “value”: “dummy incident”
    }
  ]
}

```

