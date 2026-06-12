---
title: 条件を使用した公開
description: Adobe Experience Manager Guidesを使用した条件を使用した公開
exl-id: ea94824a-884b-447f-9562-e6c629b8133b
TQID: https://experienceleague.adobe.com/Ez-rAJNfPH-Dd2lTd65B1bct4lkhoB2Gi6IKc8-A8gI
product_v2: id: fae5e35a-80c9-4b94-9352-1a060a6aab1did: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a3bd6397-2eb2-4908-a61c-226e26855dca
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 27ffc636d63300fb2e99903d92cab12f0cfcbb25
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 4%

---

# 条件を使用した公開

条件付き公開機能により、1つのコンテンツソースを、1つ以上のオーディエンス、製品、プラットフォーム向けに作成することができます。 この情報は動的に公開でき、特に必要なコンテンツのみが出力に含まれます。

>[!VIDEO](https://video.tv.adobe.com/v/339041?quality=12&learn=on)

## 演習の準備

練習用のサンプルファイルはここからダウンロードできます。

[Exercise-Download](assets/exercises/publishing-with-conditions.zip)

## 条件付き属性を使用したコンテンツのマークアップ

1. 変更するトピックを開きます。

1. コンディショナルになるテキストを入力します。 例えば、1つ以上の段落、表全体、図、その他のコンテンツなどです。

   ![ プレゼンテーション情報](images/presenting-info.png)

1. 条件付き属性を割り当てる特定のコンテンツを選択します。 例えば、ソース内の1つの段落です。

   ![Template-Choice](images/template-choice.png)

1. 右側のレールにプロパティが表示されていることを確認します。

1. オーディエンス、製品、プラットフォームの属性を追加します。

1. 属性に値を割り当てます。 コンディショナルマークアップを表示するコンテンツ表示の更新が適用されました。

   ![ テンプレートを指定](images/specify-template.png)

## 条件付きコンテンツのプレビュー

1. **プレビュー**&#x200B;をクリックします。

1. **フィルター**&#x200B;で、表示または非表示にする条件を選択または選択解除します。

1. **条件テキストをハイライト表示**&#x200B;または選択解除します。

   ![Preview-Conditional-Content](images/preview-conditional-content.png)

## 条件プリセットの作成

コンディションプリセットは、出力の生成時に含める、除外する、またはマークアップするプロパティを定義するプロパティのコレクションです。

1. マップダッシュボードから「**条件プリセット**」タブを選択します。

1. 「**作成**」をクリックします。

1. **追加** （または&#x200B;**すべて追加**）を選択します。

1. 条件に名前を付けます。

1. 属性、ラベル、アクションの組み合わせを選択します。

   ![Create-Condition-Preset](images/create-condition-preset.png)

1. 必要に応じて繰り返します。

1. 「**保存**」をクリックします。

## 条件付き出力の生成

コンテンツに条件を適用すると、出力として生成できます。 これには、条件プリセットまたはDITAval ファイルを使用できます。

## 条件プリセットを使用した条件付き出力の生成

1. 「**出力プリセット**」タブを選択します。

1. 出力プリセットを選択します。

1. 「**編集**」をクリックします。

1. **条件を適用**&#x200B;で、条件プリセットを選択します。

   ![Generate-Conditional-Output](images/generate-conditional-output.png)

1. 「**完了**」をクリックします。

1. 出力プリセットを生成し、コンテンツを確認します。

## DITAval ファイルを使用した条件付き出力の生成

DITAval ファイルを使用して、条件付きコンテンツを公開できます。 これには、ファイルを作成またはアップロードしてから、公開時に参照する必要があります。

1. 「**出力プリセット**」タブを選択します。

1. 出力プリセットを選択します。

1. 「**編集**」をクリックします。

1. 「条件を適用」で、DITAval ファイルを選択します。

   ![Generate-Using-DITAval](images/generate-using-ditaval.png)

1. 「**完了**」をクリックします。

1. 出力プリセットを生成し、コンテンツを確認します。
