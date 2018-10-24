---



copyright:
  years: 2017
lastupdated: "2017-08-10"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# カスタム・セキュリティー・グループの作成と管理
このチュートリアルでは、カスタム・セキュリティー・グループの作成、インスタンス割り当て、編集の方法を説明します。 

![カスタム・セキュリティー・グループ](./images/goal.jpg)

## 必要なもの
この例には、次のオブジェクトおよび項目が使用されます。

| リソース名  | オペレーティング・システム | タイプ | ロケーション/DC | IP/サブネット |
|:------------- |:---------------:| -------------:| :---------------:| ---------------:|
| 適用外/任意 | 10.0.0.0/16 |
| allow_icmp | 適用外  | セキュリティー・グループ | 適用外/任意 | 0.0.0.0/0 |
| allow_ssh | 適用外  | セキュリティー・グループ | 適用外/任意 | 0.0.0.0/0 |
|jpmongevsi2.testing.com | Ubuntu 16.04 | 仮想サーバー・インスタンス | ダラス 10 ポッド 01 | 10.0.0.21 |	
|jpmongevsi4.testing.com | Ubuntu 16.04 | 仮想サーバー・インスタンス |	ダラス 10 ポッド 01	| 10.0.2.219 |


このチュートリアルでは、CPA プライベート・ネットワーク/アカウントを使用しますが、実際上、セキュリティー・グループは CPA アカウントとレギュラー・アカウントのどちらでも同じように動作します。サブネット 10.0.0.0/24 と 10.0.2.0/24 は、同一の CPA プライベート・ネットワークに属します。これは、複数の VSI が同一のプライベート・サブネット/VLAN に接続されたレギュラー・アカウントを持つことと同じになります。


## 実行できるタスク

このチュートリアルでは、以下を行う方法を説明します。

タスク  | 説明
------------- | -------------
[セキュリティー・グループの作成](csg_create.html) |IBM クラウド・プラットフォームで事前定義されたセキュリティー・グループを使用するのではなく、カスタム・セキュリティー・グループを作成して構成します。
[ルールの作成](csg_rule.html)  |入力要求 (SSH および ICMP) とその関連の (出力) トラフィック・フローを許可するルールを作成します。
[セキュリティー・グループへのインスタンスの割り当て](csg_assign_instances.html) | セキュリティー・メニューまたはデバイス・メニューを使用して、セキュリティー・グループ・オブジェクトをインスタンスに割り当てます。
[セキュリティー・グループとそのルールの編集](csg_edit.html) | セキュリティー・オブジェクトのパラメーターとそのルールを変更します。