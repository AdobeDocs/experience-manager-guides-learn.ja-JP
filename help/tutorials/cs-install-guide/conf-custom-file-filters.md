---
title: ファイル参照ダイアログのフィルターを設定する
description: ファイル参照ダイアログのフィルターを設定する方法を説明します
source-git-commit: 6051181e243cf71919901093c1b5590f21832545
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---


# ファイル参照ダイアログのフィルターを設定する {#id20CIL7009GN}

Web エディターで作業を行う際は、ファイル参照ダイアログを使用して、画像、参照、キー参照などの要素を挿入する必要があります。 デフォルトのファイル参照ダイアログには、ファイルのフィルタリングオプションはありません。 必要なファイルに簡単かつ迅速にアクセスできる独自のフィルターを追加できます。

次の手順を実行して、カスタムのファイルフィルタリングオプションをファイル参照ダイアログに追加します。

1. UI 設定ファイルをダウンロードするには、管理者としてAdobe Experience Managerにログインします。

1. 上部の「 Adobe Experience Manager 」リンクをクリックし、「 」を選択します。 **ツール**.
1. 選択 **ガイド** ツールのリストから、 **フォルダープロファイル**.
1. をクリックします。 **グローバルプロファイル** タイル。
1. を選択します。 **XML エディター設定** タブをクリックし、 **編集** 上部のアイコン
1. 次をクリック： **ダウンロード** アイコンを使用して、ui\_config.json ファイルをローカルシステムにダウンロードします。 その後、ファイルに変更を加えてから、同じファイルをアップロードできます。
1. 内 `ui_config.json` ファイルを開き、追加するフィルターの定義を追加します。

   次のコードスニペットに、DITA ファイルと画像ファイルの 2 つのフィルタリングオプションを追加する方法を示します。

   ```
   "browseFilters": [
                       {
                       "title": "DITA Files",
                       "property": "jcr:content/metadata/dita_class",
                       "operation": "exists"
                       },
                       {
                       "title": "Image Files",
                       "property": "jcr:content/metadata/dc:format",
                       "value": [
                       "image/jpeg",
                       "image/gif",
                       "image/png"
                       ]
                       }
                       ]
   ```

   上記のコードスニペットでは、最初のフィルターは DITA ファイル用です。 フィルター定義では次のパラメーターを取ります。

   title :フィルターの表示名。 このタイトルは、ファイル参照ダイアログでフィルタリングオプションとして表示されます。

   プロパティ：ファイルのメタデータで一致させるプロパティ。 例えば、 `dita_class` プロパティ内のメタデータの場合、プロパティフィルターは「 `jcr:content/metadata/dita_class`」を値として使用します。

   操作：&quot; `exists`」と指定し、プロパティパラメーターで指定された値の存在を照合します。

   2 つ目のフィルターは、画像ファイル用です。 パラメーターは、 `value` パラメーター。 この `value` パラメーターは、画像タイプの配列を値として取ります。 値パラメータで指定されたすべてのファイルタイプが検索され、ファイル参照ダイアログに表示されます。その他のファイルタイプは無視されます。

1. 保存する *ui\_config.json* ファイルをアップロードし、同じファイルをアップロードします。 次に、Web エディタを再読み込みします。

   ファイルの参照ダイアログを起動すると、ui\_config.json ファイルで設定したフィルターオプションが表示されます。

   ![](assets/file-browse-custom-filters.png)


**親トピック：**[ Web エディタのカスタマイズ](conf-web-editor.md)
