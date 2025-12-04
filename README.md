# Claude Code Skills for Nuxt4 Development

Claude Code Skillsのサンプルリポジトリです。

## 概要

このリポジトリには、Nuxt4プロジェクト開発を効率化するためのClaude Code Skillsが含まれています。各スキルは、プロジェクト固有のコーディング規約やパターンをClaude Codeに教え、一貫性のあるコード生成を実現します。

## Skills一覧

### 1. nuxt4-components

Atomic Designパターンに基づくVueコンポーネントの生成スキル。

**機能:**
- Ha (Atom) / Hm (Molecule) / Ho (Organism) / Ht (Template) 階層に対応
- i18n多言語対応（日本語/英語）
- TypeScript型定義
- Scoped SCSS styling

**使用例:**
```
/skill nuxt4-components
```

### 2. nuxt4-composables

レイヤードアーキテクチャに基づくComposablesの生成スキル。

**機能:**
- UI層 / Form層 / Root層の3層構造
- InjectionKeyとprovide/injectパターン
- Repository Factory統合
- vee-validate + zodによるバリデーション

**使用例:**
```
/skill nuxt4-composables
```

### 3. nuxt4-models

Zodスキーマを使用した型安全なModel定義の生成スキル。

**機能:**
- 定数（Enum）定義パターン
- Zodオブジェクトスキーマ
- OpenAPI型拡張
- ヘルパー関数（変換、ファクトリー、フィルタリング）

**使用例:**
```
/skill nuxt4-models
```

### 4. nuxt4-pages

標準化されたページコンポーネントの生成スキル。

**機能:**
- Simple / List / Detail / Form の4種類のページタイプ
- SEOメタデータ設定
- useAsyncDataによるデータフェッチ
- エラーハンドリングパターン

**使用例:**
```
/skill nuxt4-pages
```

### 5. repository-creator

Repository層の実装パターンを提供するスキル。

**機能:**
- HTTPメソッド別実装パターン（GET/POST/PUT/PATCH/DELETE）
- FormData取り扱い
- requireValueOfによるバリデーション
- API接続先の抽象化

**使用例:**
```
/skill repository-creator
```

## ディレクトリ構成

```
.claude/
└── skills/
    ├── nuxt4-components/
    │   ├── SKILL.md              # スキル定義
    │   ├── references/           # 詳細ドキュメント
    │   │   ├── component-patterns.md
    │   │   └── styling-guide.md
    │   └── templates/            # コンポーネントテンプレート
    │       ├── atom.vue
    │       ├── molecule.vue
    │       ├── organism.vue
    │       └── template.vue
    ├── nuxt4-composables/
    │   ├── SKILL.md
    │   ├── reference.md
    │   └── templates/
    │       ├── ui.ts
    │       ├── form.ts
    │       └── root.ts
    ├── nuxt4-models/
    │   ├── SKILL.md
    │   ├── reference.md
    │   └── template.ts
    ├── nuxt4-pages/
    │   ├── SKILL.md
    │   ├── references/
    │   │   ├── best-practices.md
    │   │   └── implementation-guide.md
    │   └── templates/
    │       ├── simple-page.vue
    │       ├── list-page.vue
    │       ├── detail-page.vue
    │       └── form-page.vue
    └── repository-creator/
        ├── SKILL.md
        ├── reference.md
        └── template.ts
```

## Skillの構成要素

各スキルは以下の構成で作成されています：

### SKILL.md

スキルのエントリーポイント。以下を含む：

- **フロントマター**: name, description（Claude Codeが認識するメタデータ）
- **概要**: スキルの目的と機能
- **パターン定義**: 実装パターンとベストプラクティス
- **ガイドライン**: 使用方法とトラブルシューティング

### references/

詳細なドキュメントやガイドライン。SKILL.mdから参照される。

### templates/

コード生成時に使用するテンプレートファイル。

## 使い方

### 1. スキルの配置

`.claude/skills/` ディレクトリにスキルフォルダを配置します。

### 2. スキルの呼び出し

Claude Codeで `/skill {skill-name}` コマンドを使用してスキルを呼び出します。

```bash
# 例: コンポーネント作成時
/skill nuxt4-components

# 例: Composable作成時
/skill nuxt4-composables
```

### 3. コンテキストに応じた自動適用

スキルのdescriptionに基づき、関連するタスクで自動的にスキルが提案されます。

## カスタマイズ

各スキルはプロジェクト固有の要件に合わせてカスタマイズできます：

1. **SKILL.md**: パターンや規約を修正
2. **templates/**: テンプレートコードを更新
3. **references/**: 詳細ドキュメントを追加・修正

## ライセンス

MIT

## 関連リンク

- [Claude Code 公式ドキュメント](https://docs.anthropic.com/claude-code)
- [Qiita Advent Calendar 2024](https://qiita.com/advent-calendar/2024)
