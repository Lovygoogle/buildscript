---
title: GitHub個人情報削除ポリシー
redirect_from:
  - /articles/github-sensitive-data-removal-policy
  - /github/site-policy/github-sensitive-data-removal-policy
versions:
  fpt: '*'
topics:
  - Policy
  - Legal
---

当社は、この個人情報削除プロセスを、アクセス認証情報が暴露されることによりセキュリティが危険にさらされているなど、[GitHub利用規約](/github/site-policy/github-acceptable-use-policies#3-conduct-restrictions)に反する高リスクコンテンツに限定した例外的なサービスとして提供しています。 このガイドでは、リポジトリから個人情報を削除するリクエストをGitHubが処理するために必要な情報について説明します。

## 個人情報とは

このドキュメントにおいて、「個人情報」とは、(i) 秘密にしておく必要があり、*かつ* (ii) 公開されることで特定のまたは標的を絞ったセキュリティリスクをあなたまたはあなたの組織にもたらすコンテンツを指します。

「セキュリティリスク」とは、肉体的な危険、個人情報の盗用、あるいは設備またはネットワーク施設への不正なアクセスの可能性が高まる状況を指します。

### 個人情報削除リクエストが適する状況
- 組織のサーバー、ネットワーク、またはドメインにアクセスするための、ユーザ名とパスワード、アクセストークン、またはその他の機密情報の組み合わせなどの、アクセス認証情報。
- あなたに代わって第三者にアクセスを許可する AWS トークンおよびその他同様のアクセス認証情報。 トークンが自分のものであることを示すことができなければなりません。
- 組織に特定のセキュリティリスクをもたらす文書 (ネットワーク図やアーキテクチャーなど)。
- あなた個人に関するものであり、セキュリティ上のリスクをもたらす[情報](/github/site-policy/github-community-guidelines#doxxing-and-invasion-of-privacy) (社会保障番号、国民識別番号など)。

### 個人情報削除リクエストが適して_いない_状況
- 内部サーバー名、IPアドレス、およびURLそれ自体。 特定のファイルまたはコードの一部分においてそれらを使用することがセキュリティ上の脅威をもたらすことを示す必要があります。
- 会社のアイデンティティ、名前、ブランド、ドメイン名など、GitHub 上のファイル内で単に会社に言及しているだけの場合。 会社のアイデンティティを利用することが会社のセキュリティ体制に対する脅威となる理由を明確にする必要があります。
- 特定のセキュリティリスクをもたらすことはないが、それ以外の理由で好ましくないと考えられるファイルやリポジトリ全体。
- あなたまたはあなたの組織の著作権を侵害している可能性のあるコンテンツを削除するリクエスト。 著作権関連の問題に対する GitHub の対応方法について質問がある場合や、著作権侵害の可能性があるコンテンツを報告したい場合は、[DMCA テイクダウンポリシー](/articles/dmca-takedown-policy/)をご確認ください。 一般的に個人情報削除プロセスはファイルやリポジトリ全体を削除することが目的ではなく、ファイル内で個人情報を含んだ特定部分のみが削除の対象となります。 ファイルの内容がすべて個人情報である場合もありますが、こうしたファイルを削除するためにはセキュリティリスクがあることを証明する必要があり、このような場合、リクエストの処理にかかる時間が長くなる可能性があります。
- 商標に関する紛争。 商標関連の問題に対する GitHub の対応方法について質問がある場合や、組織の商標やサービスマークを含んでいるコンテンツを報告したい場合は、[トレードマークポリシー](/articles/github-trademark-policy/)をご確認ください。
- プライバシーに関する苦情。 GitHub上の個人情報についてアクセス、転送、変更、削除を求める場合は、[プライバシー連絡フォーム](https://github.com/contact/privacy)からご連絡ください。
- マルウェアや汎用ツールなど、[コミュニティガイドライン](/articles/github-community-guidelines/)で管理されているコンテンツ。 コミュニティガイドラインについて質問がある場合や、GitHub のコンテンツがガイドラインに違反する可能性があると思われる場合は、{% data variables.contact.report_content %} を使用してそのコンテンツを報告できます。

## 知っておくべきこと

**まずは丁寧にお願いしてください。**当社にデータ削除のリクエストを送信する前に、まずはユーザに直接連絡することが重要です。 連絡先情報は公開プロフィールページやリポジトリの README または Support ファイルに記載されている場合があります。または、Issue を作成したり、リポジトリでプルリクエストを送信して連絡を取ることもできます。 これは厳密には義務ではありませんが、その方が印象の良いやり方と言えるでしょう。

**ボットを使わないでください。**熟練の専門家に、あなたが送信するすべてのリクエストの事実を評価してもらうべきです。 取り組みを第三者に外部委託している場合は、その活動内容を把握し、第三者が自動化されたボットを使用して苦情を一括送信していないことを確認してください。 こうした苦情には、セキュリティ上の脅威をもたらさないデータが含まれていることが少なくありません。また、十分な説明が含まれていないために、正当な苦情であっても何度も確認が必要となり、結果として遅延が生じる場合もあります。

**リクエストは正しく送信してください。**上述の通り、この個人情報削除プロセスは高リスクのコンテンツに限定した例外的なサービスとして提供しています。 このプロセスを使用して、著作権侵害の可能性のあるコンテンツなど、他の種類のコンテンツを削除することはできません。また、個人情報の削除リクエストを処理している間、他の種類の削除リクエストを同時に処理することはできません。 より迅速なサポートが可能になるよう、個人情報の削除リクエストは、著作権侵害の可能性のあるコンテンツを削除するリクエストとは別に送信してください。 リクエストが個人情報にのみ関係するのか、他の法的問題にも関係するのかわからない場合は、弁護士にご相談ください。

**処理にかかる時間について。**個人情報の削除リクエストはできるだけ速やかに処理しますが、処理するリクエストの量が多いため、リクエストの審査には時間がかかる場合があります。 リクエストを追加で送信したり、複数の連絡先からの複数のリクエストを送信したりすると、遅延が発生する場合があります。

## 具体的なプロセスは？

1. **申立人が調査します。**要請者は、自身で調査を実施し、[当社が求める詳細情報](#your-request-must-include)を提供する必要があります。最も重要なのは、データがどのようにセキュリティリスクをもたらすのかを説明することです。 GitHub は、個人または組織に代わって個人情報を検索したり、最初の決定を下す立場にはありません。

2. **申立人が個人情報の削除リクエストを送信します。**調査を実施した後、申立人は個人情報の削除リクエストを準備し、GitHub に[送信](#sending-a-private-information-removal-request)します。 リクエストがセキュリティリスクを立証するほど詳細でない場合や GitHub がデータを特定できない場合は、当社は返信して追加情報を求めます。

3. **GitHub がユーザに変更を要求します。**ほとんどの場合、当社はリポジトリを作成したユーザに連絡し、リクエストで指定された個人情報を削除または変更したり、クレームに異議を唱えたりする機会を与えます。

4. **ユーザが GitHub に変更を通知します。**ユーザは、指定された変更を行うことを決定した場合、指定された時間内にその旨を当社に通知する必要があります。 そうしなかった場合は、当社はリポジトリを無効にします。 ユーザが変更を行ったことを当社に通知した場合、当社は変更が行われたことを確認してから申立人に通知します。

  または

5. **ユーザはリクエストに異議を申し立てることができます。**問題のコンテンツがこのポリシーの対象となる個人情報ではないと思われる場合、ユーザは異議を唱えることができます。 この場合、通常は申立人に対して、任意でユーザに連絡し、ユーザとの間で、問題を合理的な範囲内で直接解決していただくことになります。

6. **申立人が変更を確認します。**ユーザが変更を加えた場合、申立人はそれを確認する必要があります。 変更が不十分な場合、申立人は GitHub にその理由を説明する詳細を提供する必要があります。 GitHub はリポジトリを無効にする場合もあれば、もう一度ユーザに変更を加える機会を与える場合もあります。

7. **ユーザは変更を加えるための追加猶予期間をリクエストできます。**ユーザが通知で指定された個人情報を削除する機会を逃した場合、リクエストがあれば、その変更を行うことができるよう、当社はもう一度 1 営業日程度の猶予期間を与える場合があります。 その場合、GitHub は申立人に通知します。

### フォークの場合は？ （またはフォークとは？）
GitHub の最も優れた機能の 1 つに、ユーザが互いのリポジトリを「フォーク」できることがあります。 どういうことかと言うと、 基本的に、ユーザは GitHub のプロジェクトのコピーを自分のリポジトリに作成できます。 ライセンスや法律で許可されている範囲で、ユーザはそのフォークを変更してメインプロジェクトに戻したり、プロジェクトの独自のバリエーションとして保持したりすることができます。 これらの各コピーは、元のリポジトリの「[フォーク](/articles/github-glossary/#fork)」であり、フォークの「親」とも呼ばれます。

GitHub は、親リポジトリを無効にするときにフォークを自動的に無効にしません。 これは、フォークはさまざまなユーザに属しており、著しく変更されている可能性があるためです。 GitHub がフォークに対して独立した調査を行うことはありません。 この調査は、個人情報の削除リクエストを送信する申立人が実施するようお願いいたします。フォークにも個人情報が含まれていると思われる場合は、リクエストにフォークを明示的に含めてください。

あなたが通知を送信した時点で、そのリポジトリの既存フォーク全体を指定して申し立てた場合、通知を処理する際に、そのネットワークにあるすべてのフォークに対して、有効な請求を適用します。 新しく作成されたフォークすべてに同じコンテンツが含まれる可能性を考慮して、これを行います。 さらに、報告するネットワークに含まれる報告内容が 100 リポジトリを超え、そのすべてを確認することが困難である際、通知の中であなたが「サンプルとして十分な数のフォークを確認した結果、私はこのフォークのすべてまたは大部分が、親リポジトリで報告した内容を含んでいるものと信じています」と記載している場合にはネットワーク全体の無効化を検討します。

## 個人情報削除リクエストを送信する

GitHub がホストするコンテンツの種類（主にソフトウェアコード）やコンテンツの管理方法（Git を使用）の性質上、苦情はできるだけ具体的にする必要があります。 ユーザが報告された個人情報を完全に削除したことを確認するために、当社は確認すべき箇所を正確に知る必要があります。

このガイドラインの目的は、個人情報削除リクエストの処理をできるだけ簡単にすることです。

### リクエストには以下を含める必要があります。

1. 個人情報を含む各ファイルへの有効でクリック可能なリンク。 （検索結果、例、スクリーンショットから処理することはできません。）
2. 個人情報を含む各ファイル内の具体的な行番号。
3. 特定した各アイテムが、あなたまたはあなたの組織にどのようにセキュリティリスクをもたらすかについての簡潔な説明。 ***単にデータがセキュリティリスクをもたらすという記述だけでなく、どのようにもたらされるかを説明することが重要です。***
4. セキュリティリスクに直面している組織の代理人として行動している第三者の場合は、その組織を代理して行動する法的権利があるという声明を含めてください。
5. 任意：リクエストが特に緊急であるかどうかと、その場合は理由をお知らせください。 当社は、すべての個人情報削除リクエストにできるだけ速やかに対応します。 しかし、ごく最近の認証情報が暴露されているなど、このリクエストが特に緊急を要する場合は、その理由を説明してください。

## リクエストの提出方法

個人情報削除リクエストは、[連絡フォーム](https://support.github.com/contact?tags=docs-private-information)から提出できます。 メッセージの本文には平文版のリクエストを含めてください。 添付ファイルでリクエストを送信した場合、処理に時間がかかる場合があります。

## 異議申し立て

当社から個人情報のリクエストを受け取った場合は、これに異議を申し立てることができます。その場合はメールに返信し、問題のコンテンツがこのポリシーの対象となる個人情報ではないと思われる理由を、可能な限り詳細にお知らせください。
