---
title: リリースノート | Adobe Experience Managerガイド 4.2.1 リリースのアップグレード手順と修正された問題
description: バグ修正とAdobe Experience Managerガイドの 4.2.1 リリースにアップグレードする方法について説明します
source-git-commit: 7fdbf99a1224124d63acaebc626e3b09475f3096
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 5%

---

# 4.2.1 Adobe Experience Managerガイド（2023 年 5 月）

このリリースノートでは、アップグレード手順、互換性マトリックス、Adobe Experience Managerガイドのバージョン 4.2.1 リリース ( 後で *AEMガイド*) をクリックします。

新機能および機能強化について詳しくは、 [Adobe Experience Managerガイドの 4.2.1 リリースの新機能](whats-new-4.2.1-release.md).

## AEMガイドの 4.2.1 リリースへのアップグレード


現在のバージョンのAEMガイドを簡単にバージョン 4.2.1 にアップグレードできます。AEMガイドのバージョン 4.2.1 へのアップグレードを進める前に、次の点を考慮する必要があります。現在のバージョンのAEMガイドをバージョン 4.2.1 にアップグレードできます
* バージョン 4.1、4.1.x または 4.2 を使用している場合は、バージョン 4.2.1 に直接アップグレードできます。
* バージョン 4.0 を使用している場合は、バージョン 4.2.1 にアップグレードする前に、バージョン 4.2 にアップグレードする必要があります。
* バージョン 3.8.5 を使用している場合は、バージョン 4.2 にアップグレードする前に、バージョン 4.0 にアップグレードする必要があります。
* 3.8.5 より前のバージョンを使用している場合は、製品固有のインストールガイドの「 AEMガイドのアップグレード」の節を参照してください。

>[!NOTE]
>
>AEM Guides バージョンをアップグレードする前に、AEM Service Pack をインストールする必要があります。

詳しくは、 [アップグレードの手順](../install-guide/upgrade-xml-documentation.md).

## 互換性マトリックス

この節では、AEMガイド 4.2 でサポートされているソフトウェアアプリケーションの互換性マトリックスを示します。 1 リリース。

### Adobe Experience Manager

**非 UUID**
バージョン 6.5 Service Pack 15、14、13、または 12

**UUID**
バージョン 6.5 Service Pack 15、14、13、または 12

詳しくは、 *技術要件* 『 Adobe Experience Managerガイドのインストールと設定』の節を参照してください。

### FrameMaker と FrameMaker Publishing Server

| リリース | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.2.1（非 UUID） | 2022 以降 | 2020.2 以降* | 2022 以降 | 2020.3 以降 |
| 4.2.1(UUID) | 2022 以降 | 2020.2 以降* | 2022 以降 | 2020.4 以降 |
|  |  |  |  |

* AEMで作成されたベースラインと条件は、2020.2 以降の FMPS リリースでサポートされています。

### 酸素コネクタ

| リリース | Oxygen Connector ウィンドウ | Oxygen Connector Mac | Oxygen Windows で編集 | Oxen Macで編集 |
| --- | --- | --- |--- |--- |
| 4.2.1（非 UUID） | 2.2-regular-3 | 2.2-regular-3 | 1.6 | 1.6 |
| 4.2.1(UUID) | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |

## 修正された問題

様々な領域で修正されたバグを以下に示します。

### オーサリング

* レイアウト表示から作成者またはソース表示に切り替えると、コンテンツからナビゲーションタイトルが削除されます。 (12174)
* Web エディタの閉じるボタンがAEMナビゲーションページに移動しない。 (11948)
* DITA マップをクリックしたときにアプリケーションエラーが発生する場合があります。 (11842)
* 「変更の追跡」がオンの既存のリスト項目の代わりに移動（ドラッグ&amp;ドロップ）すると問題が発生します。 (11570)
* 「変更の追跡」がオンの新しいリスト項目として移動（ドラッグ&amp;ドロップ）すると問題が発生します。 (11569)
* [ 変更の追跡 ] で、リスト項目のインデントまたはインデント解除が期待どおりに機能しません。 (11568)
* 「変更の追跡」をオンにして行にコンテンツを追加し、「変更の追跡」をオフにしても、実際にはオフにはなりません。 (11567)
* リスト項目をドラッグ&amp;ドロップするのが困難な場合、リスト項目の代わりにテキストが移動します。 (11566)
* 緑色（「変更を追跡」）で表示されている要素のオーサリング時には、トラックの変更が無効になっている場合でも、新しいコンテンツがトラックの変更として表示されます。 (7021)
* カスタムスキーマでコンテンツを読み込むと、ブラウザー（Web エディター）がフリーズする。 (11211)
* ネイティブPDF | 「フォルダープロファイルに追加」オプションを使用して出力プリセットを作成すると、PDFの生成が「ヌルポインター」の例外で失敗します。 (10950)
* ネイティブPDF |画像タグは、すべての画像に display-inline 属性を追加します。 (10653)
* オーディオおよびビデオマルチメディアファイルの挿入が、YouTube形式で **マルチメディアの挿入** アイコン (11320)
* 検証エラーは、特殊なタイトル要素を持つテンプレートを使用してマップを作成した場合に発生します。 (11212)
* Web エディター |トピックの編集中に、XML エディターに改行なしのスペースが追加されます。 (11786)

### 管理

* Web エディター UI の「レポート」タブに、4.2 アップグレード前に作成された古い DITA マップのトピックリストが表示されません。 (11708)

* 4.2 リリースでは、Assets UI の「ファイルをアップロード」ボタン機能が動作しなくなりました。 (11633)


### 公開

* ネイティブPDF | brackets() を含む出力クラスを持つコンテンツを公開すると、公開が停止します。 (11936)
* JSON 出力 |プロパティ値が次の値を持つマップメタデータ `"value in spaces and double quotes"` 公開エラーにつながります。 (11933)
* この問題は、AEMサイト検索で発生します（は 2 ～ 3 レベルのノードを超えては機能しません）。 (11352)
* Web エディター |出力パスとテンプレートをAEMプリセットで選択できません。 (11530)
* 4.1.x から 4.2 リリースにアップグレードすると、ネイティブPDFエンジンは動作せず、サポートされている OS でも NullPointerException をスローします。(11526)
* ダウンロードPDFプロセスが Web エディタで適切に動作していません。 (11496)
* ネイティブPDF |下書きコメントは、生成された出力ではデフォルトで非表示になっています。 (10560)
* ネイティブPDF | navtitle は topichead に対しては無視されます。 (10509)
* ネイティブPDF |追加中 `xref` を画像に設定すると、生成された画像上で画像がレンダリングされません。PDF (11346)
* ネイティブPDF |テーブルヘッダーに存在する脚注は、PDF出力内の対応するページフッターで、太字および中央揃えのテキストになります。 (10610)

### 翻訳

* 4.2 のアップグレード時に、すべての翻訳コンテンツに「Out of Sync」または「Missing Copy」と表示されます。 (11834)

### レビュー

* 完了したレビューは、読み取り専用モードで開きません。 (11387)

