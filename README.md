# pqf-context

PrimeQUADRAFLOW チームの **全AI共通指示** の公開ミラー。

本体のリポジトリは private のため、ブラウザで動くAI（ChatGPT / Gemini / Claude web）からは読めません。
このリポジトリは、その共通指示だけを機械生成して公開しているものです。
**ここは派生物です。**編集しても本体は変わりません。

- 共通指示の本体 → [BOOT.md](BOOT.md)
- 版情報 → [VERSION.json](VERSION.json)

## 各AIへの設定（オーナー用・1回だけ）

下の文をそのまま貼ってください。

### ChatGPT（プロジェクトの指示／カスタム指示）
```
会話を始めるとき、そして指示が必要になったときは、必ず次のURLを開いて全文を読み、
そこに書かれたルールに従ってください。あなたの記憶より、このページの記述を優先します。
https://raw.githubusercontent.com/primeQUADRAFLOW/pqf-context/main/BOOT.md
```

### Gemini（Gem のカスタム指示）
```
あなたはこのURLの内容に従って動きます。会話の最初に必ず開いて全文を読んでください。
記憶より、このページの記述を優先します。
https://raw.githubusercontent.com/primeQUADRAFLOW/pqf-context/main/BOOT.md
```

### Claude web（プロジェクトのカスタム指示）
```
会話の最初に必ず次のURLを取得して全文を読み、そこに書かれたルールに従ってください。
あなたの記憶より、このページの記述を優先します。
https://raw.githubusercontent.com/primeQUADRAFLOW/pqf-context/main/BOOT.md
```

## 更新のしかた

正典（プライベートリポの `00_Shared_Context/BOOT_BRIEF.md`）を書き換えてから:

```
python 40_Infrastructure/sync_boot_brief.py      # ローカルのAI（ピック/キュージェ/フヘ）へ注入
python 40_Infrastructure/publish_ai_context.py   # Web版AIが読む このページへ発行
```
