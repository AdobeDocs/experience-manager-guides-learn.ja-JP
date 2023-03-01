---
title: AEMガイド用の新しいマイクロサービスベースの公開の設定をas a Cloud Service
description: AEMガイド用の新しいマイクロサービスベースの公開を設定する方法について説明します。
source-git-commit: afbc1712cf45dd0b570e20683946af6a86edae7e
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# AEMガイド用の新しいマイクロサービスベースの公開の設定をas a Cloud Service

新しい公開マイクロサービスを使用すると、as a Cloud ServiceのAEMガイドで大規模な公開ワークロードを同時に実行し、業界をリードするAdobe I/O Runtimeのサーバレスプラットフォームを活用できます。

発行リクエストごとに、AEMガイドはas a Cloud Service的に個別のコンテナを実行し、ユーザーのリクエストに従って水平方向に拡大/縮小します。 これにより、ユーザーは、複数の公開リクエストを実行し、大規模なオンプレミスのAEMサーバーよりも高いパフォーマンスを得ることができます。

新しいクラウド公開サービスはAdobe IMSJWT ベースの認証で保護されるので、お客様は以下の手順に従って、Adobeのセキュアなトークンベースの認証ワークフローと環境を統合し、新しいクラウドベースのスケーラブル公開ソリューションの使用を開始する必要があります。


## Adobe Developer Console での IMS 設定の作成

**統合の作成に必要なロール**:システム管理者

Adobe Developer Console で IMS 設定を作成するには、次の手順を実行します。

1. 開発者コンソールを開きます。 `https://developer.adobe.com/console`.

1. 切り替え先 **プロジェクト** タブを上から開きます。

   <img src="assets/projects-tab.png" alt="「プロジェクト」タブ" width="500">

1. 新しい空のプロジェクトを作成するには、「 **空のプロジェクト** から **新規プロジェクトを作成** ドロップダウン。

   <img src="assets/create-new-project.png" alt="新規プロジェクトを作成" width="500">

1. 選択 **API** から **プロジェクトに追加** ドロップダウンを使用して、IO 管理 API をプロジェクトに追加します。

   <img src="assets/add-project.png" alt="プロジェクトを追加" width="300">

   <img src="assets/io-management-api.png" alt="io 管理" width="500">

1. API の追加時に、新しい秘密鍵と公開鍵のペアを作成します。 これにより、システム上の秘密鍵が自動的にダウンロードされます。

   <img src="assets/generate-key-pair.png" alt="キーペアを生成" width="500">

1. 設定した API を保存します。

   <img src="assets/save-api.png" alt="api を保存" width="600">

1. に戻る **プロジェクト** タブをクリックし、 **プロジェクトの概要** 左側に

   <img src="assets/project-overview.png" alt="プロジェクトの概要" width="500">

1. クリック **ダウンロード** ボタンを上部に配置して、サービス JSON をダウンロードします。

   <img src="assets/download-json.png" alt="json をダウンロード" width="500">

これで、JWT 認証の詳細を設定し、秘密鍵とサービスの詳細 JSON もダウンロードしました。 これらの 2 つのファイルは、次の節で必要となるので、手元に置いておいてください。

### 環境に IMS 設定を追加する

IMS 設定を環境に追加するには、次の手順を実行します。

1. Experience Manager を開き、設定する環境を含むプログラムを選択します。
1. 切り替え先 **環境** タブをクリックします。
1. 設定する環境名をクリックします。 これにより、環境情報ページに移動します。
1. 切り替え先 **設定** タブをクリックします。
1. 秘密鍵とプロジェクト JSON をアップロードします（下のスクリーンショットを参照）。 次に示すように、同じ名前と設定を使用していることを確認します。

   <img src="assets/ims-config-environment.png" alt="ims 設定" width="500">

>[!NOTE]
>
> 上のスクリーンショットに示すように、秘密鍵とサービスの詳細 JSON ファイルの内容を開き、コピーし、設定パネルの value 列に貼り付ける必要があります。

IMS 設定を環境に追加したら、次の手順を実行して、OSGi を使用してこれらのプロパティをAEMガイドにリンクします。

1. Cloud Manager の Git プロジェクトコードで、以下の 2 つのファイルを追加します ( ファイルの内容については、 [付録](#appendix)) をクリックします。

   * `com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`
   * `com.adobe.fmdita.publishworkflow.PublishWorkflowConfigurationService.xml`
1. 新しく追加されたファイルが、 `filter.xml`.
1. Git の変更をコミットしてプッシュします。
1. パイプラインを実行して、環境に変更を適用します。

その後、新しいマイクロサービスベースのクラウドパブリッシングを使用できるようになります。

## 付録 {#appendix}

**ファイル**:
`com.adobe.aem.guides.eventing.ImsConfiguratorService.cfg.json`

**コンテンツ**:

```
{
  "service.account.details": "$[secret:SERVICE_ACCOUNT_DETAILS]",
  "private.key": "$[secret:PRIVATE_KEY]"
}
```

**ファイル**: `com.adobe.fmdita.publishworkflow.PublishWorkflowConfigurationService.xml`

**コンテンツ**:

```
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:jcr="http://www.jcp.org/jcr/1.0" xmlns:sling="http://sling.apache.org/jcr/sling/1.0"
          jcr:primaryType="sling:OsgiConfig"
          dxml.publish.microservice.url="https://adobeioruntime.net/api/v1/web/543112-guidespublisher/default/publishercaller.json"
          dxml.use.publish.microservice="{Boolean}true"
/>
```