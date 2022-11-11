---
title: ネイティブPDF公開機能 |共通のコンテンツスタイルの使用
description: スタイルシートを作成し、コンテンツのスタイルを作成する方法を説明します。
source-git-commit: a1367a6915e760e533bb984705f4be37596b5477
workflow-type: tm+mt
source-wordcount: '3496'
ht-degree: 0%

---


# 共通のコンテンツスタイルの使用 {#work-with-common-styles}

スタイルシートには、PDF出力で使用される要素のスタイルの定義が含まれます。 サンプルのスタイルシートを使用するか、新しいスタイルシートを作成するかを選択できます。 ほとんどの場合、OOTB サンプルスタイルシートのコピーを作成すると、すぐに使い始めるのに役立ちます。

スタイルエディターは WYSIWYG エディターで、ユーザーインターフェイスの背後にある CSS コードの複雑さをすべて非表示にします。 スタイルエディターを使用すると、選択した要素のスタイルを簡単かつ迅速にカスタマイズできます。 スタイルは次の見出しの下に分類されます。

* 見出しスタイル
* 段落スタイル
* 文字スタイル
* ハイパーリンクのスタイル
* 画像スタイル
* リストスタイル
* テーブルスタイル
* Div スタイル
* ページスタイル
* その他のスタイル

構造化 DITA コンテンツを使用する場合、ほとんどの DITA 要素のスタイルマッピングがデフォルトのスタイルシートに配置されます。 標準の DITA 要素を使用している場合は、スタイル定義を直接変更することで、外観と操作性を変更できます。 これらのスタイル定義は、「その他のスタイル」カテゴリで使用できます。 詳しくは、 [他のスタイルの使用](#other-styles) このトピックの後半で説明します。

以下の節では、最もよく使用されるスタイル設定を例の形式で説明します。

>[!NOTE]
>
>次の例では、製品に付属のサンプルスタイルシートを使用していることを前提としています。

## 見出しスタイルの操作 {#heading-styles}

見出しスタイルは、コンテンツで使用される見出しのすべての基本スタイルをカプセル化します。 OOTB では、トピック/章と付録のタイトル見出しの 6 つの基本見出しスタイルと見出しスタイルが取得されます。 構造化文書では、H1 はトピックまたはチャプターのタイトルを表し、H2～H6 はトピックまたはチャプター内のサブトピックまたはセクションに使用されます。 この見出しの階層は、対応する見出しが見つかるたびに、コンテンツに自動的に適用されます。

>[!NOTE]
>
>独自のカスタム見出しスタイルを作成し、output クラスを使用してコンテンツで使用できます。 詳しくは、 [ページの向きとビューの回転を使用](design-page-layout.md#page-orientation-rotation) 例：

### カスタムのチャプターレベルの見出しを作成する {#create-chapter-level-heading}

本（またはブックマップ）では、章を扱います。 基本の見出しスタイルは、カスタマイズせずにチャプターレベルの見出しに適用されるように設計されています。 ただし、コンテンツ用に特殊な見出しを作成する場合は、それらの見出しを作成する必要があります。 例えば、デフォルトの `h1.chapter` 見出しがチャプターのタイトルに適用されます。 チャプタータイトルを別のスタイルで表示する場合は、 `h1.chapter` スタイル。 同様に、章の小見出しのカスタムスタイルを作成できます。 例えば、2 つすべての<sup>nd</sup> および 3<sup>rd</sup> レベルの見出しを使用する場合は、新しいスタイルを `h2.chatper` および `h3.chatper`.

ネイティブPDF公開機能には、最も一般的なスタイルの基本スタイル定義が含まれているので、誤ってスタイルを削除した場合でも、デフォルトのスタイルがコンテンツに適用されます。 例えば、スタイルシートに h2 スタイルのスタイル定義がない場合、ネイティブPDFパブリッシング機能は h2 コンテンツに基本スタイルを適用します。

この例では、第 2 レベルの章見出しスタイルを作成します。

1. 必要なスタイルシートを編集用に開きます。
   >[!NOTE]
   >
   >詳しくは、 [定義済みまたは新しいスタイルのカスタマイズ](components-pdf-template.md#customize-style) スタイルシートを開いてカスタマイズまたは編集するためのセクション。

1. 内 **スタイル** リスト、展開 **見出しスタイル**.
1. 右クリック **見出しスタイル** スタイルと選択 **新しいスタイル**.
1. 内 *スタイルを追加* ダイアログ、 **タグ** 名前： `h2` と入力します。 `chapter` 内 **クラス** 名前フィールド。
1. 「**完了**」をクリックします。

という名前の新しい見出しスタイル `h2.chapter` が作成され、「見出しスタイル」リストに追加されます。

スタイルを作成したら、スタイルエディターを使用して、スタイルの必要なプロパティをカスタマイズできます。

### 自動番号の見出しを作成する {#auto-number-heading}

最も一般的に使用される出力スタイルの 1 つに、自動番号付きの見出しがあります。 これらの見出しは、章番号、トピックおよびサブトピック番号を表します。 自動番号の見出しは、トピック内の項目のリストに自動番号が割り当てられるリストスタイルとは異なります。

この例では、見出しをレベル 1 からレベル 3 にカスタマイズし、異なる形式の自動番号を使用します。

1. 必要なスタイルシートを編集用に開きます。

   >[!NOTE]
   >
   >詳しくは、 [定義済みまたは新しいスタイルのカスタマイズ](components-pdf-template.md#customize-style) スタイルシートを開いてカスタマイズまたは編集するためのセクション。

1. 内 **スタイル** リスト、展開 **見出しスタイル**.

1. を選択します。 **h1** スタイルを指定します。
h1 スタイルのプロパティは、プレビューと共にプロパティパネルに表示されます。

   >[!NOTE]
   >
   >プレビューパネルでは、任意の要素に適用したスタイル更新をリアルタイムで確認できます。

1. を選択します。 **自動番号** プロパティ。

   自動番号リストに適用できるスタイルは、 Autonumber プロパティの下に表示されます。

1. 次のプロパティを設定します。
   * **スタイル**:ロケール固有または汎用の番号付けスタイルの幅広い範囲から選択します。 アラビア語 — インディック語、デバナガリ語、ジョージア語、小数点、小文字のアルファなどのスタイルを選択できます。 現在の例では、「 」を選択します。 `upper-alpha`.

   * **形式**:デフォルトの形式はに設定されています。 `<x>`で、 `x` の値は、Style プロパティで選択した番号付けスタイルに置き換えられます。 例えば、 `decimal` (1) スタイル、次に `x` 自動増分は、 `h1` 「スタイル」は 2、3 などに設定します。 また、フィールドにカスタムテキストを追加して、見出しのスタイルを書式設定することもできます。 例えば、すべての h1 見出しにプレフィックスを付けたい場合、 `Chapter`の場合、このフィールドを `Chapter <x>`.

   * **文字の挿入**:書式に特殊文字を追加する場合は、挿入ボタン (<img src="./assets/insert-chars.png" width="25">) icon. スタイル形式で追加する文字を選択し、「挿入」をクリックします。 「カテゴリの選択」ドロップダウンリストから選択できる特殊文字には、様々なタイプがあります。 この例では、「句読点」カテゴリから右向き二重山括弧を選択します。

      <img src="./assets/insert-special-chars.png" width="400">


   * **開始番号**:特定の数から開始する番号を設定する場合は、その値を指定します。 この例では、デフォルト値の 1 のままにします。

   * **インデント**:見出しのインデントを設定する場合は、「インデント」の値を設定する必要があります。 この例では、値を 0 px に設定します。

      >[!NOTE]
      >
      >値は、px （ピクセル）、pt （ポイント）、rem、em、% （パーセント）または in （インチ）単位で入力できます。

   * **プレフィックスの幅**:これは、自動番号フォーマットが適用される領域です。 選択したスタイル形式に容易に対応できるサイズに自動的に設定されます。 サイズを増やす場合は、デフォルト値を置き換えることができます。

      この値を手動で設定する場合は、幅に影響を与える他のプロパティを変更してみてください。 例えば、フォントサイズ、プレフィックス（チャプター）付きの形式、サフィックス (:) を変更するには、 *開始番号* プロパティと、最適なサイズになる様々なフォントプロパティを設定します。

      この例では、デフォルト値のままにします。

   * **間隔**:水平方向と垂直方向の間隔を指定します。 この例では、デフォルト値のままにします。

      上記のカスタマイズにより、スタイルは次のようにカスタマイズされます。

      <img src="./assets/h1-style-custmization.png" width="500">

   * **書式の適用先**:[ 自動番号 ] カテゴリのプロパティは、番号付けスタイルの定義に役立ちます。 段落番号のスタイルや見出し書式の内容をさらにカスタマイズするには、このフィールドで「段落番号」または「段落番号」を選択します。 [ 段落番号 ] を選択した場合、[ フォント ]、[ 罫線 ]、[ レイアウト ]、およびその他のカテゴリに対する変更は、見出しの段落番号スタイルにのみ適用されます。 ただし、「段落」を選択した場合、変更は段落番号スタイルではなく見出しコンテンツに適用されます。

   次のスクリーンショットに示す出力を生成するには、次の設定を使用します。

   |**見出しのスタイル**|**プロパティ**|**値**|**追加のコメント**| | :- | :- | :- | :- | |h1|スタイル|小数|これらのプロパティは自動番号カテゴリの下にあります | ||形式|`Capter <x>:`|| ||接頭辞の幅|160 px|| ||フォント/テキストの整列|左|書式の適用先が段落番号に設定されていることを確認してください| |h2|スタイル|小数|これらのプロパティは自動番号カテゴリの下にあります | ||形式|`Section <x>:`|| ||接頭辞の幅|125 px|| ||フォント/テキストの整列|左|書式の適用先が段落番号に設定されていることを確認してください| |h3|スタイル|小数|これらのプロパティは自動番号カテゴリの下にあります | ||レベルの挿入|2|| ||形式|`Section <2>.<x>:`|| ||接頭辞の幅|125 px|| ||フォント/テキストの整列|左|書式の適用先が段落番号に設定されていることを確認してください| ||

   <img src="./assets/auto-number-output.png" width="500">

## 段落スタイルの操作 {#paragraph-style}

段落スタイルを作成して、段落全体に特別な書式を適用できます。 ただし、擬似クラスを使用すると、文字の特定の部分にのみスタイルを適用できます。 次の例では、ドロップキャップスタイルを使用する段落スタイルを作成します。

### ドロップキャップスタイルを作成する {#drop-cap-style}

雑誌や文学文書では、段落やセクションの最初の文字に特別なスタイルを付けたドロップキャップ（またはドロップキャピタル）スタイルが使用されます。 同じ効果を実現するには、ネイティブPDF公開機能を使用します。

次の例では、ドロップキャップスタイルを作成します。

1. 必要なスタイルシートを編集用に開きます。

   >[!NOTE]
   詳しくは、 [定義済みまたは新しいスタイルのカスタマイズ](components-pdf-template.md#customize-style) スタイルシートを開いてカスタマイズまたは編集するためのセクション。

1. 内 **スタイル** リスト、展開 **段落スタイル**.

1. を右クリックします。 **段落スタイル** を選択します。 **新しいスタイル**.

1. 内 *スタイルを追加* ダイアログ、 **タグ** 名前は p で、 **疑似** **クラス** フィールド、選択 `::first-letter`.

1. 「**完了**」をクリックします。

   新しい段落スタイル： `::first-letter`  が作成され、 **段落スタイル** リスト。

1. 選択 `::first-letter` p スタイルの下で、次のプロパティを設定します。

   * **フォント**:段落の最初の文字に使用するフォントを設定します。 この例では、「フォントファミリー」を「カーシブ」に、「フォントの太さ」を「500」に、「フォントサイズ」を「30pt」に設定し、フォントの色を選択します。

   * **レイアウト**:ドロップキャップスタイルの周囲のテキストの垂直方向の位置を設定します。 この例では、[ 垂直方向の位置合わせ ] を [ 下 ] に設定します。

を `p` タグが `<p>` 要素を使用する場合、outputclass 属性を使用してこのスタイルを明示的に追加する必要はありません。 コンテンツ内の任意の場所に `<p>` 要素を使用すると、ドロップキャップスタイルが自動的に適用されます。 次のスクリーンショットでは、チャプタータイトル、短い説明、定義リストの要素がドロップキャップスタイルでフォーマットされていません。 ドロップキャップスタイルを使用して書式設定されるのは、段落スタイルのみです。

<img src="./assets/char-style-drop-cap.png" width="500">

## 文字スタイルの操作 {#char-style}

文字スタイルを使用して、コンテンツ内の文字や単語を書式設定するためのスタイルを作成できます。 例えば、インラインコードやファイル名の文字スタイルを作成したり、選択したコンテンツに対して複数のスタイル形式を使用するスタイルを作成したりできます。

### インライン文字スタイルの作成 {#inline-char-style}

段落内のインライン文字や単語の書式設定は、非常に一般的なスタイルです。 インラインスタイルを作成するプロセスには、まず、スタイルシートで新しいスタイルを作成し、次に、 `outputclass` 属性。

次の例では、インライン文字スタイルを作成します。

1. 必要なスタイルシートを編集用に開きます。

   >[!NOTE]
   詳しくは、 [定義済みまたは新しいスタイルのカスタマイズ](components-pdf-template.md#customize-style) スタイルシートを開いてカスタマイズまたは編集するためのセクション。

1. 内 **スタイル** リスト、展開 **文字スタイル**.

1. を右クリックします。 **文字スタイル** を選択します。 **新しいスタイル**.

1. スタイルを追加ダイアログで、「 **タグ** span という名前を付け、と入力します。 `BoldItalic` 内 **クラス** 名前フィールド。

   <img src="./assets/create-char-style.png" width="400">

1. 「**完了**」をクリックします。

   code という名前の新しい文字スタイルが作成され、[ 文字スタイル ] リストに追加されます。

1. 選択 `span.BoldItalic` から **文字スタイル** リストを作成し、次のプロパティを設定します。

   * **フォント**:フォント関連のすべてのプロパティは、このセクションからカスタマイズできます。 デフォルトでは、製品にバンドルされているフォントがあります。 文字スタイルに必要なフォントを選択できます。 この例では、フォントファミリーを *セリフ、* を選択し、 *太字* および *斜体* をクリックします。 また、フォントの太さ（太字、明るい太さなど）、テキスト装飾（下線、上線など）、フォントサイズ、フォントカラー、テキストの整列など、その他のフォントプロパティをカスタマイズすることもできます。

      >[!NOTE]
      また、テンプレートの「リソース」セクションに保存されているフォントをテンプレートに追加することもできます。 フォントの追加とリソースの使用について詳しくは、 [リソースの使用](components-pdf-template.md#work-with-resources).

   * **レイアウト**:レイアウト関連のプロパティ（高さと幅、余白、パディング、整列など）を設定できます。

   * **背景**:Background プロパティを使用すると、特定のスタイルの背景色を書式設定できます。 任意のスタイルの背景色や画像を定義できます。

インライン文字スタイルを作成したら、それをコンテンツに適用する必要があります。 インラインコードスタイルを適用するには、ソースビューに移動して、 `outputclass` 属性を次の中から選択します。

`outputclass="BoldItalic"`

次の例は、実行中のテキストの様々な場所に太字斜体書式を適用する場合を示しています。

<img src="./assets/char-format-applied.png" width="500">

## リストスタイルのカスタマイズ {#custom-list-style}

リストスタイルには、順序付きリストと順序なしリストの既定のスタイル設定が含まれます。 これらのリストスタイルは、ドキュメントの要件に合わせて簡単にカスタマイズできます。

次の例では、番号付きリストスタイルまたは番号付きリストスタイルをカスタマイズします。

1. 必要なスタイルシートを編集用に開きます。

   >[!NOTE]
   詳しくは、 [定義済みまたは新しいスタイルのカスタマイズ](components-pdf-template.md#customize-style) スタイルシートを開いてカスタマイズまたは編集するためのセクション。

1. 内 **スタイル** リスト、展開 **リストスタイル**.

1. を選択します。 **ol** スタイルを指定します。

   スタイルのプロパティは、プレビューと共にプロパティパネルに表示されます。

   <img src="./assets/list-style-default.png" width="500">

1. を選択します。 **詳細フォーマット** オプション。

   確認メッセージが表示されます。

1. クリック **はい** の *確認* 開くメッセージ **詳細フォーマット** プロパティ。

   デフォルトでは、次のプロパティを使用できます。

   * **レベル**:デフォルトでは、番号付きリストは 6 つのレベルです。 このドロップダウンで選択したレベルによって、選択したレベルとそれ以降のすべてのレベルでのスタイルの変更が制御されます。 たとえば、レベル 4 を選択した場合、適用するすべてのスタイル変更はレベル 4、5、6 に設定されます。

   * **リストスタイルの種類**:リストの番号付けスタイルには、選択可能なものが多数あります。 このリストには、番号付きリストの作成に使用されるロケール固有および汎用の番号付きスタイルが含まれます。 リストのスタイルの種類には、アラビア語、カンボジア語、デバナガリ語、エチオピア語、ハングル語、ヘブライ語、日本語、韓国語、簡体字中国語、ウルドゥ語などがあります。

   さらに、次の詳細フォーマットプロパティを使用できます。

   * **数値の形式**:デフォルトの形式はに設定されています。 `<x>`で、 `x` の値は、[ リストスタイルの種類 ] プロパティで選択した番号スタイルに置き換えられます。 例えば、 `decimal` (1) スタイル、次に `x` は、リスト要素の各インスタンスに対して自動的に増分され、2、3 などとなります。 また、フィールドにカスタムテキストを追加して、リストのスタイルを書式設定することもできます。 例えば、すべての第 1 レベルのリストスタイルに「`)`&quot;の場合、このフィールドを第 1 レベルのリストスタイル用に&quot;`<x>)`&quot;.

   * **文字の挿入**:数値書式に特殊文字を追加する場合は、挿入文字 (<img src="./assets/insert-chars.png" width="25">) アイコンをクリックします。 スタイル形式で追加する文字を選択し、「挿入」をクリックします。 「カテゴリの選択」ドロップダウンリストから選択できる特殊文字には、様々なタイプがあります。

   * **レベルの挿入**:前のレベルの数値を数値の形式で含めることができます。 例えば、第 5 レベルの数値書式を第 6 レベルの数値書式に含める場合は、レベルの挿入ドロップダウンリストで「5」を選択します。 [ レベルの挿入 ] ドロップダウンには、前のレベルのみの数が表示され、後のレベルは表示されないことに注意してください。 たとえば、レベル 3 の場合、[ レベルの挿入 ] リストにはレベル 1 とレベル 2 のみが表示されます。

      <img src="./assets/list-insert-level.png" width="400">

      必要に応じて、リスト値を表示するように数値フォーマットを変更することもできます。 例えば、レベル 3 にネストされた段落番号スタイルを使用する場合は、「`<2>.<x>))`&quot;. リスト番号 2、ピリオド、リスト番号 3、2 つの括弧が表示されます。 `2.3))`.

   * **インデント**:リストのインデントを設定する場合は、「インデント」の値を設定する必要があります。 インデントの変更は、プレビューパネルで確認し、調整できます。

      >[!NOTE]
      値は、px （ピクセル）、pt （ポイント）、rem、em、% （パーセント）または in （インチ）単位で入力できます。

   * **プレフィックスの幅**:これは、数値の形式が適用される領域です。 選択した形式に容易に対応できるサイズに自動的に設定されます。 サイズを増やす場合は、デフォルト値を置き換えることができます。

      この値を手動で設定する場合は、幅に影響を与える他のプロパティを変更してみてください。 例えば、フォントサイズ、プレフィックスまたはサフィックスの付いた形式、および最適なサイズになる様々なフォントプロパティを変更します。

   * **間隔**:リスト番号形式とコンテンツとの間の水平方向の間隔を指定します。 垂直方向の間隔で、2 つのリスト項目の間隔を制御します。

      次のスクリーンショットは、各レベルのカスタマイズされた順序付きリストを示しています。

      <img src="./assets/list-number-format-final.png" width="500">


## 表スタイルの操作 {#table-styles}

スタイルシートを使用して、 *n* テーブルスタイルの数。 テーブルスタイルを使用すると、テーブル全体、特定の行または列をどのようにデザインできます。 セルレベルのスタイル設定でのコントロールを使用すると、非常に見やすい表スタイルを作成できます。

次の例では、テーブルスタイルの作成方法と、カスタマイズ可能な様々なテーブルスタイル設定オプションを確認します。

1. 必要なスタイルシートを編集用に開きます。

   >[!NOTE]
   詳しくは、 [定義済みまたは新しいスタイルのカスタマイズ](components-pdf-template.md#customize-style) スタイルシートを開いてカスタマイズまたは編集するためのセクション。

1. 内 **スタイル** リストで、 **テーブルスタイル** を選択します。 **新しいスタイル**.

1. 内 *スタイルを追加* ダイアログ、 **タグ** 名前： `table` と入力します。 `double-border` 内 **クラス** 名前フィールド。

1. 「**完了**」をクリックします。

   という名前の新しい表スタイル `table.double-border` が作成され、[ 表スタイル ] リストに追加されます。

1. 選択 `table.double-border` から **テーブルスタイル** リストを作成し、次のプロパティを設定します。

   * **書式の適用先**:表全体、奇数/偶数の行または列、最初/最後の行または列にスタイル書式を適用するよう選択できます。

      >[!NOTE]
      以下の設定が **一般** セクション **書式の適用先** が **テーブル全体**.

   * **テキストの折り返し**:テーブルの周囲でテキストを折り返す方法を選択します。 これは、テーブルが別のブロックレベル要素内にあり、そのブロック要素内の他のコンテンツと共にテーブルをレンダリングする必要がある場合に役立ちます。 ラッピングのオプションは次のとおりです *left* または *右* 整列または *なし*.

   * **境界線を折りたたむ**:表の罫線の外観を選択します。 「折りたたむ」を選択した場合は、表のセルの間に罫線が 1 本だけ描画されます。 ただし、別のスタイルの場合は、各セルの周囲に境界線が表示され、パディングが追加されます。

      <img src="./assets/table-style-collapse-separate.png" width="500">

   * **境界線の間隔**:この設定は、[ 境界線の折りたたみ ] が [ 分離 ] に設定されている場合にのみ使用できます。 この設定を使用すると、セルの境界線間の垂直方向と水平方向の間隔を指定できます。

      <img src="./assets/table-border-spacing.png" width="500">

      >[!NOTE]
      以下の設定が **セル** セクション **書式の適用先** が **テーブル全体**.

   * **パディング**:テーブルのセル間のパディングを指定します。 上、下、左、右の各辺に別々のパディング値を指定できます。

   * **垂直方向揃え**:セルコンテンツの垂直方向の配置を指定します。 次のオプションを使用できます。上、中央、下。

   * **境界線の太さ、スタイル、色、幅、半径：** 境界線関連のプロパティを指定します。 「左」や「右」など、特定の辺にのみ境界線を設定できます。 境界線のスタイルには、実線、破線、二重線など、使用可能な境界線のスタイルが表示されます。 カラーパレットを使用して境界線の色を指定します。 境界線の幅は、px、pt、rem、em、%および単位で指定できます。 半径 (Radius) は、円形のコーナーを作成するカーブを定義します。

   このトピックの他の例では、フォント、境界線、レイアウト、ページネーション、背景の下にあるその他のプロパティについて説明します。 選択に応じて、 **書式の適用先** プロパティを使用すると、これらの値をテーブル全体または選択した行や列に適用できます。

   異なる行が異なる形式であるサンプルテーブルのプレビューを次に示します。

   <img src="./assets/table-final-design.png" width="500">

## 他のスタイルの使用 {#other-styles}

構造化 (DITA) コンテンツを使用している場合、ほとんどの DITA 要素にデフォルトのスタイルシート内のスタイルマッピングが含まれています。 例： `<shortdesc>` 要素のスタイルが次の場所で定義されている **その他のスタイル** > **.shortdesc** スタイル定義。 これらのスタイルは、簡単にカスタマイズでき、構造化コンテンツから生成されるPDF出力に自動的に適用されます。 つまり、他のカスタムスタイルとは異なり、 `outputclass` 属性を設定します。

デフォルトでは使用できない要素やカスタム要素に対してスタイル定義を作成する場合は、スタイルシートで簡単に作成できます。 ここで考慮する必要がある点は、構造化要素の名前と同じ名前のスタイルを作成することだけです。

次の例では、新しいウィンドウのタイトル (`wintitle`) スタイル：

1. 必要なスタイルシートを編集用に開きます。

   >[!NOTE]
   詳しくは、 [定義済みまたは新しいスタイルのカスタマイズ](components-pdf-template.md#customize-style) スタイルシートを開いてカスタマイズまたは編集するためのセクション。

1. 内 **スタイル** リスト、展開 **その他のスタイル**.

1. を右クリックします。 **その他のスタイル** を選択します。 **新しいスタイル**.

1. 内 *スタイルを追加* ダイアログ、 **タグ** 名前： *空白* と入力します。 `wintitle` 内 **クラス** 名前フィールド。

   形式 `wintitle` は認識された DITA 要素名です。スタイル定義は `<wintitle>` 要素を選択します。

1. 「**完了**」をクリックします。

   という名前の新しいスタイル `.wintitle` が作成され、 **その他のスタイル** リスト。

1. .wintitle を **その他のスタイル** リストを作成し、必要に応じてプロパティを設定します。

次のスクリーンショットは、「プライマリ制御」というテキストに適用される wintitle スタイルを示しています。

<img src="./assets/other-style-wintitle.png" width="500">