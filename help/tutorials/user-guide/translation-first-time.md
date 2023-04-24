---
title: コンテンツ翻訳のベストプラクティス
description: コンテンツ翻訳のベストプラクティスを学ぶ
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 2%

---


# コンテンツ翻訳のベストプラクティス {#id1678G0S702F}

コンテンツを翻訳する際は、次の点を考慮してください。

- フォルダー名とファイル名は、などのファイル命名規則に従う必要があります。スペース、アポストロフィ、中括弧、等号、特殊文字、非 ASCII 文字は使用できません。

- 異なる言語のコンテンツを翻訳する場合は、各言語に対応するフォルダーを作成する必要があります。 これらの各言語フォルダーには、その言語に対応するコンテンツが含まれます。 例えば、 `de` ドイツ語の `fr` フランス語など。 または、 `fr-FR` フランスで使われるフランス語や `fr-CA` カナダで使用されているフランス語の場合
- また、ターゲット言語には、インスタンス上のターゲット言語フォルダーに従って選択された実際のロケールが含まれている必要があります。
- クラウド設定は、ソースフォルダーのクラウド設定と同じにする必要があり、1 つのフォルダーには 1 つのクラウド設定のみ存在する必要があります。 複数の翻訳コネクタを使用する場合は、/conf の下に複数のフォルダーを作成できます。
- 1 つのフォルダーに含めるファイルの数は 1,000 個以下にする必要があります。
- 翻訳プロセスの開始を担当するユーザーが、ソース言語フォルダーとターゲット言語フォルダーに対する読み取り、変更、作成、削除の権限を持っていることを確認します。
- コンテンツを翻訳するには翻訳プロジェクトを作成する必要があるので、AEMでプロジェクトを作成するには、ユーザーにアクセス権が必要です。
- マップで条件付きプリセットを使用する場合は、翻訳プロセスを開始する前に条件付きプリセットを作成する必要があります。 条件付きプリセットは翻訳版のマップにもバンドルされているので、翻訳プロセスを開始する前にプリセットを作成し、翻訳版で使用できるようにします。
- コンテンツ翻訳プロセスは、AEM Assets UI ではなく、DITA マップコンソールから開始する必要があります。
- 人による翻訳を使用してコンテンツを翻訳する場合は、コンポーネントベースの DITA 翻訳ワークフローを使用しないでください。 ただし、機械翻訳にはこのオプションを使用する必要があります。
- ローカリゼーションを必要としない、グローバルに使用されるコンテンツやメディアは、言語コピーの外に置く必要があります。
- ローカライズが必要な共通コンテンツは、すべて言語フォルダーの下の共通フォルダーに保持する必要があります。

次の図に、コンテンツと 3 つの言語コピーをグローバルに使用したAEMのフォルダー構造の例を示します。

![](images/aem-directory_structure.png)

## 翻訳サービスの設定

使用する人間または機械翻訳サービスを設定するには、次の手順を実行します。

1. Assets UI で、ソース言語フォルダーを選択します。

1. フォルダーのプロパティを開き、に移動します。 **Cloud Services** タブをクリックします。

1. 内 **Cloud Services** タブで、使用する翻訳サービスを設定します。

   機械ベースまたは人間による翻訳を設定できます。

   1 つのフォルダーに翻訳コネクタの設定が 1 つだけあることを確認します。 翻訳コネクタが複数ある場合は、/conf の下に複数のフォルダーを作成できます。 翻訳プロセスを開始する前に、ソース言語フォルダーでクラウド設定を選択する必要があります。

   >[!NOTE]
   >
   > 詳しくは、 [翻訳統合フレームワークの設定](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/integration-framework.html?lang=en) サードパーティの翻訳サービスとの統合について詳しくは、 AEMのドキュメントを参照してください。

1. クリック **保存して閉じる** をクリックして、更新したフォルダーのプロパティを保存します。


>[!TIP]
>
> 詳しくは、 *翻訳* 」の節を参照してください。

## 新しい翻訳プロジェクトを作成

翻訳プロジェクトを作成するには、次の手順を実行します。

>[!NOTE]
>
> この手順を実行する前に、必要な言語ルートおよびターゲットフォルダーが、 [コンテンツ翻訳のベストプラクティス](#id1678G0S702F).

1. Assets UI で、DITA マップファイルをクリックします。

1. 次をクリック： **翻訳** タブをクリックします。

1. 次の **ターゲット言語** リストで、プロジェクトを翻訳するロケールを選択し、 **完了**.

   トピックと関連アセットの概要と詳細が表示されます。

   >[!IMPORTANT]
   >
   > この **ターゲット言語** 言語フォルダーがソース言語と並行して作成された言語のみを表示します。 ソース言語フォルダーから 1 レベル下のレベルなど、他のレベルで作成された言語フォルダーも表示されません。 すべてのターゲット言語フォルダーを、ソース言語フォルダーと同じレベルで作成してください。

1. 翻訳用に送信するトピックを選択します。

   また、次のトピックのフィルタリングオプションを使用できます。

   >[!NOTE]
   >
   > 必要なフィルターを適用したら、 **完了** を使用して、選択した内容に基づいてトピックをフィルタリングします。

   - **翻訳ステータス**:翻訳ステータスに基づいてトピックをフィルタリングすることを選択します。 次のオプションを使用できます。非同期、コピーが見つからない、処理中、同期中。
   - **検索**:1 つまたは複数の語句を入力して、トピックのタイトルを検索します。
   - **ソースタイプ**:ファイルタイプに基づいてトピックをフィルタリングするよう選択します。 次のオプションを使用できます。すべて、DITA、DITA マップ、リソース。
   - **ソースのバージョン変更後**:変更日時に基づいてトピックをフィルタリングすることを選択します。 指定した日時以降に変更されたすべてのトピックがリストに表示されます。
   - **ベースライン**:「ベースラインを使用」をクリックし、マップ上に作成したベースラインを選択します。 選択したベースラインの一部であるすべてのファイルが、翻訳ページに表示されます。 ベースラインから目的のファイルを選択し、翻訳プロセスを続行できます。 コンテンツが翻訳されたら、翻訳されたベースラインを書き出すことができます。 翻訳されたベースラインのエクスポートについて詳しくは、 [翻訳済みベースラインを書き出し](generate-output-use-baseline-for-publishing.md#id196SE600GHS).
1. クリック **言語コピーを作成/更新** をクリックします。

1. 次の **プロジェクト** リスト、選択 **新しい翻訳プロジェクトを作成**.

   >[!NOTE]
   >
   > 既に翻訳プロジェクトがある場合は、そのプロジェクトにトピックを追加できます。 選択 **既存の翻訳プロジェクトに追加** オプションを **プロジェクト** リストを表示し、 **既存の翻訳プロジェクト** リスト。

1. 「**プロジェクトタイトル**」フィールドに、プロジェクトのタイトルを入力します。

1. を選択します。 **DITA マップを含める** 翻訳するマップを送信するオプション。
1. クリック **開始** 新しい翻訳プロジェクトを作成します。

   トピックの選択したバージョンで新しい翻訳プロジェクトが作成されます。 この時点で、翻訳プロジェクトが作成されたことを確認するポップアップメッセージが表示されます。 翻訳プロジェクトですべてのターゲット言語コピーが使用可能になったら、インボックスに通知が表示されます。 翻訳プロジェクトで使用可能なターゲット言語コピー領域が開いたら、先に進んで翻訳ジョブを開始できます。


## 翻訳ジョブを開始 {#id225IK030OE8}

翻訳ジョブを開始するには、次の手順を実行します。

1. 内 **プロジェクト** コンソールで、ローカライゼーション用に作成したプロジェクトフォルダーに移動します。

1. ローカリゼーションプロジェクトをクリックして、詳細ページを開きます。

1. 「 **翻訳ジョブ** タイルと選択 **開始** 翻訳ワークフローを開始するためのリストから。

   >[!NOTE]
   >
   > 人間翻訳サービスを使用している場合は、翻訳用にコンテンツを書き出す必要があります。 翻訳されたコンテンツを取得したら、そのコンテンツを翻訳プロジェクトに読み込む必要があります。

1. 翻訳ジョブのステータスを表示するには、「**翻訳ジョブ**」タイルの一番下にある省略記号をクリックします。


翻訳が完了すると、翻訳ジョブのステータスが「 *レビュー準備完了*. 翻訳プロセスを完了するには、プロジェクトコンソールの「翻訳ジョブ」タイルから翻訳済みのコピーとアセットのメタデータを承認する必要があります。

>[!NOTE]
>
> 翻訳ジョブで 1 つ以上のトピックの翻訳を拒否した場合、 **処理中** すべての却下されたトピックの翻訳ステータスは、元のステータスに戻ります。 参照元のトピックのステータスは、最新の翻訳状態に応じてチェックされ、元に戻されます。 また、宛先プロジェクトで作成された翻訳ファイルは、翻訳が拒否されても削除されません。

**親トピック：**[&#x200B;コンテンツを翻訳](translation.md)
