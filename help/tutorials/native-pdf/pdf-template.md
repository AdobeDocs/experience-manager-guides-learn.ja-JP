---
title: ネイティブPDF公開機能 |ネイティブPDF機能のカスタマイズと設定
description: ネイティブPDF機能の様々なコンポーネントをカスタマイズして設定する方法を説明します。
source-git-commit: bd62afd85ddbcf5f305b18b9a9c226a4790d383a
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# PDFテンプレート

テンプレートを使用すると、コンテンツのレイアウトと構造の一貫性が確保されます。 テンプレートは事前に定義されているので、新しいプロジェクトや更新のたびに発生する書式の問題が再び解決されるのを防ぐことができます。 テンプレートを使用すると、ページレイアウトのデザイン、スタイルコンテンツの作成、様々な設定の適用によるPDFのカスタマイズが可能です。

作成者はPDFプリセットを使用して出力を生成できますが、開発者は独自のテンプレートを作成できます。 標準で提供されているサンプルテンプレートがあります。開発者は、組織の要件に従って、さらにカスタマイズしたり複製したりできます。


## 新しいテンプレートのPDF {#create-pdf-template}

特定のページレイアウトでカスタムPDFテンプレートを作成し、スタイルシートを使用して、ページレイアウトコンポーネント（TOC、インデックス、用語集など）や DITA コンポーネント（見出し、段落、リストなど）の書式を定義できます。 新しいテンプレートを最初から作成したり、サンプルテンプレートを使用して作成したりできます。

新しいテンプレートをPDFするには、次の手順に従います。
1. Web エディターで、 **出力** タブをクリックします。
1. 左側のサイドバーを展開し、 **テンプレート**.
<img src="assets/create-pdf-template.png" alt="PDFテンプレートを作成" width="400">
1. 「**テンプレート**」パネルで、「**テンプレート**」の横にある**+**アイコンをクリックし、「**テンプレートテンプレート**」を選択します。
1. 「**新しいテンプレート**」ダイアログで、テンプレートの名前を指定します。
1. 「**完了**」をクリックします。

新しいテンプレートが作成され、 *テンプレート* パネル。

## PDFテンプレートの複製

既存のテンプレートと同じページレイアウトおよび書式を持つ新しいテンプレートを作成する場合は、コピーを作成できます。 テンプレートを複製した後は、必要に応じて、そのコンポーネントをさらにカスタマイズできます。

既存のテンプレートを複製するPDFを作成するには、次の手順に従います。
1. Web エディターで、 **出力** タブをクリックします。
1. 左側のサイドバーを展開し、 **テンプレート**.

   テンプレートパネルが開きます。
1. 複製するテンプレートの上にマウスポインターを置いて、「*オプション* アイコン ) **...** を選択します。 **複製** を選択します。

   [ 複製テンプレート ] ダイアログが開きます。\
   <img src="assets/duplicate-template.png" alt="重複PDFテンプレート" width="250">
1. テンプレートの名前を指定します。

   この **名前** フィールドに、ソーステンプレートと同じ名前のコピーが事前に入力されています。

1. 希望の名前を指定するには、事前入力された名前を削除し、名前を指定します。
1. 「**完了**」をクリックします。

   複製したテンプレートが作成され、「テンプレート」の下に追加されます。

## テンプレートのカスタマイズPDF

テンプレートをカスタマイズするには、テンプレートコンポーネントを調整し、スタイルシートを使用してスタイル形式を適用します。

テンプレートテンプレートをPDFするには、次の手順に従います。
1. Web エディターで、「出力」タブに移動します。
1. 左側のサイドバーを展開し、「テンプレート」をクリックします。

   テンプレートパネルが開きます。
1. テンプレートのコンポーネントを表示するには、次のいずれかの操作を行います。

   * テンプレートの横にある「 / 」アイコンをクリックするか、テンプレート名をダブルクリックします。
   * テンプレートの上にマウスポインターを置いて…（オプションアイコン）をクリックし、コンテキストメニューから「編集」を選択します。

      デフォルトでは、テンプレートエディターに設定パネルが開きます。
   <img src="assets/customize-pdf-template.png" alt="テンプレートのPDF" width="350">

   カスタマイズ可能な様々なテンプレートコンポーネントは、次のセクションに分類されます。
   * ページレイアウト：一般的なPDFには、表紙やタイトルページ、目次、章、索引など、様々なページが含まれます。 「ページレイアウト」セクションを使用すると、PDFを構成する様々なページのルックアンドフィールをデザインできます。 外観に加えて、ページ上のヘッダー、フッター、コンテンツ領域などのページ要素の配置を定義することもできます。 ページのレイアウトのカスタマイズについて詳しくは、 ***ページレイアウトの作成とカスタマイズ***.
   * スタイルシート：「スタイルシート」セクションの設定を使用すると、TOC、インデックス、用語集など、ページレイアウトコンポーネントの外観をカスタマイズできます。 また、見出し、段落、リストなどの DITA コンテンツのスタイルをカスタマイズすることもできます。 スタイルシートの使用について詳しくは、 ***スタイルシートを使用したPDFのカスタマイズ***.
   * リソース：アセットテンプレートのカスタマイズやデザインに必要なPDFファイルを保存します。 ロゴ、カスタムフォント、背景画像などのアセットは、リソースに保存されます。 リソースの活用について詳しくは、 ***リソースの使用***.
   * 設定：テンプレートを使用してテンプレートを生成するための出力PDFを設定します。 このセクションでは、PDF、チャプター開始ページ、印刷マーカーなどの、様々なページのテンプレートマッピングを定義できます。 設定の適用について詳しくは、 ***詳細PDF設定***.
1. テンプレートコンポーネントをカスタマイズするには、テンプレートコンポーネントをダブルクリックするか、その前の/アイコンをクリックします。

   例えば、 *ページレイアウト* または *>* 前のアイコン *ページレイアウト* をクリックして、使用可能なページレイアウトを表示します。
1. 必要な変更を加えたら、「 *すべて保存* ( または `Ctrl+S`) をクリックします。

