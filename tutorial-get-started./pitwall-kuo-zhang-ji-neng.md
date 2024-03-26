# 🔩 PITWALL拡張機能

## 拡張機能とは？

拡張機能はPITWALL にデフォルトで装備されている機能に加えて、次のような追加機能を実装するために使用できるコンポーネントのセットです。

1. ツールのアイコンを追加してStudio UIを充実させます。
2. Studioでパラメータ化するURL からタイムスタンプを検出するための時間形式を追加します。

### 1. ツールのアイコンを追加してStudio UIを充実させます。

PITWALLにはコミュニティメンバーが提供したさまざまなツール / サイトが用意されています。\
ただし、常に新しいツール、サイト、自身のアセットの更新が続くため、Studioに新しい宛先を追加すると、次のように空のアイコンが表示されることがあります。 それは味気ない...

<figure><img src="../.gitbook/assets/image (56).png" alt=""><figcaption><p>AWS Health Status without an icon.</p></figcaption></figure>

次の手順で新しい拡張機能を登録してUIを充実させましょう。

1. アップロードするアイコン画像を用意します。
2. 「拡張機能」に移動して、新しい「拡張機能」を追加します。
3. URL の重要な部分を名前を付けて貼り付けます。 これにより、PITWALL がStudioでサイト / ツールをパターンマッチングで検出できるようになります。

{% embed url="https://drive.google.com/file/d/1VcpnIMNnW6FsJK-8Dw2sbflfKghpAhuc/view?usp=sharing" %}

これで、Studioのアイコンを追加することで、シナリオの見栄えが大幅に向上しました。これは公開拡張機能として提供されているため、誰でも利用できるようになりました。プライベート拡張機能として登録すれば、自身のテナントにのみ登録できます。

<figure><img src="../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

### 2. Studioでパラメータ化するURL からタイムスタンプを検出するための時間形式を追加します。

PITWALLユーザーの一人がCoralogixのトレースビューのタイムスタンプ形式に対応するために提供した拡張機能の一つを紹介します。この拡張機能はURLの "from "と "to "のタイムスタンプを検出する方法を定義しています。

`from%3A[0-9]{4}-[0-9]{2}-[0-9]{2}T[0-9]{2}%3A[0-9]{2}%3A[0-9]{2}.[0-9]{3}Z`

`to%3A[0-9]{4}-[0-9]{2}-[0-9]{2}T[0-9]{2}%3A[0-9]{2}%3A[0-9]{2}.[0-9]{3}Z`

<figure><img src="../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

この拡張機能によりPITWALLはCoralogixのトレース ビューからタイムスタンプを検出できるようになります。

[https://YOURTENANT.coralogix.com/#/query-new/tracing?metadataFilters=%5B%7B%22metadataField%22%3A1%2C%22values%22%3A%5B%5D%7D%2C%7B%22metadataField%22%3A2%2C%22values%22%3A%5B%5D%7D%2C%7B%22metadataField%22%3A3%2C%22values%22%3A%5B%5D%7D%2C%7B%22metadataField%22%3A4%2C%22values%22%3A%5B%5D%7D%5D\&tagFilters=%5B%5D\&traceId=null\&time=%22from%3A2022-10-01T18%3A04%3A00.000Z%2Cto%3A2022-10-01T18%3A19%3A00.000Z%22](https://tocaro-prod.coralogix.com/#/query-new/tracing?metadataFilters=%5B%7B%22metadataField%22%3A1%2C%22values%22%3A%5B%5D%7D%2C%7B%22metadataField%22%3A2%2C%22values%22%3A%5B%5D%7D%2C%7B%22metadataField%22%3A3%2C%22values%22%3A%5B%5D%7D%2C%7B%22metadataField%22%3A4%2C%22values%22%3A%5B%5D%7D%5D\&tagFilters=%5B%5D\&traceId=null\&time=%22from%3A2022-10-01T18%3A04%3A00.000Z%2Cto%3A2022-10-01T18%3A19%3A00.000Z%22)

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

このアプローチでは、自身のツールまたは新しいクラウドサービスを含むさまざまなツールに対応できます。
