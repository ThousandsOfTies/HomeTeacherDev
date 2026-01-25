# HomeTeacherDev

**HomeTeacher 開発用 (ステージング) リポジトリ**

このリポジトリは、[HomeTeacher](https://github.com/ThousandsOfTies/HomeTeacher) の **ステージング環境** です。
各サブリポジトリ (`home-teacher-core` 等) の `main` ブランチの最新状態をデプロイし、本番環境更新前の動作確認を行うために使用します。

## 🎯 環境の役割

| 環境 | リポジトリ | 役割 | 参照するコード |
|---|---|---|---|
| **Staging** (Dev) | **此処 (HomeTeacherDev)** | 最新の動作確認 | 各サブリポジトリの `main` (最新) |
| **Production** | [HomeTeacher](https://github.com/ThousandsOfTies/HomeTeacher) | 安定版の公開 | 各サブリポジトリの `main` (検証済み時点) |

## 📚 Dev Build (TutoTuto)

**[Launch Dev App →](https://thousandsofties.github.io/HomeTeacherDev/)**

- サブリポジトリの `main` ブランチの最新状態が反映されます。
- 本番環境と異なり、開発中の機能が含まれる可能性があります。

## 🛠️ 開発フロー

1. **実装**: `home-teacher-core` 等のサブリポジトリで開発を行い、`main` にプッシュします。
2. **ステージング反映**: この `HomeTeacherDev` リポジトリで [Actions] からワークフローを手動実行（または空コミットをプッシュ）します。
   - これにより、サブリポジトリの最新 `main` が取り込まれてデプロイされます。
3. **検証**: 生成された [Dev App](https://thousandsofties.github.io/HomeTeacherDev/) で動作確認を行います。
4. **本番反映**: 検証が完了したら、本番用リポジトリ `HomeTeacher` 側でデプロイを実行します。

## 🚀 クイックスタート (ローカル)

```bash
git clone https://github.com/ThousandsOfTies/HomeTeacherDev.git
cd HomeTeacherDev
make setup
```

**Note**: `Makefile` の設定により、デフォルトで各リポジトリの `main` ブランチがクローンされます。

---
For official documentation, please refer to the [Main Repository](https://github.com/ThousandsOfTies/HomeTeacher).
