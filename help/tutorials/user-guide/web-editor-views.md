---
title: Web エディターの表示
description: Web エディターの表示方法を学ぶ
source-git-commit: fa6e9f8b32d191f5b6f7136724d2145d81317767
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 0%

---


# Web エディターの表示 {#id204GK0D0V5Z}

AEM Guides の Web エディタは、次の 3 つの異なるモードまたはビューでのドキュメントの表示をサポートします。

## オーサー

これは、Web エディタの一般的な「表示される内容」とは、Web エディタの「(WYSISYG)」ビューです。 通常のリッチテキストエディターと同様にトピックを編集できます。 作成者ビューでは、ドキュメントのリビジョンの保存、コンテンツの検索と置換、要素の挿入、ハイパーリンクの挿入、コンテンツ参照の挿入などのオプションを使用できます。

>[!NOTE]
>
> コンテンツ参照を使用すると、参照元のコンテンツもオーサー表示で青色で表示されます。 参照されるコンテンツは編集できません。

## ソース

ソースビューには、トピックを構成する基になる XML が表示されます。 XML を直接操作する場合は、ソースビューを使用する必要があります。 このビューで通常のテキスト編集を行う以外に、スマートカタログを使用して要素や属性を追加したり、テキスト、要素、または属性を検索して置き換えたりすることもできます。

- スマートカタログを呼び出すには、新しい要素を挿入する要素タグの最後にカーソルを置き、「&lt;」と入力します。 エディターには、その場所に挿入できるすべての有効な XML 要素のリストが表示されます。 矢印キーを使用して挿入する要素を選択し、Enter キーを押します。 閉じ角括弧&quot;\> を入力すると、要素の終了タグが自動的に追加されます。

   ![](images/smart-catalog-elements.png){width="400" align="left"}

- また、ソースビューから要素を簡単に変更することもできます。 例えば、 `p` 要素から `note`、次に、終了 `p` タグは自動的に `/note`. 要素を正しくない要素で置き換えた場合は、検証エラーが直ちに表示されます。

- 要素に属性を追加する場合は、要素タグ内にカーソルを置き、スペースバーを押します。 その要素に対して有効な属性のリストがスマートカタログに表示されます。 矢印キーを使用して目的の要素を選択し、Enter キーを押して要素を挿入します。 属性の値を指定するには、等号 (=\) を入力します。エディターは自動的に開始引用符と終了引用符「」を入力し、ここで属性の値を指定します。

   ![](images/smart-catalog-attribute.png){width="350" align="left"}

- ソースビューには、XML コードを表示可能で読みやすい形式に整理し直す自動インデントオプションがあります。 また、任意のテキストを選択して、オーサーからソースに切り替えた場合、またはソースからオーサーに切り替えた場合、選択したテキストも他のビューでハイライト表示されます。
- ソースビューのもう 1 つの強力な機能は、ドキュメント内の XML 検証です。 無効な XML を含むドキュメントを開くと、そのドキュメントは、無効な XML に関する情報と共にソースビューで開かれます。 例えば、次のスクリーンショットでは、誤った XML に関する正確な情報が「解析エラー」ポップアップに表示されます。

   ![](images/invalid-topic-xml.png){width="650" align="left"}

   上のスクリーンショットでは、誤った XML を含む行を示すために、クロスハイライトが使用されます。

- 「検索と置換」機能を使用すると、ソースビュー内の任意のテキスト、要素または属性を検索できます。
詳しくは、 **検索と置換** 機能の説明 [メインツールバー](web-editor-features.md#id#id2051EA0G05Z) 」セクションに入力します。

- ソースビューには、ドキュメントをすばやく移動して操作するのに役立つ多くのショートカットが用意されています。 次の表に、サポートされるアクションとそのショートカットキーを示します。

   | これをおこなうには | このショートカットを使用 |
   |----------|-----------------|
   | 複数カーソルの追加 | **Ctrl**+左クリック |
   | 複数の連続しないテキスト選択 | **Ctrl**+左クリックでテキストをドラッグ&amp;選択 |
   | 行間のテキストを選択 | **Alt**+左クリックでテキストをドラッグ&amp;選択 |
   | 複数選択を取り消すか、全画面表示モードを終了します | **Esc** |
   | オートコンプリートを表示 | **Ctrl**+**スペース** |
   | 現在のタグの開始タグまたは終了タグに移動します | **Ctrl**+**J** |
   | 現在のタグとそのコンテンツを展開または折りたたみます | **Ctrl**+**Q** |
   | 現在の要素とそのコンテンツを選択 | **Ctrl**+**L** |
   | 現在の要素をアウトデント | **Shift**+**タブ** |
   | 現在の要素とそのコンテンツを削除 | **Shift**+**Ctrl**+**K** |
   | カーソルを 1 単語左に移動 | **Alt**+**左向き矢印** |
   | カーソルを 1 単語右に移動します。 | **Alt**+**右矢印** |
   | カーソル位置を変更せずに 1 行上にスクロール | **Ctrl**+**上向き矢印** |
   | カーソル位置を変更せずに 1 行下にスクロール | **Ctrl**+**下矢印** |
   | 全画面を切り替え | **F11** |
   | 現在の要素の後に新しい行を挿入します | **Ctrl**+**入力** |
   | 現在の要素の前に新しい行を挿入します | **Shift**+**Ctrl**+**入力** |
   | 現在の単語の次の出現箇所を検索して選択 | **Ctrl**+**D** |
   | 現在の要素とそのコンテンツを 1 つ上に移動します。 | **Shift**+**Ctrl**+**上向き矢印** |
   | 現在の要素とそのコンテンツを 1 つ下に移動します。 | **Shift**+**Ctrl**+**下矢印** |
   | 現在の要素をコメントタグで囲む | **Ctrl**+**/** |
   | 現在の要素とそのコンテンツを複製 | **Shift**+**Ctrl**+**D** |
   | カーソルの後のテキストを削除します。 カーソルが開始要素の前にある場合、要素全体が削除されます。 | **Ctrl**+**K**+**K** |
   | 現在の行のカーソルの左側にあるテキストを削除します。 カーソルが要素の終了タグの後にある場合、要素全体が削除されます。 | **Ctrl**+**K**+**Backspace** |
   | 現在のテキストを大文字に変換します | **Ctrl**+**K**+**U** |
   | 現在のテキストを小文字に変換します | **Ctrl**+**K**+**L** |
   | 現在の要素をエディターの中心までスクロールします。 | **Ctrl**+**K**+**C** |
   | 現在の位置の上にカーソルを追加 | **Ctrl**+**Alt**+**上向き矢印** |
   | 現在の位置の下にカーソルを追加 | **Ctrl**+**Alt**+**下矢印** |
   | 現在の単語を再帰的に検索します\（前方向\） | **Ctrl**+**F3** |
   | 現在の単語\（逆方向\）を再帰的に検索します | **Shift**+**Ctrl**+**F3** |


## プレビュー

プレビューモードでトピックを開くと、ユーザーがブラウザーでトピックを表示したときに、そのトピックがどのように表示されるかが表示されます。 DITA マップの場合、マップのプレビューが表示され、マップ内のすべてのトピックの 1 つの複合文書が表示されます。

プレビューモードでは、次の機能を使用できます。

- [条件フィルターに基づいてコンテンツを表示](#id2114BI00VXA)
- [トラックの変更マークアップを表示](#id2114BJ00CE8)
- [トピックをPDFとしてエクスポート](#id2114BL00B5U)

### 条件フィルターに基づいてコンテンツを表示 {#id2114BI00VXA}

トピックまたはマップで条件を使用した場合、その条件はフィルターパネルに表示されます。 デフォルトでは、すべての条件が選択され、コンテンツ全体が表示されます。 条件の選択を解除すると、その条件を持つコンテンツは表示から削除されます。 条件付きコンテンツをハイライトすることもできます。

次の図は、2 つの条件を使用するトピックを示しています。 `Audience` および `Product`. 条件付きコンテンツは、黄色の背景でハイライト表示されます。

![](images/preview-filters.png){width="800" align="left"}

### トラックの変更マークアップを表示 {#id2114BJ00CE8}

ドキュメントにトラックの変更マークアップ（またはビジュアルキュー）が含まれている場合は、それらのマークアップの有無に関わらずドキュメントをプレビューすることもできます。 ドキュメントのプレビュー中、右側のパネルには「フィルター」と「追跡」オプションが表示されます。

![](images/preview-tracking_cs.png){width="400" align="left"}

三つある **トラッキング** 次の中から選択できるオプションです。

- **マークアップなし**:このビューでは、すべての挿入と削除が受け入れられ、ドキュメントの単純なビューが表示されます。 このビューでは、トラックの変更マークアップは表示されません。
- **オリジナル**:このビューでは、すべての挿入が拒否され、すべての削除が元に戻され、プレビューが表示されます。 単純に、変更の追跡モードを有効にする前に、元の形式のドキュメントを取得します。
- **マークアップを表示**:このビューでは、挿入および削除されたコンテンツのすべてのマークアップを取得します。

   次の図は、マークアップを含むマップファイルのプレビューを示しています。

   ![](images/preview-map-with-track-changes.PNG){width="800" align="left"}


### トピックをPDFとしてエクスポート {#id2114BL00B5U}

PDFは、ドキュメント開発サイクルのあらゆる段階で使用される最も一般的な出力形式の 1 つです。 AEMガイドでは、個々のトピックまたはマップファイル全体のPDFを柔軟に生成できます。 「PDFとして書き出し」機能を使用すると、作成者、投稿者、または管理者は、個々のトピックのPDF出力を簡単に生成できます。 フォルダーレベルのプロファイルで保存された DITA-OT 設定を使用して、PDFを生成します。

この機能は、次の機能をサポートしています。

- トピックの現在アクティブな作業用コピーのPDFを生成します。
- DITA-OT 変換名とコマンドライン引数を受け入れて、PDFを生成します。
- 生成された出力をローカルシステムに保存します。
- 出力を生成する前に、トピックで使用されているキーおよびコンテンツの参照を解決します。

トピックをPDFとして書き出すには、次の手順に従います。

1. トピックをプレビューモードで開きます。

1. 次をクリック： **書き出しPDF** \(![](images/export-as-pdf-icon.svg)\) アイコンをクリックします。

   [ 書き出しPDF] ダイアログが表示されます。

   ![](images/export-as-pdf-dialog.png){width="350" align="left"}

1. *\（オプション\）* DITA-OT 変換名と、使用するコマンドライン引数を指定します。

1. 「**ダウンロード**」をクリックします。

   >[!NOTE]
   >
   > ブラウザー設定でポップアップウィンドウを有効にしておく必要があります。有効にしないと、PDFはダウンロードされません。

   PDFが生成され、新しいタブで開かれます。または、ローカルシステムにPDFを保存するためのダイアログが表示されます。


**親トピック：**[ Web エディターの操作](web-editor.md)
