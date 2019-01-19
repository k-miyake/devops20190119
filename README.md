# Azure DevOps Live 20190119 チェックリスト

## リファレンス

- [ ]  公式ドキュメントのConceptは一読の価値あり

## プロジェクトの開始

- 組織の作成
  - [ ] AAD認証では、サインインしているアカウント + ディレクトリで Organization が決まる
  - [ ] Azureポータルから、DevOpsプロジェクトが作成できなくなった
  - [ ] [Visual Studio Profile](https://app.vsaex.visualstudio.com/profile/view) でディレクトリが選択できる
- プロジェクトの作成
  - [ ] 作成時にAdvance設定で Agile か Scrum を選択する
- サブスクリプションとの紐付け
  - [ ] evOpsの課金をAzureの費用とまとめられる -> Azure Portalで紐付け

## アジャイルなプロジェクト運営

- かんばん
  - [ ] Boards は Story レベルなので、実際あまり使わない
  - [ ] 日々のタスク管理は Sprints
  - [ ] QueriesでIssue Listを作っておくとシンプルな課題管理ができる
- スプリント計画立案
  - [ ] 設定からイテレーションを設定しておく（ハマりポイント）
  - [ ] Backlogs でスプリント計画をシミュレーションできる

## Reposでのライブコミュニケーション

- リポジトリの作成
  - [ ] デフォルトは消す
  - [ ] 1プロジェクトで複数リポジトリも作成できる
  - [ ] masterにはブランチポリシーを設定しておく
- 開発ワークフロー
  - [ ] ブランチやPRの作成はTaskから
  - [ ] PRをDRAFTで作成してディスカッションできるように
  - [ ] コメントはMarkdown, 更新はほぼリアルタイムに反映
  - [ ] PRでは、細かい課題管理ができる（ポリシーでチェックも可能）
  - [ ] Set Auto-CompleteでPRを最終的に発行する
- GitKrakenから使う

## Piplineでのビルド&リリース

- デプロイはリリースで行う
  - [ ] デプロイは Builds ではなく Releases で
  - [ ] Releases では 環境（DevとProduction等）にStageを分ける
- Azureとの接続
  - [ ] Service Connectionの設定をAzureの権限がある人に依頼しておく
- YAMLビルド
  - ビルドタスクが安定してきたら、YAMLに変換する
- 拡張機能 [Azure Cosmos DB Emulator (public preview) - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=azure-cosmosdb.emulator-public-preview&targetId=cfb04ec5-76ac-471b-b1df-538f1588df16&utm_source=vstsproduct&utm_medium=ExtHubManageList)

## プロダクトドキュメントとしてのWiki

- [ ] プロジェクト実施中のメモは通常のWikiを使う
- [ ] プロダクトのDocsはReposのドキュメントディレクトリを指定する
- https://docs.microsoft.com/en-us/azure/devops/project/wiki/provisioned-vs-published-wiki?view=vsts

## プロジェクトの完了（納品）

- Organization Settings でオーナーを変更し、利用ユーザーや権限を変更して完了
- 必要に応じてサブスクリプションの付け替えも
