# RaiaEngineドキュメント

これはRaiaEngineのドキュメントです。

### このドキュメントについて

RaiaEngineに関する包括的な解説を記述することを目的としています。

### RaiaEngineとは

RaiaEngineはクロスプラットフォームで動作するスクリプトベースのゲームエンジンです。

### 対応するプラットフォーム

- Windows
- macOS

### RaiaEngineの技術基盤

スクリプト言語には組み込み可能なECMAScriptエンジンであるDuktapeを採用しています。DukutapeはES5.0/ES5.1に準拠しているので、使い慣れたJavaScriptのコードやTypeScriptからトランスコンパイルしたコードをそのまま使用することができます。

描画処理にはGoogleの開発したANGLEを採用しており、各プラットフォームに最適なグラフィックAPIが呼び出されます。例えばWindowsであればDirectX、macOSであればMetalAPIが選ばれます。ANGLEはGpenGLES互換レイヤーでもあるため、GpenGLESを利用するウェブやモバイルへの移植も容易になっています。

RaiaEngineはC言語で記述されており、C/C++による拡張が