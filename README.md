# Mastra クイックスタートサンプル

このプロジェクトは、Mastraフレームワークを使った簡単なAIエージェントアプリケーションのサンプルです。

## プロジェクトの概要

Mastraは、AIアプリケーションを構築するためのTypeScriptフレームワークです。このサンプルでは、基本的なAIエージェントを設定し、メモリ機能（メッセージ履歴）を持たせています。

### 主な機能

- 基本的なAIエージェント（myAgent）の実装
- libSQLを使用したメモリストレージ
- Langfuseによるテレメトリ（AIの動作追跡）

## 始め方

### 前提条件

- Node.js v20.9.0以上
- npm または pnpm

### インストール

```bash
# 依存関係のインストール
npm install
# または
pnpm install
```

### 環境変数の設定

必要に応じて以下の環境変数を設定してください：

```
LANGFUSE_PUBLIC_KEY=your_langfuse_public_key
LANGFUSE_SECRET_KEY=your_langfuse_secret_key
LANGFUSE_BASEURL=your_langfuse_baseurl
```
参考：https://langfuse.com/docs/get-started

### 開発サーバーの起動

```bash
npm run dev
# または
pnpm dev
```

これにより、Mastraの開発環境が起動し、ブラウザでエージェントとチャットできるようになります。

## プロジェクト構造

```
src/
  mastra/
    agents/
      my-agent.ts    # AIエージェントの定義
    tools/           # エージェントが使用するツール（関数）を定義
    index.ts         # Mastraのメイン設定
```

## カスタマイズ方法

1. エージェントの指示を変更する：
   `src/mastra/agents/my-agent.ts` の `instructions` を編集してエージェントの動作を調整できます。

2. 異なるAIモデルを使用する：
   `model: openai("gpt-4o-mini")` の部分を変更して、他のモデルを使用できます。

3. ツールの追加：
   `src/mastra/tools` ディレクトリにツール（関数）を追加し、エージェントに新しい機能を持たせることができます。

## 詳細情報

Mastraの詳細については、[公式ドキュメント](https://mastra.ai/ja/docs)を参照してください。 