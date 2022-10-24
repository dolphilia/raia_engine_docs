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

スクリプト言語には組み込み可能な[ECMAScript](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/)エンジンである[Duktape](https://duktape.org)を採用しています。Dukutapeは[ES5.0](https://www.ecma-international.org/wp-content/uploads/ECMA-262_5th_edition_december_2009.pdf)/[ES5.1](https://note.affi-sapo-sv.com/js-ecmascript-link.php)に準拠しているので、使い慣れたJavaScriptのコードや[TypeScript](https://www.typescriptlang.org)からトランスコンパイルしたコードをそのまま使用することができます。

描画処理にはGoogleの開発した[ANGLE](https://chromium.googlesource.com/angle/angle/+/main/README.md)を採用しており、各プラットフォームに最適なグラフィックAPIが呼び出されます。例えばWindowsであれば[DirectX](https://learn.microsoft.com/ja-jp/windows/win32/directx)、macOSであれば[MetalAPI](https://developer.apple.com/documentation/metal/)が選ばれます。ANGLEはGpenGLES互換レイヤーでもあるため、[GpenGLES](https://www.khronos.org/opengles/)を利用するウェブやモバイルへの移植も容易になっています。

RaiaEngineはC言語で記述されており、C/C++による拡張が