---
title: バージョン管理
description: バージョンの管理方法の詳細
source-git-commit: 4f15166b1b250578f07e223b0260aacf402224be
workflow-type: tm+mt
source-wordcount: '1498'
ht-degree: 1%

---


# バージョン管理 {#id181GB000XY4}

バージョン管理は、あらゆるコンテンツ管理システムの重要な側面です。 特定の時点でのデジタルアセットのスナップショットを作成できます。 デジタルアセットのバージョンを用意したら、必要なバージョンのアセットを復元して更新できます。 通常、任意のアセットのバージョンを作成する場合は、必要なアセットをチェックアウトしてチェックインします。

管理者は、チェックアウトせずにユーザーがファイルを編集できないようにするルールを適用できます。 同様に、チェックアウトしたすべてのファイルをチェックインして、データの損失を防ぐことができます。

複数使用の環境では、ユーザーがシステムからファイルを削除しないようにすることも重要です。 この要件は、他のユーザーがチェックアウトしたファイルに対しては、より重要です。 ユーザーがチェックアウトしたファイルをシステムから誤って削除するのを防ぐため、AEMガイドでは、使用できる設定を提供しています。 チェックアウトしたファイルに加えて、参照を含むファイルや他のファイルから参照されるファイルの削除を制御することもできます。

## アップロードしたファイルの新しいバージョンを作成

>[!NOTE]
>
> この設定は、ファイルのアップロード時にのみ適用できます。

を有効にするには、以下を実行します。 **アップロードしたファイルの新しいバージョンを作成** オプションを選択するには、次の手順を実行します。

1. に示す手順を使用します。 [設定の上書き](download-install-additional-config-override.md#) 設定ファイルを作成します。
1. 設定ファイルで、次の\(property\) 詳細を指定して **アップロードしたファイルの新しいバージョンを作成** オプション：


   | PID | プロパティキー | プロパティの値 |
   |---|------------|--------------|
   | `com.adobe.fmdita.confi g.ConfigManager` | `create.ver.new.content` | ブール値\(true/false\)。<br> **デフォルト値**: `true` |

>[!NOTE]
>
> このオプションを選択すると、新しいバージョン管理メカニズムが実行され、以降のアップロードで使用されるデフォルトのアップロード動作を上書きして、アップロードされたファイルの内容を新しいバージョンとして保存します。 このオプションの選択を解除した場合、AEM Guides はAEMのデフォルトのバージョン管理メカニズムを使用します。

## チェックアウトしたファイルの編集を許可する設定を構成します

AEM Guides Web Editor を使用すると、DITA トピックを作成および更新できます。 Web エディターを設定して、リポジトリからチェックアウトされたドキュメントのみを編集できるようにすることができます。 これにより、他のライターが誤って別のライターが編集用に開いたトピックを上書きすることを防ぐことができます。 トピックを開いて編集した後、作成者はファイルを閉じる際にファイルをチェックインできます。

もう 1 つの重要なルールは、チェックアウトされたファイルを確実にシステムにチェックインすることです。 これにより、ユーザーがチェックインせずに誤ってファイルを閉じるのを防ぎます。

に示す手順を使用します。 [設定の上書き](download-install-additional-config-override.md#) 設定ファイルを作成します。 設定ファイルで、チェックアウトしたファイルの編集を設定する次の\（プロパティ\）の詳細を指定します。

| PID | プロパティキー | プロパティの値 |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.autocheckout` | ブール値\(true/false\)。<br> **デフォルト値**: `false` |

また、チェックアウトしたファイルを保存またはリポジトリにチェックインせずに閉じた場合に警告メッセージを表示するようにを設定することもできます。

| PID | プロパティキー | プロパティの値 |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.checkin` | ブール値\(true/false\)。<br> **デフォルト値**: `false` |

>[!NOTE]
>
> この機能のオン/オフに関係なく、トピックプレビューでは、常に「チェックアウト」と「チェックイン」の各オプションを使用できます。

## アップロード時にチェックアウトしたファイルを上書き

>[!NOTE]
>
> *この設定は、Assets UI からファイルを作成する場合にのみ適用され、WebDAV ツールを使用してファイルをアップロードする場合には適用されません。*

ユーザーがチェックアウトしたファイルや他のユーザーがアップロード時にファイルを上書きできるようにするには、次の手順を実行します。

1. に示す手順を使用します。 [設定の上書き](download-install-additional-config-override.md#) 設定ファイルを作成します。
1. 設定ファイルで、次の\(property\) 詳細を指定して **チェックアウトしたファイルをアップロード時に上書き** オプション：


| PID | プロパティキー | プロパティの値 |
|---|------------|--------------|
| `com.adobe.fmdita.confi g.ConfigManager` | `overwrite.checkout.onupload` | ブール値\(true/false\)。<br> **デフォルト値**: `false` |

>[!NOTE]
>
> デフォルトでは、このオプションはオフになっています。 このオプションを選択すると、チェックアウトされたファイルを上書きできます。 このオプションが選択されていない場合、ファイルがチェックアウトされた場合や他のユーザーによって上書きされることはありません。

## チェックアウトしたファイルの削除を禁止する

に示す手順を使用します。 [設定の上書き](download-install-additional-config-override.md#) 設定ファイルを作成します。 設定ファイルで、チェックアウトされたファイルをユーザーが誤って削除するのを防ぐために、次の\（プロパティ\）詳細を指定します。

| PID | プロパティキー | プロパティの値 |
|---|------------|--------------|
| `com.adobe.fmdita.xmleditor.config.XmlEditorConfig` | `xmleditor.preventcheckedoutcontentdeletion` | ブール値\(true/false\)。 <br> **デフォルト値**: `true` |

## 参照ファイルを削除しない

管理者は、AEMリポジトリからファイルを削除できるユーザーを制御できます。 特に、ファイルに参照が含まれている場合や、他のファイルによって参照されている場合は、そのようなファイルを削除できるユーザーを定義できます。

この設定を使用すると、すべてのユーザーに対してファイルの削除を許可または禁止したり、特定のユーザーグループに対してのみファイルの削除を許可したりできます。 ファイルの削除が許可されている場合は、次の手順に従います。

- 参照ファイルと参照ファイルをすべて含むフォルダを削除する場合、すべてのファイルが削除されます。 プロセスは、参照を含まないすべてのファイルを最初に削除し、その後に参照を含むまたは参照されるファイルを削除します。

- フォルダを削除し、そのフォルダ内のファイルがそのフォルダの外のファイルによって参照されている場合は、参照を削除するよう求められた後で、ファイルを削除します。


に示す手順を使用します。 [設定の上書き](download-install-additional-config-override.md#) 設定ファイルを作成します。 設定ファイルで、参照を含むファイル、または他のファイルから参照されるファイルを削除できるユーザーを定義する次の\（プロパティ\）の詳細を指定します。

| PID | プロパティキー | プロパティの値 |
|---|------------|--------------|
| `com.adobe.fmdita.config.ConfigManager` | `block.unsafe.delete` | 次の値を指定できます。 <br> - allow\_unsafe\_delete\_for\_all <br> - allow\_unsafe\_delete\_for\_delete\_assets\_group <br> - block\_unsafe\_delete\_for\_all <br> **デフォルト値**: `allow_unsafe_delete_for_delete_assets_group` <br> これらの定数の詳細は以下のとおりです。 |

削除のアクセス権を付与するユーザーに応じて、次のいずれかの定数を指定します。

- allow\_unsafe\_delete\_for\_all:すべてのユーザーに、ファイルを削除する権限を付与します。 この場合、ファイルに参照が含まれているか、他のファイルが参照している場合は、そのようなファイルを強制的に削除することもできます。 ファイルを削除する前に、参照を示すプロンプトが表示され、削除操作をキャンセルし、参照を削除してから、最後にファイルを削除できます。 または、参照を削除せずに強制的にファイルを削除することもできます。

  ![](assets/allow_unsafe_delete-force-delete.PNG)

- allow\_unsafe\_delete\_for\_delete\_assets\_group:管理者または *delete-assets* グループはファイルを削除できます。 参照を持つファイルを他のユーザーが削除しようとした場合、すべての参照が削除されるまで、そのようなファイルの削除は許可されません。 権限を持たないユーザーがファイルの削除を試みると、次のスクリーンショットが表示されます。

  ![](assets/allow_unsafe_delete_for_delete_assets_group.PNG)

- block\_unsafe\_delete\_for\_all:ファイルへの参照とファイルからの参照が削除されるまで、すべてのユーザー（管理者を含む）に対してファイルの削除を許可しません。


## DITA ファイルの古いバージョンのパージ

コンテンツを更新し、新しいバージョンを作成すると、以前のバージョンの DITA ファイルがリポジトリに保持されます。 多くのバージョンが、ある期間に DITA ファイル用に作成され、また、複数のバージョンをまとめてリポジトリ内の大量の領域を占有する場合があります。 AEMガイドを使用すると、リポジトリから削除する必要がある古いバージョンを設定できます。

管理者権限を持っている場合は、指定された URL を使用してこのユーティリティにアクセスできます。

`<server folder path> /libs/fmdita/clientlibs/xmleditor_version_purge/page.html`

指定した条件のいずれかを満たす DITA ファイルのバージョンは維持され、パージされません。

- ファイルの最初のバージョンです
- ベースラインに含まれる
- 任意の翻訳またはレビューワークフローに含まれる
- ラベルが適用されている
- 定義された年齢またはバージョンの条件を満たす

以前のバージョンをパージするには、次の手順を実行します。

1. パージするファイルに関する次の詳細を入力します。

   ![](assets/preview-purge-report.png)

1. 
   - **最新バージョンから保持するバージョンの数**:保持し、パージしないバージョンの数を入力します。 例えば、5 と入力すると、最近の 5 つのバージョンが保持され、それより前のバージョンは、他のパージ条件が満たされた場合にパージされる資格があります。
- **期間内に作成されたバージョンを保持\（日数）**:バージョンの最大期間を日数で入力します。 指定された日数より古いバージョンは、他のパージ条件が満たされた場合にパージされる資格があります。 例えば、100 と入力した場合、他のパージ条件が満たされた場合に、100 日前までに作成されたすべてのバージョンがパージ対象として認定されます。
- **パス**:ファイルをパージするファイルまたはフォルダのパスを選択します。

  >[!NOTE]
  >
  > DITA ファイルのみをパージできます。

1. クリック **パージレポートのプレビュー**.

   >[!NOTE]
   >
   > 一度に 1 つのパージタスクのみ存在します。 処理中のバージョンのパージ操作は開始できません。

   バージョンパージレポートが生成されます。

1. バージョンのパージレポートをダウンロードし、パージされるファイルとバージョンを確認します。
1. 次の項目を選択できます。 **パージをキャンセル** または **パージを開始**.

   ![](assets/download-purge-report.png)

   パージステータスが表示されます。

   クリック **バージョンのパージレポートをダウンロード** ：パージされたバージョンを表示します。 このレポートは、すべてのバージョンのパージステータスと、特定のバージョンが保持された理由、またはパージされた理由を表示します。


>[!NOTE]
>
> レポートは次の場所にダウンロードされます。 `/var/dxml/versionpurge`
