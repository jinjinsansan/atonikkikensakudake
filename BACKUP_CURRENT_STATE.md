# かんじょうにっき - 現在の状態バックアップ

## バックアップ日時
2025年1月24日 - カウンセラーメモ表示機能実装前

## プロジェクト概要
一般社団法人NAMIDAサポート協会が提唱するテープ式心理学に基づいた、自己肯定感を育てる感情日記アプリです。

## 🌟 現在実装済みの機能

### ✅ ユーザー向け機能
- **感情日記システム**: 8種類のネガティブ感情（恐怖、悲しみ、怒り、悔しい、無価値感、罪悪感、寂しさ、恥ずかしさ）
- **無価値感推移グラフ**: グラフによる自己肯定感の可視化
- **日記検索**: キーワード・日付・感情での高度な検索
- **SNSシェア**: 成長の記録をシェア
- **レスポンシブデザイン**: 全デバイス対応

### ✅ 管理者向け機能
- **管理画面**: カウンセラー専用の統合管理システム
- **カレンダー検索**: 視覚的な日付検索機能
- **カウンセラーメモ**: 各日記への専門的なメモ機能（管理画面のみ表示）
- **担当者管理**: ワンクリックでの担当者割り当て
- **緊急度管理**: 3段階の緊急度設定・監視
- **データ管理**: Supabaseとの連携・同期機能

### ✅ 新機能（実装済み）
- **自動同期システム**: ローカルデータの自動Supabase同期
- **同意履歴管理**: プライバシーポリシー同意の完全追跡
- **デバイス認証システム**: PIN番号認証、秘密の質問、セキュリティダッシュボード
- **メンテナンスモード**: システム保守時の適切な案内

## 🚀 技術スタック

- **フロントエンド**: React + TypeScript
- **スタイリング**: Tailwind CSS
- **データベース**: Supabase (PostgreSQL)
- **認証**: デバイス認証システム
- **デプロイ**: Netlify
- **開発環境**: Vite

## 📦 依存関係

```json
{
  "dependencies": {
    "lucide-react": "^0.344.0",
    "react": "^18.3.1",
    "react-dom": "^18.3.1",
    "@supabase/supabase-js": "^2.39.0"
  },
  "devDependencies": {
    "@eslint/js": "^9.9.1",
    "@types/react": "^18.3.5",
    "@types/react-dom": "^18.3.0",
    "@vitejs/plugin-react": "^4.3.1",
    "autoprefixer": "^10.4.18",
    "eslint": "^9.9.1",
    "eslint-plugin-react-hooks": "^5.1.0-rc.0",
    "eslint-plugin-react-refresh": "^0.4.11",
    "globals": "^15.9.0",
    "postcss": "^8.4.35",
    "tailwindcss": "^3.4.1",
    "typescript": "^5.5.3",
    "typescript-eslint": "^8.3.0",
    "vite": "^5.4.2"
  }
}
```

## 🗄️ データベース構成

### 主要テーブル
- **users**: ユーザー情報
- **diary_entries**: 日記エントリー（counselor_memoフィールド含む）
- **counselors**: カウンセラー情報
- **chat_rooms**: チャットルーム
- **messages**: メッセージ
- **consent_histories**: 同意履歴

## 👥 カウンセラーアカウント

| 名前 | メールアドレス |
|------|----------------|
| 仁カウンセラー | jin@namisapo.com |
| AOIカウンセラー | aoi@namisapo.com |
| あさみカウンセラー | asami@namisapo.com |
| SHUカウンセラー | shu@namisapo.com |
| ゆーちゃカウンセラー | yucha@namisapo.com |
| sammyカウンセラー | sammy@namisapo.com |

**共通パスワード**: `counselor123`

## 📁 重要なファイル構成

### 主要コンポーネント
- `src/App.tsx`: メインアプリケーション
- `src/pages/DiaryPage.tsx`: 日記作成ページ
- `src/pages/DiarySearchPage.tsx`: 日記検索ページ
- `src/components/AdminPanel.tsx`: 管理画面（カウンセラーメモ機能含む）
- `src/components/DataMigration.tsx`: データ管理
- `src/components/AutoSyncSettings.tsx`: 自動同期設定
- `src/components/ConsentHistoryManagement.tsx`: 同意履歴管理
- `src/components/DeviceAuthManagement.tsx`: デバイス認証管理
- `src/components/SecurityDashboard.tsx`: セキュリティダッシュボード

### フック
- `src/hooks/useAutoSync.ts`: 自動同期フック
- `src/hooks/useSupabase.ts`: Supabase連携フック
- `src/hooks/useMaintenanceStatus.ts`: メンテナンス状態フック

### ライブラリ
- `src/lib/supabase.ts`: Supabase設定・サービス
- `src/lib/deviceAuth.ts`: デバイス認証システム

## 🎯 次の実装予定

**カウンセラーメモのユーザー表示機能**
- 既存の`counselor_memo`フィールドを活用
- `DiaryPage.tsx`と`DiarySearchPage.tsx`に読み取り専用表示を追加
- 新機能追加ではなく、既存機能の表示拡張

## ⚠️ 重要な制約事項

- `pages`ディレクトリ以外は変更しないこと
- Tailwind設定ファイルに手を加えないこと
- 新しい依存パッケージはインストールしないこと
- `supabase/migrations/`内のファイルは変更しないこと

## 🔍 現在の状態

- すべての機能が正常に動作中
- エラーなし
- UI/UX完全に機能
- データベース接続正常
- 自動同期機能動作中

## 📞 サポート情報

- **開発者**: 一般社団法人NAMIDAサポート協会
- **メール**: info@namisapo.com
- **受付時間**: 平日 9:00-17:00

---

**このバックアップ時点で、すべての機能が正常に動作しています。**
**次の変更: カウンセラーメモのユーザー表示機能を安全に実装予定**