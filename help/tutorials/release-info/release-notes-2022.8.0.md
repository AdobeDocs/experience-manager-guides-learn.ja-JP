---
title: リリースノート | Adobe Experience Managerガイドas a Cloud Service、2022 年 8 月リリース
description: Adobe Experience Manager Guides の最新リリースのas a Cloud Service
source-git-commit: 7cc33e4621c2bfbf08a720f173e8e419c5424a6c
workflow-type: tm+mt
source-wordcount: '1156'
ht-degree: 2%

---

# Adobe Experience Manager Guides の最新リリースのas a Cloud Service

## 最新リリースへのアップグレード

現在のAdobe Experience Managerガイドをas a Cloud Service的にアップグレード ( 後で *AEMガイドas a Cloud Service*) を設定する必要があります。
1. Cloud Servicesの Git コードを確認し、アップグレードする環境に対応するCloud Servicesパイプラインで設定されたブランチに切り替えます。
2. 更新 `<dox.version>` プロパティ `/dox/dox.installer/pom.xml` ファイルのCloud ServicesGit コードを 2022.8.167 に変更します。
3. 変更をコミットし、Cloud Servicesパイプラインを実行して、AEM Guides as a Cloud Serviceの最新リリースにアップグレードします。

## 互換性マトリックス

この節では、AEMガイドのas a Cloud Service 2022 年 8 月リリースでサポートされるソフトウェアアプリケーションの互換性マトリックスを示します。

### FrameMaker と FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| 互換性がありません | 2020 Update 4 以降 |
|  |  |

* AEMで作成されたベースラインと条件は、2020.2 以降の FMPS リリースでサポートされています。

### 酸素コネクタ

| AEM Guides as a Cloud リリース | Oxygen Connector ウィンドウ | Oxygen Connector Mac |
| --- | --- | --- |
| 2022.8.0 | 2.7.5 | 2.7.5 |
|  |  |  |


## 新機能および機能強化

AEMガイドas a Cloud Serviceは、最新リリースの様々な機能強化と新機能を提供します。

### マップエディタのレイアウトビュー

これで、マップエディタで DITA マップの完全なレイアウトを表示できます。 編集用にマップを開くと、 **レイアウト** マップエディタのビュー このビューでは、ツリービューでマップ階層を表示し、マップ内のトピックを整理または構造化することができます。

![レイアウト表示](assets/layout-view-map.png)

レイアウトビューには、マップに存在するトピックに対して多くのタスクを実行するのに役立つ個別のツールバーが含まれています。
トピック参照、トピックグループ、キー定義をマップに挿入できます。 マップ内のトピックを上下左右に移動すると、トピックを再編成できます。 トピックをドラッグ&amp;ドロップしてマップに移動することもできます。 また、マップエディタには、ファイルのロックまたはロック解除、バージョン履歴の確認、バージョンラベル管理を行うためのアイコンも表示されます。


レイアウトビューでは、 **表示オプション** 行番号の表示/非表示を切り替えるには、チェックボックスを表示/非表示にするか、マップ内のトピックのファイル名やタイトルを表示します。


![view-options](assets/view-options.png)

また、適用された条件フィルターに基づいてトピックを表示することもできます。

マップファイル内のトピックを整理する以外に、 **オプション** レイアウトビューの要素で使用できるメニュー また、リポジトリパネルからマップエディタで開いたマップに、トピックまたはマップをドラッグ&amp;ドロップすることもできます。

右側のパネルでは、マップエディタのレイアウトビューに [ コンテンツプロパティ ] と [ マッププロパティ ] が表示されます。 選択したトピックに対して定義されたインライン属性が、レイアウトビューのトピックに対して表示されます。 例えば、platform 属性が `IOS`.

次に、トピックまたはマップのメタデータ情報を設定することもできます。 選択したトピックまたはマップに対して、ナビゲーションタイトル、リンクテキスト、短い説明およびキーワードを定義できます。

![レイアウトビュー右パネル](assets/layout-inline-attributes.png)

詳しくは、 *レイアウト表示* 『 Adobe Experience Manager Guides の使用』のas a Cloud Serviceの節を参照してください。

### エディタ設定のインライン属性

AEMガイドで **インライン属性** 管理者が **エディター設定**. また、新しいインライン属性を追加したり、既存の属性を **インライン属性** 」タブをクリックします。
トピックに対して定義された設定済みのインライン属性が、レイアウト表示のトピックに対して表示されます。

![エディター設定](assets/editor-settings-inline-attributes.png)


### リポジトリ表示の追加フィルター

現在は、リポジトリ表示でのフィルター検索がより強力になりました。 2 つの新しい検索条件、 **最終変更日** および **タグ** ファイルをフィルタリングし、AEMリポジトリでの検索を絞り込むためのが追加されました。
* **最終変更日**:選択した日付の後、選択した日付の前に最後に変更されたファイルを検索できます。 また、事前定義された条件を使用して、過去 2 時間、先週、先月または昨年に最後に変更されたファイルを探すこともできます。
* **タグ**:また、特定のタグが適用されているファイルを探すこともできます。 タグを入力するか、ドロップダウンリストから選択できます。

![リポジトリ表示フィルター](assets/repo-filter-search.png)


## 修正された問題

様々な領域で修正されたバグを以下に示します。

* 非推奨の Lucene インデックスは/core/article-publish/src/main/java/com/adobe/dxml/article/publish/util/DoxUtils.java (9291) で使用されます
* 更新された Node.js は公開に使用されません。 (9835)
* DITA トピックは、 **プロパティ** ページ。 (8745)
* DITA ブックマップに追加された際の FrontMattere 要素が正しく機能しません。 (9507)
* ネイティブPDF |使用時に空のPDFが生成されます **クイック生成** 複数のファイルに対して、空の要素が選択されている場合。 (9822)
* ネイティブPDF |付録は、章としてPDF出力に公開されます。 (9829)
* ネイティブPDF |SVG画像が編集されても、ページレイアウトには更新されて表示されません。 (9069)
* 通常のハイフンは、 `Nonbreaking Hyphen` 文字が **特殊文字の挿入** ダイアログ。 (8919)
* 編集済みの場合、XML Editor では、トピック内に更新済みの画像は表示されません。 (9500)
* エディターを使用して出力を公開する際に、プリセットを **出力** タブをクリックします。 (9100)
* DITA マップのサブマップは、 **すべてを選択** 」オプションを使用します。 (9814)
* マップまたはトピックテンプレートをからドラッグ&amp;ドロップできません **テンプレート** Web エディターのカスタムマップテンプレートへのメニュー。 (9846)
* マップまたはトピックテンプレートのサブフォルダーに新しいトピックまたはマップテンプレートを作成できません。 (9888)
* マップまたはトピックテンプレートのサブフォルダ内に存在するトピックまたはマップを参照するオプションはありません。 (9889)
* DITA ファイルと共に Schematron ファイルを更新して保存すると、右側のパネルは表示されません（DITA ファイルが Schematron ファイルに存在する検証機能を壊した場合）。 (9986)
* 名前が既存のプリセットと同じ場合は、新しい重複出力プリセットを作成できます。 (9997)
* SVG出力の生成時に、HTML画像が破損し、正しく公開されない。 (9949)


## 既知の問題

Adobeは、2022 年 8 月のリリースのAEMガイドに関して、次の既知の問題を特定しました。

### 回避策に関する既知の問題

次の既知の問題に対して、特定の回避策を使用します。

* [ レイアウト ] ビューは、マップエディタには表示されません。

   **回避策**:フォルダープロファイルの ui_config.json を更新します。

* 8919 の問題が発生するように、Symbols.json が上書きされます。

   **回避策**:更新された symbols.json は、上書きされた symbols.json と結合する必要があります。

### その他の既知の問題

* リポジトリでの検索の実行時に表示される結果セクションから複数のファイルを選択し、作成者ビューでドラッグ&amp;ドロップした場合、1 つのファイルのみが追加されます。