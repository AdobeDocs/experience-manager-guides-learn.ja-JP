---
title: ファイルとフォルダーの管理
description: ファイルとフォルダーを管理する方法を説明します
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '2502'
ht-degree: 0%

---


# ファイルとフォルダーの管理 {#id2116G0L08XA}

この節では、AEMガイドで、ファイルのコピー、貼り付け、ドラッグ&amp;ドロップ、削除など、基本的なファイル操作をどのように処理するかを説明します。 次のシナリオが考えられます。

## ファイルのコピーと貼り付け

**ファイルに人間が読み取り可能なファイル名が含まれている場合**

- *同じ名前のファイルが保存先フォルダーに存在しない場合*:ファイルの新しいコピーが作成され、UUID も割り当てられます。 ここでは、ファイル名は元のファイル名と同じです。
- *同じ名前のファイルが既に保存先フォルダーに存在する場合*:ファイルの新しいコピーがサフィックス付きで作成されます（例： filename0.extension\）。 また、UUID は新しく作成されたファイルにも割り当てられます。


**ファイル名が UUID パターンに基づいている場合**

- *同じ名前のファイルが保存先フォルダーに存在しない場合*:ファイルの新しいコピーが作成され、新しい UUID も新しい場所に割り当てられます。 ここでは、ファイル名は UUID と同じです。
- *同じ名前のファイルが既に保存先フォルダーに存在する場合*:ファイルの新しいコピーが作成され、新しい UUID も割り当てられます。 ファイル名は UUID と同じです。


## フォルダーのコピーと貼り付け

**同じ場所にフォルダーをコピーして貼り付けます。**

- *フォルダーには、人間が読み取り可能なファイル名を持つファイルが含まれています*:フォルダーの新しいコピーがサフィックス付きで作成されます（foldername0 など）。 新しい UUID もフォルダー内のファイルに割り当てられます。 ただし、ファイル名に変更はありません。

- *フォルダーには、UUID パターンに基づくファイル名が付いたファイルが含まれています*:フォルダーの新しいコピーがサフィックス付きで作成されます（foldername0 など）。 また、新しい UUID は、新しいフォルダー内のすべてのファイルにも割り当てられます。 ファイル名も変更されます。ファイル名は新しい UUID と同じです。


**別の場所にフォルダーをコピーして貼り付けます**

- *フォルダーには、人間が読み取り可能なファイル名を持つファイルが含まれています*:フォルダーの新しいコピーが作成され、新しい UUID もフォルダー内の新しい場所にあるすべてのファイルに割り当てられます。 この場合、フォルダやファイル名は変更されません。

- *フォルダーには、UUID パターンに基づくファイル名が付いたファイルが含まれています*:元のフォルダーと同じ名前で、新しいフォルダーのコピーが作成されます。 また、新しい UUID は、新しいフォルダー内のすべてのファイルにも割り当てられます。 ファイル名も変更されます。ファイル名は新しい UUID と同じです。


## ファイルのドラッグ&amp;ドロップ

**人間が読み取り可能なファイル名でドラッグ&amp;ドロップ**

- *同じ場所にドラッグ&amp;ドロップ*:次のオプションが用意されています。 **既存のファイルを上書き**, **両方のファイルを保持**、および既存の作業用コピーのバージョンを作成するオプション。

   ![](images/uuid-human-readable-drag-drop-same-location.PNG){width="650" align="center"}

   次を選択した場合、 **既存のファイルを上書き** 」オプションを選択すると、アップロード中のファイルが、元の場所にある既存のファイルの現在の作業バージョンに置き換えられます。 UUID は作成も変更もされません。

   次を選択した場合、 **両方のファイルを保持** オプションを指定すると、ファイルの新しいコピーがサフィックス付きで作成されます（例： filename0.extension\）。 新しくコピーされたファイルにも、新しい UUID が割り当てられます。

   「既存のファイルを上書き」オプションを選択した場合、既存の作業用コピーからバージョンを作成するオプションを選択すると、ドキュメントの作業用コピーから新しいバージョンも作成されます。

   >[!NOTE]
   >
   > **アップロードしたファイルの新しいバージョンを作成** 機能は管理者が有効にする必要があります。 この機能を有効にすると、アップロードされたファイルの新しいバージョンが作成されます。 このオプションの選択を解除すると、アップロードされたファイルのバージョンは作成されません。 詳しくは、 *アップロードしたファイルの新しいバージョンを作成* の節を参照してください。Adobe Experience Managerガイドのインストールと設定as a Cloud Service。

   別のユーザーが既にファイルをチェックアウトして編集をチェックアウトしていて、既存のファイルをアップロードして上書きしようとすると、失敗し、エラーが表示されます。

   >[!NOTE]
   >
   >この **チェックアウトしたファイルをアップロード時に上書き** の機能は管理者が無効にする必要があります。 この機能を有効にした場合、チェックアウトしたファイルを上書きできます。 この機能が有効になっていない場合、チェックアウトされたファイルは上書きされません。 詳しくは、 *チェックアウトしたファイルをアップロード時に上書き* の節を参照してください。Adobe Experience Managerガイドのインストールと設定as a Cloud Service。


- *ファイルを別の場所にドラッグ&amp;ドロップ*:ファイルの新しいコピーが作成され、新しい UUID も新しい場所に割り当てられます。 ここでは、ファイル名は元のファイル名と同じです。


**UUID パターンに基づくファイル名のドラッグ&amp;ドロップ**

*ファイルを同じ場所にドラッグ&amp;ドロップ*:次のオプションが用意されています。 **既存のファイルを上書き** 既存の作業用コピーのバージョンを作成するオプションと共に使用します。

![](images/uuid-drag-drop-same-location.PNG){width="650" align="center"}

ファイルが上書きされた場合、ファイル名または UUID は変更されません。

次を選択した場合、 **既存の作業コピーのバージョンを作成** 」オプションを選択すると、ドキュメントの作業用コピーから新しいバージョンが作成されます。新しいファイルがアップロードされ、新しいバージョンのファイルも作成され、ドキュメントの作業用コピーとして作成されます。

**アップロードしたファイルの新しいバージョンを作成** 機能は管理者が有効にする必要があります。 この機能を有効にすると、アップロードされたファイルの新しいバージョンが作成されます。 このオプションの選択を解除すると、アップロードされたファイルのバージョンは作成されません。 詳しくは、 *アップロードしたファイルの新しいバージョンを作成* の節を参照してください。Adobe Experience Managerガイドのインストールと設定as a Cloud Service。


*ファイルを別の場所にドラッグ&amp;ドロップ*:次のオプションが用意されています。 **既存のファイルを上書き**, **ファイルを新しい場所に移動**、および既存の作業用コピーのバージョンを作成するオプション。

![](images/uuid-drag-drop-different-location.PNG){width="650" align="center"}

次を選択した場合、 **既存のファイルを上書き** 」オプションを選択すると、アップロード中のファイルが、元の場所にある既存のファイルに置き換えられます。 UUID は作成も変更もされません。

次を選択した場合、 **ファイルを新しい場所に移動** 」オプションを選択した場合、既存のファイルは現在の場所に移動され、その後、アップロードされるファイルで上書きされます。 ファイルを新しい場所に移動しても、ファイルからまたはファイルへの既存の参照は壊れません。

ファイルを置き換えるか移動するときに、既存のコピーからバージョンを作成するオプションを選択した場合、ドキュメントの作業用コピーから新しいバージョンが作成されます。新しいファイルは、既存の場所で置き換えられるか、新しい場所に移動されます。


## ファイルを一括で移動

AEMガイドには、大量のファイルを含むフォルダーを別の場所に移動する際に役立つ一括移動ツールが付属しています。 このツールを使用すると、1 つ以上のフォルダー内のファイルをAEMリポジトリ内の別のフォルダーに簡単に移動できます。 このツールの主な特徴の 1 つは、大量のファイルを移動するだけでなく、移動中のファイルへの参照とファイルからの参照も維持する点です。 オーサリングやパブリッシュのタスクを妨げることなく、一括で移動できるファイル数を調整できます。

>[!NOTE]
>
> 一括移動ツールは、フォルダーレベルでのみ機能します。 個々のトピックまたはマップファイルを移動する場合は、AEM Assets UI の通常の移動ツールを使用します。

一括移動ツールで提供される機能の一部を次に示します。

- 各バッチで処理するファイル数を調整できます。 この場合、システムが簡単に処理できる最適な数に達する前に、いくつかのテストを実行する必要が生じる場合があります。
- オーサリングサービスと公開サービスは、移動操作を中断することなくスムーズに実行されます。
- 後続の\(running of) バッチプロセスの間の時間間隔を完全に制御できる。 この時間間隔を指定すると、次のファイルバッチを開始する前に後処理操作が完了します。

- 同じ名前のフォルダーの自動処理。 この機能により、同じ名前のフォルダが移動されても、そのフォルダが上書きされることはありません。

- 移動するファイルとの参照の自動処理。


バッチ処理を実行する前に、次の点を考慮する必要があります。

- 現在レビュー中のトピックを移動する場合は、移動する前に、そのトピックのレビュープロセスをすべて閉じる必要があります。 レビュータスクを閉じないと、レビュープロセスが中断されます。
- 一括移動操作は、いつでもシステム上で 1 回だけ実行する必要があります。 これにより、移動するトピックへの参照およびトピックからの参照を適切に処理できます。


ファイルを一括で移動するには、次の手順を実行します。

1. 上部の「 Adobe Experience Manager 」リンクをクリックし、「 」を選択します。 **ツール**.
1. 選択 **ガイド** を選択します。
1. をクリックします。 **一括移動ツール** タイル。

   一括移動ツールページが表示されます。

   ![](images/bulk-move-tool_cs.PNG){width="550" align="center"}

1. 一括移動ツールページで次の詳細を指定します。

   - **重複ファイルにサフィックスを追加**:同じ名前のフォルダを移動する場合は、このオプションを選択する必要があります。 例えば、上のスクリーンショットでは、 **ソースパス** 移動するフォルダの名前が含まれます。 topic という名前のフォルダーは、test-A と test-B の 2 つの異なる場所に存在します。このオプションを選択すると、フォルダーは正常に移動します。 最初に移動したフォルダーの名前は topic になり、2 番目のフォルダーの名前は topic0 になります。 移動操作では、同じ名前のフォルダに連続系列\（0、1、2 など）のサフィックスが追加されます。

      このオプションを選択せずに同じ名前のフォルダを移動する場合、この操作はメッセージとともに中止されます。

   - **ソースパス\(s\)**:移動するフォルダの場所を指定します。 通常は、ブラウザーのアドレスバーからソースの場所をコピーして貼り付ける必要があります。 複数のフォルダーの場所を指定するには、 **追加** 」ボタンをクリックします。

   - **宛先のパス**:ソースフォルダを移動する場所を指定します。

1. クリック **一括移動**.

   ソースから宛先へのファイルの移動が開始されます。 プロセスが完了すると、ページの下部に移動プロセスの概要が表示されます。

   ![](images/bulk-move-summary.PNG){width="650" align="center"}


## DITA コンテンツを検索

デフォルトでは、AEMは DITA コンテンツを認識しないので、リポジトリ内の DITA コンテンツを検索するメカニズムは提供されません。 AEMガイドでは、AEMの上にレイヤーが追加され、AEMが DITA コンテンツを理解し、処理できるようになります。 AEMガイドの DITA コンテンツの検索機能を使用すると、AEMリポジトリ内で DITA コンテンツを検索できます。

>[!NOTE]
>
>システム管理者が **DITA 要素** 検索コンポーネントを使用して、AEM Assets UI の機能を使用できます。 詳しくは、 *Assets UI での DITA 要素検索コンポーネントの追加* の「 Adobe Experience Manager Guides のインストールと設定」のas a Cloud Service。

検索機能を使用して、次の操作を実行できます。

- 要素の値に基づいて DITA コンテンツを検索する。例： `author`= xml
- 属性値に基づいて DITA コンテンツを検索する。例： `@platform`= windows
- DITA 要素と属性値の組み合わせを使用します。例： `author`= xml `AND` `@platform`= windows

AEMリポジトリ内の DITA コンテンツを検索するには、次の手順を実行します。

1. Assets UI を開きます。

1. 左側のレールで、「 」を選択します。 **フィルター**.

   ![](images/left-rail-filter.png){width="450" align="center"}

   コンテンツのフィルターオプションが左側のパネルに表示されます。 また、DITA コンテンツのフィルタリングに使用する DITA 要素のフィルタリングオプションもあります。

   ![](images/dita-element-search.png){width="450" align="center"}

1. *\（オプション\）* 内 **検索ディレクトリを選択** フィールドで、検索する場所を参照します。

1. 内 **DITA 要素** フィルター、 **エレメント名**, **属性**、および検索する値。 例えば、 `author` 次の要素 `@type` creator 次のスクリーンショットに示すように、情報を指定する必要があります。

   ![](images/search-params.png){width="650" align="center"}

   指定した **DITA 要素** フィルターが検索バーの上部に表示されます。 検索条件に一致するファイルが **検索結果** 領域

   検索条件を指定する際は、次の点を考慮してください。

   - 完全に一致するフレーズを検索するには、「値」フィールドにフレーズを引用符で囲んで入力します `"`フレーズ検索`"`.
   - 最大 3 つの DITA 要素検索条件を追加できます。
   - 複数の検索条件を指定する場合、すべての検索条件が AND 論理を使用して結合されます。
   - 検索条件にワイルドカード文字は使用できません。 例えば、Windows の値を持つプラットフォーム\(attribute\) を検索する場合、\*form や Windo?s を指定することはできません。

**検索でのチェックアウトステータスフィルター**

DITA 要素フィルターに加えて、AEMガイドでは、チェックアウトステータスに基づいてコンテンツを検索することもできます。 これは、現在自分がチェックアウトしているファイルをすばやく除外し、再度チェックインする場合に便利です。

チェックアウトステータスに基づいてファイルを検索するには、次の手順を実行します。

1. Assets UI を開きます。

1. クリック **フィルター** をクリックします。
1. 検索バーに検索キーワードを入力します。
1. 左側のパネルから必要なフィルターを適用します。

   例えば、 **チェックアウトステータス** チェックアウト済みまたはチェックイン済みのトピックを表示するには、filter を使用します。 このリストをさらに絞り込むには、「チェックアウト者」(Checked Out By) リストからユーザーまたはグループを選択します。

   検索結果が表示されます。


## ファイルを削除

AEMリポジトリからのファイルの削除は制限付きの機能で、システム管理者が制御します。 設定に基づいて、次の場合にファイルの削除が制限される可能性があります。

- チェックアウト済み
- 受信または送信の参照がある

また、ファイルを削除する権限を持つ特定のユーザーグループに属している場合にのみ、ファイルを削除できます。

>[!NOTE]
>
> ファイル管理の設定の詳細については、 *チェックアウトしたファイルの削除を禁止する* および *参照ファイルを削除しない* 「 Adobe Experience Managerガイドのインストールと設定」のas a Cloud Service。

管理者がすべてのユーザーに対してファイルの削除権限を付与している場合、参照を含むファイルを削除すると、次のメッセージが表示されます。

![](images/allow_unsafe_delete-force-delete.PNG){width="650" align="center"}

このシナリオでは、ファイルからの受信参照または送信参照を削除せずに、強制的にファイルを削除できます。

削除権限が特定のユーザーグループに与えられている場合は、そのグループに属するユーザーに対しても上記のメッセージが表示されます。 ただし、他のユーザーの場合は、次のメッセージが表示されます。

![](images/allow_unsafe_delete_for_delete_assets_group.PNG){width="650" align="center"}

このシナリオでは、すべての受信参照と送信参照が削除されるまで、ユーザーはファイルを削除できません。

## メディアファイルの操作

画像やビデオなどのメディアファイルは、コンテンツに不可欠な要素です。 コンテンツをアップロードおよび管理する際に、メディアファイルを扱うこともできます。

メディアファイルに変更が加えられている場合は、 **バージョン履歴**&#x200B;メディアファイルの異なるバージョンでの変更を調べるには、次の手順を実行します。

1. でファイルにアクセスします。 **Assets UI**.
1. バージョン履歴を表示するファイルを選択します。
1. 左側のレールで、 **バージョン履歴** をクリックし、バージョンを選択します。
1. また、「バージョン履歴」の下に、様々なバージョンのサムネールを表示できます。

   ![](images/media-version-history-icon.png){width="800" align="center"}

1. 表示されたバージョンから、ベースバージョンとして使用するバージョンを選択し、 **バージョンをプレビュー**. 選択したバージョンのプレビューが、バージョンのプレビューウィンドウに表示されます。

   ![](images/media-version-preview.png){width="650" align="center"}


**親トピック：**[&#x200B;コンテンツを管理](authoring.md)
