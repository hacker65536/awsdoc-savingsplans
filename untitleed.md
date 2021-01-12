# What is Saveings Plan?

`Savings Plans` とは柔軟な課金モデルで、 Amazon EC2、AWS Fargate、そして AWS Lambda の使用量を最大72%節約できる。`Savings Plans` は1-3年契約の一貫した使用量のコミットメントと引き換えに低価格を提供する。`Savings Plans` は 管理アカウントもしくはメンバーアカウントのどちらからでも購入することができる。`Saving Plans` はそのプランの所有アカウントで最初に適応され、それから AWS Organizationにあるその他のアカウントに適応される。

すべての compute usage タイプは `On-Demand` レートと `Savmings Plans` レートを持っている。例えば、 `$10/hour` の compute usage をコミットした場合、`10$` までは `Savings Plans` で課金され、`Savings Plans` を超えた使用量は通常の `On-Demand` レートで請求されます。

`Savings Plans` にサインアップすると、compute usage に支払う価格は プラン期間通して同じである。すべて前払い、一部前払い、前払いなしのいずれかの支払いを行う事が可能である。

まず、`AWS Cost Explorer` からお勧めの `Savings Plans` を確認、`Savings Plans` の購入と管理、AWSの利用履歴の確認を行う。これらは `Savings Plans` の最適化レベルを知るには便利である。`recomendation` をカスタマイズし必要な `Savings plan` の購入を行うことができる。`Savings Plans` のすべての対象サービスは  \[aaa\]\(aaaa\)`Working with supported services` から確認できる。

### Plan types

* Compute Savings Plans 
  * 最も柔軟で、最大 On-Demand レートの 66% off の価格となる。このプランは Instance family \(M5,C5,etc.\)、 Instance size\(c5.large,c5xlarge, etc.\)、 リージョン\(us-east-1,us-east-2,etc.\)、OS\(Windows,Linux,etc.\)、テナンシー\(default\[shared\], dedicated, dedicated host\)に関係なく自動的にEC2の利用量に適応される。また、FargateとLambdaにも適応される。Compute Savings Plansを利用すると、いつでもワークロードを C5 から M5に、 EU\(Ireland\)からEU\(London\)に、もしくは、Amazon EC2から Amazon ECS \(Fargate\)にアプリケーションを移行することができる。これらの変更をしても、Compute Savings Plansの提供する低価格の恩恵を続けて受けることができる。
* EC2 Instance Savings Plans
  * 最大で On-Demand から72%の offの節約となる。その代わりinstance familyとregionを指定したコミットメントが必要。このプランは自動でリージョン内のinstance familyに対して適応される。 size、OS、tenancyに制限はない。

    EC2 Instance Savings Planでは 同 instance familyでのsize、OS、テナンシーの変更しても、ディスカウントレートを引き続き受けることができる。

#### note

`Savings Plans` が提供する低価格はコミットメントが必要。コミットメントの期間は購入後に変更することはできない。もし利用量が変化があれば追加の Savings Plans を契約しなければいけない。

専有 instance は 一台でも起動しているとそのリージョンに対して`$2/hour` の課金が生じる。この専有 fee は `Savings plans` の割引対象外。

２つのプランは Amazon EMR、 Amazon EKS、そしてAmazon ECS clustersの一部である EC2 instanceに対して適応される。Amazon EKSは `Savings Plans` の対象ではないが、配下の EC2 instance は対象である。

### Savings Plans and RIs

`Savings Plans` はAmazon EC2 RIs のような低価格を提供するが、さらに柔軟性が加わる。`Savings Plans` では、特定の instance 構成の代わりに 時間単位 \($/hour\)の一定の compute 利用量を確約することで請求をへらすことができる。 `Savings Plans` は取替や変更の必要性なく、ニーズに最適な低価格を conput optionによって柔軟さを提供する。

`Compute Savings Plans` は On-Demand から 最大 66% off を提供する。Convertibale RIsと近い。 `Compute Savings Plans` は自動的に EC2 instance、Fargate、Lambda の使用量のコストから削減が適応される。`EC2 Instance Savings Plans` は最大で On-Demand から 72% off を提供する。Standard RIsと近い。そして、自動的に 選択したRegionにあるInstance familyに属するEC2 instanceのコストを削減してくれる。

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">Compute Savings Plans</th>
      <th style="text-align:left">EC2 Instance Savings Plans</th>
      <th style="text-align:left">Convertible RIs*</th>
      <th style="text-align:left">
        <p>Standard RIs</p>
        <p></p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Savings over On-Demand</td>
      <td style="text-align:left">Up to 66 percent</td>
      <td style="text-align:left">Up to 72 percent</td>
      <td style="text-align:left">Up to 66 percent</td>
      <td style="text-align:left">Up to 72 percent</td>
    </tr>
  </tbody>
</table>

