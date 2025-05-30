---
title: AEM Guides エディターの設定
description: AEM Guides用のエディターの設定
exl-id: 437d9598-4afc-431f-81bd-6762e22656b7
source-git-commit: 988c288fc03e509a3a55e87b1e1ecd8fd07d1c92
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# XML エディターの設定

制限のある環境で作業する場合は、特定のフォルダープロファイル内でエディター設定をカスタマイズすることで、作成者が表示できる機能を選択できます。 このフォルダープロファイルを適用すると、エディター自体のルックアンドフィール、CSS テンプレート、使用可能なスニペットおよびコンテンツバージョンラベルを変更できます。

このレッスンで使用するサンプル ファイルは、ファイル [xmleditorconfiguration.zip](assets/xmleditorconfiguration.zip) にあります。

>[!VIDEO](https://video.tv.adobe.com/v/342762?quality=12&learn=on)

## デフォルトのエディター UI 設定のカスタマイズ

いつでも、デフォルトの UI 設定をローカルシステムにダウンロードし、任意のテキストエディターで変更して、再度アップロードできます。

1. ナビゲーション画面で、「[!UICONTROL **ツール**]」アイコンをクリックします。

   ![ ツールアイコン ](images/reuse/tools-icon.png)

1. 左側のパネルで「**ガイド**」を選択します。

1. [!UICONTROL **フォルダープロファイル**] タイルをクリックします。

   ![ フォルダープロファイル ](images/reuse/folder-profiles-tile.png)

1. フォルダープロファイルを選択します。

1. 「[!UICONTROL **XML エディター設定**]」タブをクリックします。

1. [!UICONTROL **ダウンロード**] デフォルトをクリックします。

   ![Download Default](images/lesson-4/download-default.png)

これで、テキストエディターでコンテンツを開いて変更できるようになりました。 _AEM Guides インストールおよび設定_ ガイドには、UI 設定に対する関数の削除、カスタマイズ、追加方法のサンプルが含まれています。

## 変更した XML エディター設定をアップロード

UI 設定をカスタマイズしたら、アップロードできます。 サンプルの設定ファイル _ui-config-restricted-editor.json_ は、このレッスンのサポート トピックのセットとともに提供されています。

1. フォルダープロファイル内で、「[!UICONTROL **XML エディター設定**]」タブをクリックします。

1. 「XML エディター設定」で、「[!UICONTROL **アップロード**]」をクリックします。

   ![アップロード](images/lesson-4/upload.png)

1. 変更した UI 設定のファイル、または以下に示すように、提供されたサンプルファイルをダブルクリックします。

   ![ サンプル設定ファイル ](images/lesson-4/sample-config-file.png)

1. 画面の左上隅にある「[!UICONTROL **保存**]」をクリックします。

変更された UI 設定が正常にアップロードされました。

## CSS テンプレートレイアウトのカスタマイズ

UI 設定と同様に、CSS テンプレートレイアウトをダウンロードできます。 これをテキストエディターで開き、変更を加えて、アップロード前にトピックのルックアンドフィールをカスタマイズできます。

1. ナビゲーション画面で、「[!UICONTROL **ツール**]」アイコンをクリックします。

   ![ ツールアイコン ](images/reuse/tools-icon.png)

1. 左側のパネルで「**ガイド**」を選択します。

1. [!UICONTROL **フォルダープロファイル**] タイルをクリックします。

   ![ フォルダープロファイル ](images/reuse/folder-profiles-tile.png)

1. フォルダープロファイルを選択します。

1. 「[!UICONTROL **XML エディター設定**]」タブをクリックします。

1. 「CSS テンプレートレイアウト」で、「[!UICONTROL **ダウンロード**]」をクリックします。

   ![CSS をダウンロード ](images/lesson-4/download-css.png)

CSS コンテンツをテキストエディターで変更して保存できるようになりました。

## 変更した CSS テンプレートレイアウトのアップロード

CSS テンプレートレイアウトをカスタマイズしたら、アップロードできます。 サンプルファイル _css-layout-ONLY-draft-comment-change.css_ には、このレッスンでサポートされる一連のトピックが含まれています。 このファイルには下書きコメントの変更のみが含まれていますが、_css-layout-draft-comment-change.css_ はファイル全体であり、テストやレビューの目的でのみ使用できます。

1. フォルダープロファイル内で、「[!UICONTROL **XML エディター設定**]」タブをクリックします。

1. 「CSS テンプレートレイアウト」で、「[!UICONTROL **アップロード**]」をクリックします。

   ![CSS をアップロード ](images/lesson-4/upload-css.png)

1. 独自のカスタム CSS レイアウトまたは提供されたサンプルファイルのファイルをダブルクリックします。

   ![ サンプル CSS ファイル ](images/lesson-4/sample-css-file.png)

1. 画面の左上隅にある「[!UICONTROL **保存**]」をクリックします。
カスタマイズされた CSS テンプレートレイアウトが正常にアップロードされました。

## XML エディタースニペットの編集

スニペットは、製品またはグループに固有の、再利用可能なコンテンツです。 このレッスンのサポート ファイルには、サンプル スニペットが用意されています。

1. ナビゲーション画面で、「[!UICONTROL **ツール**]」アイコンをクリックします。

   ![ ツールアイコン ](images/reuse/tools-icon.png)

1. 左側のパネルで「**ガイド**」を選択します。

1. [!UICONTROL **フォルダープロファイル**] タイルをクリックします。

   ![ フォルダープロファイル ](images/reuse/folder-profiles-tile.png)

1. フォルダープロファイルを選択します。

1. 「[!UICONTROL **XML エディター設定**]」タブをクリックします。

1. 「XML エディタースニペット」の下の「**アップロード**」をクリックします。

   ![ スニペットのアップロード ](images/lesson-4/upload-snippets.png)

1. 独自のスニペットを選択するか、提供されているサンプルを使用します。

   ![ サンプルスニペット ](images/lesson-4/sample-snippet.png)

1. 画面の左上隅にある「[!UICONTROL **保存**]」をクリックします。

エディターに新しいスニペットが正常に追加されました。

## XML コンテンツバージョンラベルのカスタマイズ

デフォルトでは、作成者は任意のラベルを作成し、それらをトピックファイルに関連付けることができます。 これにより、同じラベルでも異なるバリエーションが生じる可能性があります。 ラベルの一貫性を保つために、定義済みのラベルのリストから選択することもできます。

1. ナビゲーション画面で、「[!UICONTROL **ツール**]」アイコンをクリックします。

   ![ ツールアイコン ](images/reuse/tools-icon.png)

1. 左側のパネルで「**ガイド**」を選択します。

1. [!UICONTROL **フォルダープロファイル**] タイルをクリックします。

   ![ フォルダープロファイル ](images/reuse/folder-profiles-tile.png)

1. フォルダープロファイルを選択します。

1. 「[!UICONTROL **XML エディター設定**]」タブをクリックします。

1. [XML コンテンツ バージョン ラベル ] で、[[!UICONTROL **ダウンロード**]] をクリックします。

   ![ ラベルをダウンロード ](images/lesson-4/download-labels.png)

これで、必要に応じてラベルをカスタマイズできるようになりました。

## XML コンテンツバージョンラベルのアップロード

ラベルをダウンロードして変更したら、XML コンテンツバージョンラベルトピックをアップロードできます。 このレッスンのサポート トピックのセットに含まれているサンプル ファイル _labels.json_ を使用することもできます。

1. フォルダープロファイル内で、「[!UICONTROL **XML エディター設定**]」タブをクリックします。

1. 「XML コンテンツバージョンラベル」で、「[!UICONTROL **アップロード**]」をクリックします。

   ![ ラベルをアップロード ](images/lesson-4/upload-labels.png)

1. 独自のカスタムラベルのファイルまたは提供されたサンプルファイル（ここでは）をダブルクリックします。

   ![ サンプルラベルファイル ](images/lesson-4/sample-labels-file.png)

1. 画面の左上隅にある「[!UICONTROL **保存**]」をクリックします。

カスタム XML コンテンツ バージョン ラベルが正常にアップロードされました。
