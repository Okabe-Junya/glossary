---
title: カオスエンジニアリング
status: Completed
category: コンセプト
tags: ["方法論", "", ""]
---

カオスエンジニアリング(CE)とは、本番環境の[分散システム](/ja/distributed-systems/)に実験する学問分野です。
分散システムが乱雑で予期せぬ状況に耐えるシステムの能力に対する信頼を築くことを目指します。

## 解決すべき問題はなんですか

[SRE](/ja/site-reliability-engineering/)や[DevOps](/ja/devops/)の実践は、プロダクトの回復力と[信頼性](/ja/reliability/)を高める技術に焦点を当てています。
システムが障害を許容しつつ適切なサービス品質を保証する能力は、通常のソフトウェア開発の要件です。
インフラストラクチャ、プラットフォーム、あるいは([マイクロサービス](/ja/microservices-architecture/)ベースの)アプリケーションの他の動作部分のように、アプリケーションの停止につながる可能性のある複数の側面が関与しています。
本番環境に新機能を高頻度でデプロイすることは、高い確率でダウンタイムと重大なインシデントをもたらし、ビジネスに重大な影響を及ぼす可能性があります。

## どのように役に立つのでしょうか

カオスエンジニアリングは、回復力の要件を満たすための技術です。
インフラストラクチャ、プラットフォーム、そしてアプリケーションの障害に対する回復力を達成するために使用されます。
カオスエンジニアは、アプリケーション、インフラストラクチャ、あるいはプラットフォームが自己修復でき障害が顧客に目立った影響を与えないことを検証するために、プロアクティブにランダムな障害を注入するカオス実験を行います。
カオス実験の目的は、盲点(例えば、モニタリングや自動スケーリング技術)を発見し、重大なインシデントの最中にチーム間のコミュニケーションを改善することです。
このアプローチは、特に本番環境において、複雑なシステムにおける回復力とチームの自信を高めるのに役立ちます。
