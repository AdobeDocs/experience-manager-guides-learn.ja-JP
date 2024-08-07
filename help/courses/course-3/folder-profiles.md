---
title: フォルダープロファイル
description: AEM Guidesのフォルダープロファイルの作成と使用
exl-id: 5a0daa68-51ae-42d0-8320-6e8bdb1fe545
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 1%

---

# フォルダープロファイル

AEMから設定ツールにすばやくアクセスできます。 フォルダープロファイルをカスタマイズすることで、異なる部門や製品に一意のテンプレート、オーサリング環境、条件付き属性プロファイル、スニペットを設定したり、web エディター設定を設定したりできます。

このレッスンで使用するサンプル ファイルは、ファイル [folderprofiles.zip](assets/folderprofiles.zip) に用意されています。

>[!VIDEO](https://video.tv.adobe.com/v/342758?quality=12&learn=on)

## フォルダープロファイルへのアクセス

設定は、フォルダープロファイル アイコンで管理します。

1. ナビゲーション画面で、「[!UICONTROL **ツール**]」アイコンをクリックします。

   ![ ツールアイコン ](images/reuse/tools-icon.png)

1. 左側のパネルで「**ガイド**」を選択します。

1. [!UICONTROL **フォルダープロファイル**] タイルをクリックします。

   ![ フォルダープロファイル ](images/reuse/folder-profiles-tile.png)

1. 目的のプロファイルを選択します。 例えば、デフォルトプロファイルである「**グローバルプロファイル**」を選択します。

   ![ グローバルプロファイル ](images/lesson-3/global-profile-tile.png)

## グローバルプロファイルでの条件属性の編集

グローバルプロファイルにアクセスしたら、その設定を編集できます。 特に指定のない限り、グローバルプロファイル設定はすべてのユーザーに適用されます。

1. グローバルプロファイルで、「**条件属性**」タブを選択します。

1. 画面の左上隅にある「[!UICONTROL **編集**]」をクリックします。

   ![ 条件属性 ](images/lesson-3/edit-conditional-attributes.png)

1. 「[!UICONTROL **追加**]」をクリックします。

1. 新しい条件の **名前**、**値** および **ラベル** フィールドに値を入力します。

   ![ 新規条件 ](images/lesson-3/new-condition.png)

1. 画面の左上隅にある「[!UICONTROL **保存**]」をクリックします。
すべてのユーザーが新しい条件を使用できるようになりました。 コンテンツのプロパティパネルで選択し、必要に応じてコンテンツに適用できます。

## 新規フォルダープロファイルの作成

デフォルトのグローバルプロファイルに加えて、独自のカスタムプロファイルを作成できます。

1. ナビゲーション画面で、「[!UICONTROL **ツール**]」アイコンをクリックします。

   ![ ツールアイコン ](images/reuse/tools-icon.png)

1. 左側のパネルで「**ガイド**」を選択します。

1. [!UICONTROL **フォルダープロファイル**] タイルをクリックします。

   ![ フォルダープロファイル ](images/reuse/folder-profiles-tile.png)

1. 「[!UICONTROL **作成**]」をクリックします。

1. フォルダープロファイルを作成ダイアログで、次の手順を実行します。

   a. プロファイルに名前を付けます。

   b. パスを指定します。

   c. 「[!UICONTROL **作成**]」をクリックします。

   ![ フォルダープロファイルの作成 ](images/lesson-3/create-folder-profile.png)

新しいプロファイル名を含んだタイルがフォルダープロファイル ページに表示されます。

## 「一般」タブからの管理者ユーザーの追加

管理者ユーザーには、フォルダープロファイルの条件属性、オーサリングテンプレートおよび出力プリセットを更新する権限があります。

1. タイルをクリックして、目的のフォルダープロファイルを開きます。

   ![ フォルダープロファイルを編集 ](images/lesson-3/edit-folder-profile.png)

1. 「**一般**」タブを選択します。

1. 画面の左上にある「[!UICONTROL **編集**]」をクリックします。

1. 「管理者ユーザー」で、ドロップダウンからユーザーを選択するか、ユーザー名を入力します。

1. 「[!UICONTROL **追加**]」をクリックします。

   必要に応じて、複数の管理者ユーザーを追加できます。

   ![ 管理者を追加 ](images/lesson-3/add-admin.png)

1. すべてのユーザーを追加したら、画面の右上隅にある「[!UICONTROL **保存**]」をクリックします。

これで、このプロファイルに管理者ユーザーが割り当てられました。

## 「条件属性」タブから新しいオーディエンスを追加します

グローバルプロファイルにアクセスしたら、その設定を編集できます。 特に指定のない限り、グローバルプロファイル設定はすべてのユーザーに適用されます。

1. 目的のフォルダープロファイル内から、「**条件属性**」タブを選択します。

1. 画面の左上隅にある「[!UICONTROL **編集**]」をクリックします。

   ![ 条件属性の編集 2](images/lesson-3/edit-conditional-attributes-2.png)

1. 「[!UICONTROL **追加**]」をクリックします。

1. 新しい条件の **名前**、**値** および **ラベル** フィールドに値を入力します。

   [!UICONTROL **プラス**] 記号をクリックすると、名前付き属性に値とラベルのペアを追加できます。

   ![ 条件を追加 ](images/lesson-3/add-conditions.png)

1. 画面の左上隅にある「[!UICONTROL **保存**]」をクリックします。

新しい条件付き属性がこのプロファイルに追加されました。

## 「オーサリングテンプレート」タブからテンプレートとマップを選択します

AEM Guidesには、すぐに使用できるオーサリングテンプレートとマップが付属しています。 特定の作成者に制限できます。 デフォルトでは、テンプレートは DITA テンプレートフォルダ内のAssetsの場所に保存されます。

1. 目的のフォルダープロファイル内から、「オーサリングテンプレート」タブを選択します。

1. 画面の左上隅にある「編集」をクリックします。

1. マップ テンプレートを追加します。

   a. 「**マップテンプレート**」ドロップダウンで、使用可能なマップからオプションを選択します。

   b. 「[!UICONTROL **追加**]」をクリックします。

   ![ マップ テンプレート ](images/lesson-3/map-templates.png)

1. トピック テンプレートを追加します。

   a. **トピックテンプレート** ドロップダウンで、使用可能なテンプレートからオプションを選択します。

   ![ トピック テンプレート ](images/lesson-3/topic-templates.png)

1. 「[!UICONTROL **追加**]」をクリックします。

1. 必要に応じて、トピック テンプレートを追加します。

1. 終了したら、画面の左上にある [!UICONTROL **保存**] をクリックします。

新しいオーサリングテンプレートがこのプロファイルに追加されました。

## 「出力プリセット」タブからの不要なプリセットの削除

フォルダープロファイルに基づいて各出力プリセットを設定できます。 不要な出力プリセットは削除する必要があります。

1. 目的のフォルダープロファイル内から、「**出力プリセット**」タブを選択します。

1. 左側のパネルで、不要なプリセットのチェックボックスをオンにします。

   ![ プリセットを削除 ](images/lesson-3/delete-presets.png)

1. 画面の左上隅にある [!UICONTROL **プリセットを削除**] をクリックします。

1. プリセットを削除ダイアログで、「[!UICONTROL **削除**]」をクリックします。

   ![削除](images/lesson-3/delete.png)

使用するプリセットは、表示される出力プリセットのみです。

## XML エディターの「設定」タブからスニペットをアップロード

1. 目的のフォルダープロファイル内から、「**XML エディター設定**」タブを選択します。

1. 「XML エディタースニペット」の下の「[!UICONTROL **アップロード**]」をクリックします。

   ![ スニペットのアップロード ](images/lesson-3/upload-snippet.png)

1. 以前に作成したスニペットに移動します。

1. 「[!UICONTROL **開く**]」をクリックします。

1. 画面の左上にある「[!UICONTROL **保存**]」をクリックします。

エディターの構成がスニペットを含むように正常に変更されました。

## リポジトリでのフォルダープロファイルの指定

エディターで、フォルダープロファイルに加えた変更の結果を確認できます。

1. **リポジトリ表示** に移動します。

1. 使用するコンテンツのフォルダーをクリックします。

1. 上部ツールバーの [!UICONTROL **ユーザー環境設定**] アイコンをクリックします。

   ![ ユーザー環境設定 ](images/lesson-3/hr-user-prefs.png)

1. ユーザーの環境設定ダイアログで、目的のフォルダープロファイルをドロップダウンから選択します。

   ![ ユーザー環境設定の選択 ](images/lesson-3/select-user-pref.png)

1. 「[!UICONTROL **保存**]」をクリックします。

コンテンツにフォルダープロファイルを適用している。 新しい DITA トピックを作成すると、フォルダプロファイルに基づいたトピックタイプの制限リストが表示されます。 オーディエンス条件には、グローバル設定に加え、フォルダープロファイルに固有の設定が含まれます。 アップロードしたスニペット ファイルにより、選択できる既定のスニペットのセットが作成されました。 マップダッシュボードに、制限された出力プリセットが表示されます。
