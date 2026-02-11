# System Monitor Cinnamon

CinnamonデスクトップパネルにCPU使用率、メモリ使用率、リアルタイムのネットワーク速度を表示するための小さなツールです。
[RunCat365](https://github.com/Kyome22/RunCat365)に触発されました。


## 機能

- 📊 リアルタイムのCPU使用率表示
- 💾 メモリ使用状況の表示
- 🌐 ネットワークのアップロード/ダウンロード速度の表示
- 🎨 カスタマイズ可能なアイコンテーマ（猫/馬）
- 🌓 自動/黒/白のアイコンテーマをサポート
- ⚙️ 調整可能なリフレッシュレート
- 🎯 軽量、低リソース消費

## インストール方法

1. プロジェクトファイルをローカルにダウンロードします。
2. フォルダ全体をCinnamonアプレットディレクトリにコピーします：
   ```bash
   mkdir -p ~/.local/share/cinnamon/applets/system-monitor-cinnamon@MainPoser/;
   cp -r system-monitor-cinnamon ~/.local/share/cinnamon/applets/system-monitor-cinnamon@MainPoser/;
   # 翻訳ファイルをインストールする
   mkdir -p ~/.local/share/locale/zh_CN/LC_MESSAGES/;
   msgfmt -o ~/.local/share/locale/zh_CN/LC_MESSAGES/system-monitor-cinnamon@MainPoser.mo ~/.local/share/cinnamon/applets/system-monitor-cinnamon@MainPoser/po/zh_CN.po
   ```
3. Cinnamonの設定でアプレットを有効にします。
4. パネルを右クリック → アプレットを追加 → "System Monitor Cinnamon" を選択します。

## 使用方法

インストール後、アプレットはパネルにシステム監視情報を自動的に表示します。デフォルトの表示形式は次のとおりです：

```
CPU: 45% | MEM: 2.1G/8G | ↑ 1.2MB/s ↓ 500KB/s
```

## 設定オプション

アプレットを右クリックして「設定」を選択すると、次のオプションを調整できます：

- **ネットワーク速度の表示**：パネルにネットワーク速度を表示するかどうかを制御します。
- **リフレッシュレート**：データ更新間隔（1〜60秒）を設定します。
- **アイコンテーマ**：アイコンのカラーテーマ（システム/白/黒）を選択します。
- **アニメーションアイコン**：アニメーションアイコンの種類（猫/馬）を選択します。

## プロジェクト構造

```
system-monitor-cinnamon/
├── applet.js              # メインプログラムファイル
├── metada.json            # アプレットのメタデータ
├── setting-schema.json    # 設定オプションの定義
├── stylesheet.css         # スタイルファイル
├── icons/                 # アイコンリソース
│   └── runners/
│       ├── cat/          # 猫のアニメーションアイコン
│       └── horse/        # 馬のアニメーションアイコン
├── LICENSE                # ライセンスファイル
└── README.md              # プロジェクトの説明
```

## 技術的な実装

- JavaScript (ES6)で記述
- Cinnamon Appletフレームワークに基づく
- システムファイルからCPU、メモリ、ネットワークデータを読み取る
- アニメーション効果にGdkPixbufを使用

## トラブルシューティング

アプレットが正常に動作しない場合は、次の解決策を試してください：

1. Cinnamonを再起動する：`Ctrl+Alt+Esc`を押すか、`cinnamon --replace`を実行します。
2. システムログを確認する：`~/.xsession-errors`でエラーメッセージを確認します。
3. 必要な依存関係がシステムにインストールされていることを確認してください。

## 貢献ガイド

バグレポートや機能リクエストを歓迎します！コードに貢献したい場合：

1. このプロジェクトをフォークする
2. 機能ブランチを作成する (`git checkout -b feature/AmazingFeature`)
3. 変更をコミットする (`git commit -m 'Add some AmazingFeature'`)
4. ブランチにプッシュする (`git push origin feature/AmazingFeature`)
5. プルリクエストを作成する

## ライセンス

このプロジェクトはMITライセンスの下でライセンスされています - 詳細については[LICENSE](LICENSE)ファイルを参照してください。

## 著者

MainPoser - 2026
