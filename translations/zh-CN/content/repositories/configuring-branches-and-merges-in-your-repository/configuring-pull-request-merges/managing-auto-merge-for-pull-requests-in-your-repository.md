---
title: 管理仓库中拉取请求的自动合并
intro: 您可以允许或禁止仓库中拉取请求的自动合并。
product: '{% data reusables.gated-features.auto-merge %}'
versions:
  fpt: '*'
  ghes: '>=3.1'
  ghae: '*'
  ghec: '*'
permissions: People with maintainer permissions can manage auto-merge for pull requests in a repository.
topics:
  - Repositories
redirect_from:
  - /github/administering-a-repository/managing-auto-merge-for-pull-requests-in-your-repository
  - /github/administering-a-repository/configuring-pull-request-merges/managing-auto-merge-for-pull-requests-in-your-repository
shortTitle: 管理自动合并
---

## 关于自动合并

如果您允许自动合并仓库中的拉取请求，则具有写入权限的用户可以配置仓库中的单个拉取请求在满足所有合并要求时自动合并。 {% ifversion fpt or ghae-next or ghes > 3.1 or ghec %}If someone who does not have write permissions pushes changes to a pull request that has auto-merge enabled, auto-merge will be disabled for that pull request. {% endif %}更多信息请参阅“[自动合并拉取请求](/github/collaborating-with-issues-and-pull-requests/automatically-merging-a-pull-request)”。

## 管理自动合并

{% data reusables.pull_requests.auto-merge-requires-branch-protection %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
1. 在“Merge button（合并按钮）”下，选择或取消选择 **Allow auto-merge（允许自动合并）**。 ![允许或禁止自动合并的复选框](/assets/images/help/pull_requests/allow-auto-merge-checkbox.png)
