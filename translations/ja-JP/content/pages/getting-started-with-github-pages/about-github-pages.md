---
title: GitHub Pages について
intro: 'You can use {% data variables.product.prodname_pages %} to host a website about yourself, your organization, or your project directly from a repository on {% ifversion ghae %}{% data variables.product.product_name %}{% else %}{% data variables.product.product_location %}{% endif %}.'
redirect_from:
  - /articles/what-are-github-pages/
  - /articles/what-is-github-pages/
  - /articles/user-organization-and-project-pages/
  - /articles/using-a-static-site-generator-other-than-jekyll/
  - /articles/mime-types-on-github-pages/
  - /articles/should-i-rename-usernamegithubcom-repositories-to-usernamegithubio/
  - /articles/about-github-pages
  - /github/working-with-github-pages/about-github-pages
product: '{% data reusables.gated-features.pages %}'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pages
---

## {% data variables.product.prodname_pages %} について

{% data variables.product.prodname_pages %} は、{% data variables.product.product_name %} のリポジトリから HTML、CSS、および JavaScript ファイル を直接取得し、任意でビルドプロセスを通じてファイルを実行し、ウェブサイトを公開できる静的なサイトホスティングサービスです。 {% data variables.product.prodname_pages %} サイトの例については、[{% data variables.product.prodname_pages %} サンプル集](https://github.com/collections/github-pages-examples)で見ることができます。

{% ifversion fpt or ghec %}
{% data variables.product.prodname_dotcom %} の`github.io` ドメインまたはご自身のカスタムドメインで、サイトをホストできます。 詳細は「[{% data variables.product.prodname_pages %} でカスタムドメインを使用する](/articles/using-a-custom-domain-with-github-pages)」を参照してください。
{% endif %}

{% ifversion fpt or ghec %}
{% data reusables.pages.about-private-publishing %} 詳しい情報については、「[{% data variables.product.prodname_pages %} サイトの可視性を変更する](/pages/getting-started-with-github-pages/changing-the-visibility-of-your-github-pages-site)」を参照してください。
{% endif %}

作成方法については、「[{% data variables.product.prodname_pages %} サイトを作成する](/articles/creating-a-github-pages-site)」を参照してください。

{% ifversion fpt or ghes > 3.0 or ghec %}
Organizationのオーナーは、Organizationのリポジトリからの{% data variables.product.prodname_pages %}サイトの公開を無効化できます。 詳しい情報については「[Organizationの{% data variables.product.prodname_pages %}サイトの公開の管理](/organizations/managing-organization-settings/managing-the-publication-of-github-pages-sites-for-your-organization)」を参照してください。
{% endif %}

## {% data variables.product.prodname_pages %} サイトの種類

{% data variables.product.prodname_pages %} サイトには、3 つの種類があります。プロジェクト、ユーザ、そして Organization です。 プロジェクトサイトは、JavaScript ライブラリやレシピ集など、{% data variables.product.product_name %} の特定のプロジェクトに関するものです。 User and organization sites are connected to a specific account on {% ifversion ghae %}{% data variables.product.product_name %}{% else %}{% data variables.product.product_location %}{% endif %}.

ユーザサイトを公開するには、{% ifversion fpt or ghec %}`<username>.github.io`{% else %}`<username>.<hostname>`{% endif %} という名前のユーザアカウントが所有するリポジトリを作成する必要があります。 Organization サイトを公開するには、 {% ifversion fpt or ghec %}`<organization>.github.io`{% else %}`<organization>.<hostname>`{% endif %}という名前のOrganizationが所有するリポジトリを作成する必要があります。 {% ifversion fpt or ghec %}カスタムドメインを使用している場合を除き、ユーザサイトと Organization サイトは `http(s)://<username>.github.io` または `http(s)://<organization>.github.io` で利用できます。{% elsif ghae %}ユーザサイトと Organization サイトは `http(s)://pages.<hostname>/<username>` または `http(s)://pages.<hostname>/<organization>` で利用できます。{% endif %}

プロジェクトサイトのソースファイルは、プロジェクトと同じリポジトリに保存されます。 {% ifversion fpt or ghec %}カスタムドメインを使用している場合を除き、プロジェクトサイトは `http(s)://<username>.github.io/<repository>` または `http(s)://<organization>.github.io/<repository>` で利用できます。{% elsif ghae %}プロジェクトサイトは `http(s)://pages.<hostname>/<username>/<repository>/` または `http(s)://pages.<hostname>/<organization>/<repository>/` で利用できます。{% endif %}

{% ifversion fpt or ghec %}
サイトを非公開で公開する場合、サイトの URL が異なります。 詳しい情報については、「[{% data variables.product.prodname_pages %} サイトの可視性を変更する](/pages/getting-started-with-github-pages/changing-the-visibility-of-your-github-pages-site)」を参照してください。
{% endif %}

{% ifversion fpt or ghec %}
カスタムドメインがサイトの URL に与える影響に関する詳しい情報については、「[カスタムドメインと {% data variables.product.prodname_pages %} について](/articles/about-custom-domains-and-github-pages)」を参照してください。
{% endif %}

{% data variables.product.product_name %} のアカウントごとに作成できるユーザまたは Organization サイトは 1 つだけです。 プロジェクトサイトの数については、Organization アカウントでもユーザアカウントでも、無制限です。

{% ifversion ghes %}
サイトが利用できる URL については、{% data variables.product.product_location %} で Subdomain Isolation を有効にしているかどうかで異なります。

| サイトの種類 | Subdomain Isolation が有効 | Subdomain isolation が無効 |
| ------ | ----------------------- | ----------------------- |
|        |                         |                         |
 ユーザ | 

`http(s)://pages.<hostname>/<username>` | `http(s)://<hostname>/pages/<username>` | Organization | `http(s)://pages.<hostname>/<organization>` | `http(s)://<hostname>/pages/<organization>` | ユーザアカウントが所有するプロジェクトサイト | `http(s)://pages.<hostname>/<username>/<repository>/` | `http(s)://<hostname>/pages/<username>/<repository>/` Organization アカウントが所有するプロジェクトサイト | `http(s)://pages.<hostname>/<orgname>/<repository>/` | `http(s)://<hostname>/pages/<orgname>/<repository>/`

詳しい情報については、 「[Subdomain Isolation を有効化する](/enterprise/{{ currentVersion }}/admin/installation/enabling-subdomain-isolation)」を参照するか、サイト管理者にお問い合わせください。
{% endif %}

## {% data variables.product.prodname_pages %} サイトの公開元

{% data variables.product.prodname_pages %} サイトの公開元は、サイトのソースファイルが保存されているブランチまたはフォルダです。

{% data reusables.pages.private_pages_are_public_warning %}

デフォルトの公開元がリポジトリに存在する場合、{% data variables.product.prodname_pages %} はそこから自動的にサイトを公開します。 ユーザサイトと Organization サイトのデフォルトの公開元は、リポジトリのデフォルトブランチのルートです。 プロジェクトサイトのデフォルトの公開元は、`gh-pages` ブランチのルートです。

サイトのソースファイルを別の場所に保持する場合は、サイトの公開元を変更できます。 リポジトリ内の任意のブランチから、そのブランチのリポジトリのルート、`/`、またはそのブランチの `/docs` フォルダからサイトを公開できます。 詳しい情報については「[{% data variables.product.prodname_pages %} サイトの公開元を設定する](/articles/configuring-a-publishing-source-for-your-github-pages-site#choosing-a-publishing-source)」を参照してください。

公開元としていずれかのブランチの `/docs` フォルダを選択した場合{% ifversion fpt or ghec %}、{% data variables.product.prodname_pages %} は`/docs` フォルダから _CNAME_ ファイル{% endif %}を含むサイトを公開するためのすべてを読み取ります。{% ifversion fpt or ghec %}たとえば、{% data variables.product.prodname_pages %} 設定を使用してカスタムドメインを編集すると、カスタムドメインは `/docs/CNAME` に書き込みます。 _CNAME_ ファイルに関する詳しい情報については、「[{% data variables.product.prodname_pages %} サイト用のカスタムドメインを管理する](/articles/managing-a-custom-domain-for-your-github-pages-site)」を参照してください。{% endif %}


## 静的サイトジェネレータ

{% data variables.product.prodname_pages %} は、リポジトリにプッシュされたあらゆる静的ファイルを公開します。 静的ファイルを自分で作成することも、静的サイトジェネレータでサイトをビルドすることも可能です。 ローカルまたは別のサーバー上で独自のビルドプロセスをカスタマイズすることもできます。 {% data variables.product.prodname_pages %} に組み込まれている静的サイトジェネレータで、ビルドプロセスを容易化できる Jekyll のご利用をおすすめします。 詳しい情報については、「[{% data variables.product.prodname_pages %} と Jekyll](/articles/about-github-pages-and-jekyll)」を参照してください。

{% data variables.product.prodname_pages %} は、デフォルトでは Jekyll を使ってサイトを構築します。 Jekyll 以外の静的サイトジェネレータを使いたい場合、公開元のルートに `.nojekyll` という空のファイルを作成し、お使いの静的サイトジェネレータの指示に従ってローカルでサイトをビルドします。

{% data variables.product.prodname_pages %} は、PHP、Ruby、Python などのサーバーサイド言語はサポートしていません。

## {% data variables.product.prodname_pages %} を使用するためのガイドライン

{% ifversion fpt or ghec %}
- 2016 年 6 月 15 日以降に作成され、`github.io` ドメインを使用して作成された {% data variables.product.prodname_pages %} サイトは、HTTPS 経由で配信されます。 2016 年 6 月 15 日までにサイトを作成した場合は、サイトへのトラフィックに対して、HTTPS サポートを有効にすることができます。 詳しい情報については「[HTTPS で{% data variables.product.prodname_pages %}サイトをセキュアにする](/articles/securing-your-github-pages-site-with-https)」を参照してください。
- {% data reusables.pages.no_sensitive_data_pages %}
- {% data variables.product.prodname_pages %} の使用には、転売禁止を含めて、[GitHub 利用規約](/free-pro-team@latest/github/site-policy/github-terms-of-service/)が適用されます。

### 使用制限
{% endif %}
{% data variables.product.prodname_pages %} サイトには、次の使用制限があります:

  - {% data variables.product.prodname_pages %} ソースリポジトリには、1GB の推奨上限があります。{% ifversion fpt or ghec %}詳しい情報については、「[私のディスク容量はいくつですか？](/articles/what-is-my-disk-quota/#file-and-repository-size-limitations)」を参照してください。{% endif %}
  - 公開された{% data variables.product.prodname_pages %}のサイトは1GB以上であってはなりません。
{% ifversion fpt or ghec %}
  - {% data variables.product.prodname_pages %} サイトには、月当たり 100GB の*ソフトな*帯域幅制限があります。
  - {% data variables.product.prodname_pages %} サイトには、時間当たり 10 ビルドの*ソフトな*制限があります。

あなたのサイトがこれらの使用割当量を超えている場合、あなたのサイトにサービスを提供できないか、{% data variables.contact.contact_support %} から、あなたのサイトが当社のサーバーに与える影響を減らす方法を示唆するメールが届くことがあります。そうした方法の例としては、サードパーティのコンテンツ配信ネットワーク (CDN) をサイトの前に配置したり、リリースなどの他の {% data variables.product.prodname_dotcom %} 機能を利用したり、ニーズに合った別のホスティングサービスに移行したりすることなどが挙げられます。

### 禁止される用途

{% data variables.product.prodname_pages %} は、オンラインビジネス、eコマースサイト、主に商取引の円滑化またはサービスとしての商用ソフトウェアの提供 (SaaS) のどちらかを目的とする、その他のウェブサイトを運営するための無料のウェブホスティングサービスとしての使用を意図したものではなく、またそのような使用を許可するものでもありません。

加えて、{% data variables.product.prodname_dotcom %} は{% data variables.product.prodname_pages %} の特定の目的またはアクティビティへの使用を許可していません。 禁止されている用途のリストについては、「[{% data variables.product.prodname_dotcom %} の {% data variables.product.prodname_pages %} に関する追加製品の利用規約](/free-pro-team@latest/github/site-policy/github-terms-for-additional-products-and-features#pages)」を参照してください。
{% endif %}

## {% data variables.product.prodname_pages %} での MIME タイプ

MIME タイプとは、ブラウザがリクエストするファイルの性質やフォーマットに関する情報を提供するため、サーバーがブラウザに送信するヘッダのことです。 {% data variables.product.prodname_pages %} は、数千のファイル拡張子にわたり、750 を超える MIME タイプをサポートしています。 サポートする MIME タイプのリストは、[mime-db project](https://github.com/jshttp/mime-db) から生成されます。

ファイルごと、リポジトリごとにカスタム MIME タイプを指定することはできませんが、{% data variables.product.prodname_pages %} で使う MIME タイプを追加や変更することは可能です。 詳しい情報については、「[mime-db コントリビューションガイドライン](https://github.com/jshttp/mime-db#adding-custom-media-types)」を参照してください。

## 参考リンク

- {% data variables.product.prodname_learning %} の [{% data variables.product.prodname_pages %}](https://lab.github.com/githubtraining/github-pages)
- 「[{% data variables.product.prodname_pages %}](/rest/reference/repos#pages)」
