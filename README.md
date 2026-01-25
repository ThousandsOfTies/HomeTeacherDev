# HomeTeacherDev

**HomeTeacher 開発用リポジトリ**

このリポジトリは、[HomeTeacher](https://github.com/ThousandsOfTies/HomeTeacher) の開発版（ステージング環境）です。
最新の機能を本番環境にマージする前に、ここで動作確認を行います。

## 🎯 Versions

### 📚 Dev Build (TutoTuto)
開発中の最新ビルドです。動作が不安定な可能性があります。

**[Launch Dev App →](https://thousandsofties.github.io/HomeTeacherDev/)**

```
HomeTeacherDev/ (このリポジトリ)
├── .github/workflows/  # GitHub Pages自動デプロイ
├── Makefile            # 統合ビルド管理
└── repos/              # 依存リポジトリ
    ├── drawing-common/
    └── home-teacher-core/
```

## ⚠️ 注意事項

- **開発用環境**: この環境は開発者のテスト用です。
- **データのリセット**: データベース構造の変更に伴い、保存されたデータがリセットされる可能性があります。
- **API接続先**: 本番API、または開発用APIに接続されます（設定によります）。

## 🚀 クイックスタート

```bash
git clone https://github.com/ThousandsOfTies/HomeTeacherDev.git
cd HomeTeacherDev
make setup
```

## 📤 本番への反映手順

1. このDev環境で動作確認を完了する
2. `home-teacher-core` 等の各リポジトリを `main` ブランチにマージ
3. 本番用リポジトリ `HomeTeacher` で `make update-versions` を実行
4. 本番環境へデプロイ

---
Since this is a development mirror, please refer to the [Main Repository](https://github.com/ThousandsOfTies/HomeTeacher) for detailed documentation.
