---
title: AEM Guides Editor Configuration
description: AEM Guides用エディターの設定
exl-id: 437d9598-4afc-431f-81bd-6762e22656b7
TQID: https://experienceleague.adobe.com/CI-uq6AoY0Jtdz6LZ4zoWNYmYO1qkRgxiqsGNu7YRds
product_v2:
  - id: fae5e35a-80c9-4b94-9352-1a060a6aab1d
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: cb8c6a2a-3c38-4e40-867c-756f8c36bb0e
subfeature_v2:
  - id: b1ef4d86-3917-4b76-a0bc-4a4771f9b3b0
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 27ffc636d63300fb2e99903d92cab12f0cfcbb25
workflow-type: tm+mt
source-wordcount: 793
ht-degree: 0%

---

# XML エディター設定

制限付き環境で作業する場合は、特定のフォルダープロファイル内でエディター設定をカスタマイズして、作成者が表示できる機能を選択できます。 このフォルダープロファイルを適用すると、エディター自体、CSS テンプレート、利用可能なスニペット、コンテンツバージョンラベルのルック&amp;フィールを変更できます。

このレッスンで使用することを選択できるサンプルファイルは、[xmleditorconfiguration.zip](assets/xmleditorconfiguration.zip)というファイルに用意されています。

>[!VIDEO](https://video.tv.adobe.com/v/342762?quality=12&learn=on)

## デフォルトのエディターUI設定のカスタマイズ

デフォルトのUI設定をいつでもローカルシステムにダウンロードし、任意のテキストエディターで変更し、再度アップロードできます。

1. ナビゲーション画面で、[!UICONTROL **ツール**] アイコンをクリックします。

   ![&#x200B; ツールアイコン &#x200B;](images/reuse/tools-icon.png)

1. 左側のパネルで「**ガイド**」を選択します。

1. 「[!UICONTROL **フォルダープロファイル**]」タイルをクリックします。

   ![&#x200B; フォルダープロファイル &#x200B;](images/reuse/folder-profiles-tile.png)

1. フォルダープロファイルを選択します。

1. 「[!UICONTROL **XML エディター設定**]」タブをクリックします。

1. 「[!UICONTROL **ダウンロード**] デフォルト」をクリックします。

   ![既定をダウンロード &#x200B;](images/lesson-4/download-default.png)

テキストエディターでコンテンツを開いて変更できるようになりました。 _AEM Guides インストールおよび設定_ ガイドには、UI設定の削除、カスタマイズ、または追加の方法のサンプルが含まれています。

## 変更したXML エディター設定のアップロード

UI設定をカスタマイズしたら、アップロードできます。 サンプル設定ファイル _ui-config-restricted-editor.json_&#x200B;には、このレッスンのサポートトピックのセットが含まれています。

1. フォルダープロファイル内で、「[!UICONTROL **XML Editor Configuration**]」タブをクリックします。

1. XML エディター設定で、[!UICONTROL **アップロード**]&#x200B;をクリックします。

   ![アップロード](images/lesson-4/upload.png)

1. 変更したUI設定のファイルをダブルクリックするか、ここに示すように、提供されたサンプルファイルをダブルクリックします。

   ![設定ファイルのサンプル &#x200B;](images/lesson-4/sample-config-file.png)

1. 画面の左上隅にある「[!UICONTROL **保存**]」をクリックします。

変更されたUI設定が正常にアップロードされました。

## CSS テンプレートレイアウトのカスタマイズ

UI設定と同様に、CSS テンプレートレイアウトをダウンロードできます。 テキストエディターで開き、トピックの外観をカスタマイズして変更してからアップロードすることができます。

1. ナビゲーション画面で、[!UICONTROL **ツール**] アイコンをクリックします。

   ![&#x200B; ツールアイコン &#x200B;](images/reuse/tools-icon.png)

1. 左側のパネルで「**ガイド**」を選択します。

1. 「[!UICONTROL **フォルダープロファイル**]」タイルをクリックします。

   ![&#x200B; フォルダープロファイル &#x200B;](images/reuse/folder-profiles-tile.png)

1. フォルダープロファイルを選択します。

1. 「[!UICONTROL **XML エディター設定**]」タブをクリックします。

1. CSS テンプレートレイアウトで、[!UICONTROL **ダウンロード**]&#x200B;をクリックします。

   ![CSSをダウンロード &#x200B;](images/lesson-4/download-css.png)

テキストエディターでCSS コンテンツを変更して保存できるようになりました。

## 変更したCSS テンプレートレイアウトのアップロード

CSS テンプレートレイアウトをカスタマイズしたら、アップロードできます。 サンプルファイル _css-layout-ONLY-draft-comment-change.css_&#x200B;には、このレッスンのサポートトピックのセットが含まれています。 このファイルにはドラフトコメント変更のみが含まれていますが、_css-layout-draft-comment-change.css_&#x200B;はファイル全体で、テストまたはレビューの目的でのみ使用できます。

1. フォルダープロファイル内で、「[!UICONTROL **XML Editor Configuration**]」タブをクリックします。

1. CSS テンプレートレイアウトで、[!UICONTROL **アップロード**]&#x200B;をクリックします。

   ![CSS](images/lesson-4/upload-css.png)をアップロード

1. 独自のカスタム CSS レイアウトまたは提供されたサンプルファイルのファイルをダブルクリックします。

   ![&#x200B; サンプル CSS ファイル &#x200B;](images/lesson-4/sample-css-file.png)

1. 画面の左上隅にある「[!UICONTROL **保存**]」をクリックします。
カスタマイズされたCSS テンプレート レイアウトが正常にアップロードされました。

## XML エディターのスニペットの編集

スニペットとは、製品やグループに特化した、再利用可能なコンテンツのことです。 サンプルスニペットには、このレッスンのサポートファイルが用意されています。

1. ナビゲーション画面で、[!UICONTROL **ツール**] アイコンをクリックします。

   ![&#x200B; ツールアイコン &#x200B;](images/reuse/tools-icon.png)

1. 左側のパネルで「**ガイド**」を選択します。

1. 「[!UICONTROL **フォルダープロファイル**]」タイルをクリックします。

   ![&#x200B; フォルダープロファイル &#x200B;](images/reuse/folder-profiles-tile.png)

1. フォルダープロファイルを選択します。

1. 「[!UICONTROL **XML エディター設定**]」タブをクリックします。

1. 「XML エディターのスニペット」で、「**アップロード**」をクリックします。

   ![&#x200B; スニペットのアップロード &#x200B;](images/lesson-4/upload-snippets.png)

1. 独自のスニペットを選択するか、提供されているサンプルを使用します。

   ![&#x200B; サンプルスニペット &#x200B;](images/lesson-4/sample-snippet.png)

1. 画面の左上隅にある「[!UICONTROL **保存**]」をクリックします。

新しいスニペットがエディターに追加されました。

## XML コンテンツバージョンラベルのカスタマイズ

デフォルトでは、作成者は任意のラベルを作成し、それらをトピックファイルに関連付けることができます。 そのため、同じラベルでもバリエーションが異なる場合があります。 ラベルに一貫性がないようにするには、定義済みのラベルのリストから選択することもできます。

1. ナビゲーション画面で、[!UICONTROL **ツール**] アイコンをクリックします。

   ![&#x200B; ツールアイコン &#x200B;](images/reuse/tools-icon.png)

1. 左側のパネルで「**ガイド**」を選択します。

1. 「[!UICONTROL **フォルダープロファイル**]」タイルをクリックします。

   ![&#x200B; フォルダープロファイル &#x200B;](images/reuse/folder-profiles-tile.png)

1. フォルダープロファイルを選択します。

1. 「[!UICONTROL **XML エディター設定**]」タブをクリックします。

1. 「XML コンテンツバージョンラベル」で、「[!UICONTROL **ダウンロード**]」をクリックします。

   ![&#x200B; ラベルのダウンロード &#x200B;](images/lesson-4/download-labels.png)

これで、必要に応じてラベルをカスタマイズする準備が整いました。

## XML コンテンツバージョンラベルのアップロード

ラベルをダウンロードして変更したら、XML コンテンツバージョンラベルのトピックをアップロードできます。 このレッスンのサポートトピックのセットが含まれているサンプルファイル _labels.json_&#x200B;を使用できます。

1. フォルダープロファイル内で、「[!UICONTROL **XML Editor Configuration**]」タブをクリックします。

1. 「XML コンテンツバージョンラベル」で、「[!UICONTROL **アップロード**]」をクリックします。

   ![&#x200B; ラベルをアップロード &#x200B;](images/lesson-4/upload-labels.png)

1. 独自のカスタムラベルまたは提供されたサンプルファイルのファイルをダブルクリックします。

   ![&#x200B; サンプルラベルファイル &#x200B;](images/lesson-4/sample-labels-file.png)

1. 画面の左上隅にある「[!UICONTROL **保存**]」をクリックします。

カスタム XML コンテンツ バージョン ラベルが正常にアップロードされました。
