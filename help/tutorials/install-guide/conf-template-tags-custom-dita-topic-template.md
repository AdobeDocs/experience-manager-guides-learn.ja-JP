---
title: カスタム DITA トピックテンプレートの設定
description: カスタム DITA トピックテンプレートの設定方法を説明します
source-git-commit: 801c306fa120e7889d4b9428fd5bee2849bf1956
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 2%

---


# カスタム DITA トピックテンプレートの設定 {#id16A7G0O02TD}

AEMガイドには、次の DITA トピックテンプレートが付属しています。

- トピック

- タスク

- 概念

- 参照

- 用語集

- トラブルシューティング

- 空白


これらのテンプレートを使用すると、オーサリング要件に応じて、トピックテンプレートを作成できます。 空の DITA テンプレートには、他のテンプレートなどの構造や要素が含まれていません。 テンプレートが高度にカスタマイズされ、通常の DITA トピックテンプレートに基づいていない場合は、空白テンプレートを基本として使用できます。

DITA トピックテンプレートをカスタマイズしてオーサリングに使用するには、次の 3 つの主なタスクを実行する必要があります。

1. *\（オプション\）* [カスタム DITA テンプレートフォルダーのパスを設定](#id191LCF0095Z)

1. [カスタムオーサリングテンプレートの作成](conf-folder-level.md#id1917D0EG0HJ)

1. カスタムテンプレートをグローバルプロファイルまたはフォルダーレベルのプロファイルに追加する方法については、 [オーサリングテンプレートの設定](conf-folder-level.md#id1889D0IL0Y4) セクション


## カスタム DITA テンプレートフォルダーのパスを設定 {#id191LCF0095Z}

AEMガイドでは、カスタマイズした DITA マップとテンプレートを格納するフォルダーを設定できます。 デフォルトでは、テンプレートファイルは DAM の次のフォルダーに保存されます。

`/content/dam/dita-templates/`

トピックおよびマップテンプレートファイルを管理するために、トピックおよびマップテンプレートを保存する専用のフォルダがあります。 デフォルトでは、すべてのトピックテンプレートは、 `/content/dam/dita-templates/topics`

フォルダー。 すべてのマップテンプレートは、 `/content/dam/dita-templates/maps` フォルダー。

管理者は、カスタムマップまたはトピックテンプレートをデフォルトのフォルダに作成するか、独自のフォルダを作成してカスタムテンプレートを保存するかを選択できます。 デフォルトのフォルダを使用する予定がある場合は、このプロセスをスキップできます。

カスタム DITA トピックテンプレート用のフォルダーを設定するには、次の手順を実行します。

>[!IMPORTANT]
>
> デフォルトのフォルダーを使用してカスタムテンプレートを保存する場合は、この処理をスキップできます。

1. Adobe Experience Manager Web コンソール設定ページを開きます。

   設定ページにアクセスするデフォルトの URL は次のとおりです。

   ```http
   http://<server name>:<port>/system/console/configMgr
   ```

1. を検索して、 *com.adobe.fmdita.config.ConfigManager* バンドル。

1. 内 **テンプレートの場所** プロパティを指定し、カスタムテンプレートを保存する場所を指定します。

1. 「**保存**」をクリックします。


指定した場所が DAM に存在する場合、デフォルトのマップおよびトピックテンプレートがすべてそのフォルダーにコピーされます。 場所が存在しない場合は、すべてのデフォルトのマップおよびトピックテンプレートを使用してフォルダーが作成されます。

**親トピック：**[&#x200B;トピックとマップのテンプレートの設定](conf-template-tags.md)
