---
title: Pod
status: Completed
category: コンセプト
tags: ["インフラストラクチャ", "基礎", ""]
---

[Kubernetes](/ja/kubernetes/)環境の中では、Podは最も基本的なデプロイ可能ユニットとして機能します。
これはコンテナ化されたアプリケーションをデプロイし、管理するための基本的な構成要素を表しています。
各Podには単一のアプリケーションインスタンスが含まれ、一つ以上の[コンテナ](/ja/container/)を保持することができます。
Kubernetesは、より大規模なDeploymentの一部としてPodを管理し、必要に応じてPodを[垂直スケーリング](/ja/vertical-scaling/)または[水平スケーリング](/ja/horizontal-scaling/)することができます。

## 解決すべき問題はなんですか

コンテナは一般的に、特定のワークロードを実行し制御する独立した単位として機能しますが、コンテナが密接に相互作用し、適切に連携して制御される必要がある場合もあります。

これらの密接に関連するコンテナがそれぞれ個別に管理される場合、冗長な管理作業が発生します。
たとえば、オペレーターは関連するコンテナの配置を繰り返し判断し、それらが一緒に保たれるようにしなければなりません。
また、これらの関連するコンテナのライフサイクルは同期される必要がありますが、個別にしか管理できません。

## どのように役に立つのでしょうか

Podは密接に関連するコンテナを単一のユニットにまとめることで、コンテナ操作を大幅に簡素化します。
たとえば、補助的なコンテナは、追加機能を提供したり、グローバルな設定を行うために主コンテナと一緒に使用されることがよくあります。
これには、基本設定を主コンテナに注入して適用するコンテナ、 _sidecar_ (コンテナ)であり、主コンテナのためのネットワークトラフィックルーティングを処理する([サービスメッシュ](/ja/service-mesh/)を参照)、あるいは各コンテナと連動してログを収集するコンテナなどが含まれます。

メモリとCPUの割り当ては、Podレベルで定義することも、コンテナごとに定義することもできます。
Podレベルで定義すると、内部のコンテナがリソースを柔軟に共有できます。
