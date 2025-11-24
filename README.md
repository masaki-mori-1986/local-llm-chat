# local-llm-chat

ローカル環境で動作する LLM（例：Ollama + Llama3 など）を用いた **簡易チャットアプリ** の開発プロジェクトです。

このプロジェクトでは、Mac mini 上で動作するローカル LLM をフロントエンド（TypeScript / Node.js）から叩き、  
最終的に「ローカルだけで完結するチャットアプリ」を構築することを目的としています。

---

## 🚀 機能（予定含む）

- ローカル LLM（Ollama API）への問い合わせ
- シンプルな CLI / Web UI チャット
- 会話履歴の管理
- モデル切り替え（llama3:8b など）
- 将来的には：
  - 簡易プロンプト管理
  - LoRA / QLoRA での学習済みモデル利用
  - マルチモーダル対応（必要になれば）

---

## 🧱 開発環境

|項目|内容|
|---|---|
|OS|macOS（M4 Pro）|
|LLM推論エンジン|Ollama|
|言語|TypeScript / Node.js（nvm 管理）|
|エディタ|VSCode + Copilot|
|バージョン管理|GitHub（public repo）|

---

## 📦 事前準備

### 1. Node.js

```bash
nvm install --lts
nvm use --lts
```

### 2. パッケージインストール

```bash
npm install
```

### 3. Prettier（自動フォーマット）

`.prettierrc` は既に含まれています。

---

## 🤖 Ollama（ローカルLLM）

### 1. インストール

```bash
brew install ollama
```

### 2. モデル取得

```bash
ollama run llama3:8b
```

### 3. API が動作しているか確認

```bash
curl http://localhost:11434/api/version
```

---

## 🧪 開発の始め方

```bash
npm run dev
```

（※後で `dev` スクリプトを追加します）

---

## 📁 プロジェクト構成（予定）

```
local-llm-chat/
 ├── src/
 │    ├── main.ts        # エントリポイント
 │    ├── api/           # Ollama API 呼び出し
 │    └── ui/            # CLI or Web UI
 ├── .gitignore
 ├── .prettierrc
 ├── package.json
 └── README.md
```

---

## 📌 今後の予定（メモ）

- Chat UI の実装（CLI → Web）
- モデル切り替え機能
- ログ保存
- LoRA/QLoRA 学習が終わったらモデルを差し替える仕組み作り

---

## 📝 ライセンス

このプロジェクトは個人学習用途のため、ライセンスは未設定（後で必要なら追加）。

