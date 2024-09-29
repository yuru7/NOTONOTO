# NOTONOTO

NOTONOTO は、 [Noto シリーズ](https://fonts.google.com/noto) である Noto Sans Mono と Noto Sans JP を合成した、プログラミング向けフォントです。

Noto シリーズは、その語源が "No more tofu (豆腐はいらない！)" から来ているように (*)、表示できない文字を無くすことを目標に作られたフォントファミリーです。

(*): 「豆腐」はフォントに含まれない文字が `□` 表示になる様を表すネットスラング

Noto シリーズでは、様々なデバイスや文書で使えることを目指しているため、プレーンでクセが無く、読みやすいことも特徴です。いわば「特徴が無いことが特徴」とも言えるフォントで、様々な場面で馴染むので多くのWebサイトデザインでも用いられています。

NOTONOTO は、そんなプレーンであっさりとした Noto シリーズを、いつものコーディングシーンでも使いたい方のためのフォントです。

👉 ダウンロードは [NOTONOTO リリース](https://github.com/yuru7/NOTONOTO/releases/latest) からどうぞ。  
※「Assets」内の zip ファイルをダウンロードしてご利用ください。

> 💡 その他、公開中のプログラミングフォント
> - 日本語文字に源柔ゴシック、英数字部分に Hack を使った [**白源 (はくげん／HackGen)**](https://github.com/yuru7/HackGen)
> - 日本語文字に IBM Plex Sans JP、英数字部分に IBM Plex Mono を使った [**PlemolJP (プレモル ジェイピー)**](https://github.com/yuru7/PlemolJP)
> - 日本語文字にBIZ UDゴシック、英数字部分に JetBrains Mono を使った [**UDEV Gothic**](https://github.com/yuru7/udev-gothic)

## 特徴

以下の特徴を備えています。

- Noto シリーズの等幅英文フォント Noto Sans Mono 由来のラテン文字
- Noto シリーズの日本語フォント Noto Sans JP 由来の日本語文字
- Noto シリーズ由来のWeight
- 半角・全角の幅比率が異なるバリエーションあり
    - Noto Sans Mono ExtraCondensed スタイルを用いた、幅比率 半角1:全角2
    - Noto Sans Mono 標準スタイルを用いた、幅比率 半角3:全角5
- 全角スペースの可視化
    - 全角スペースの可視化したくない方向けの不可視版あり
- 一部記号の判読性の向上
    - Noto Sans Mono ExtraCondensed スタイル (1:2 幅版利用) における `#` `*` の拡大
    - `_` が2つ連なったときに離れて見えるように調整
- 収録される文字の違い等によって分かれた複数のバリエーションを用意 (下記参照)

### バリエーション

| **フォント ファミリー** | **説明** |
| :------------:          | :---     |
| **NOTONOTO** | ラテン文字に Noto Sans Mono ExtraCondensed スタイルを用いることで文字幅比率「半角1:全角2」にした通常版。その他の日本語文字や日本語文書に頻出する記号類に Noto Sans JP を使用。 |
| **NOTONOTO Console** | Noto Sans Mono の字体を除外せずに全て適用したバリエーション。多くの記号が半角で表示されるため、コンソールでの利用や記号類は可能な限り半角で表示したい人にオススメ。 |
| **NOTONOTO35** | ラテン文字に Noto Sans Mono 標準スタイルを用いることで文字幅比率「半角3:全角5」にしたバリエーション。英数字が通常版の NOTONOTO よりも広く余裕をもって表示される。 |
| **NOTONOTO35 Console** | NOTONOTO Console の文字幅比率を 半角3:全角5 にしたバリエーション |

## 表示サンプル

| 通常版 (幅比率 半角1:全角2) | 35版 (幅比率 半角3:全角5) |
| :---: | :---: |
|  |  |

## ビルド

環境:

- fontforge: `20230101` \[[Windows](https://fontforge.org/en-US/downloads/windows/)\] \[[Linux](https://fontforge.org/en-US/downloads/gnulinux/)\]
- Python: `>=3.12`

### Windows (PowerShell Core)

```sh
# 必要パッケージのインストール
pip install -r requirements.txt
# ビルド
& "C:\Program Files (x86)\FontForgeBuilds\bin\ffpython.exe" .\fontforge_script.py && python3 .\fonttools_script.py
```

### ビルドオプション

`fontforge_script.py` 実行時、以下のオプションを指定できます。

- `--35`: 半角3:全角5 の幅にする
- `--console`: できるだけ East Asian Ambiguous Width 記号を半角で表示する
- `--hidden-zenkaku-space`: 全角スペース可視化を無効化
- `--debug`: Regular スタイルのみをビルドする

## ライセンス

SIL OPEN FONT LICENSE Version 1.1 が適用され、商用・非商用問わず利用可能です。

- 詳細は [LICENSE](https://raw.githubusercontent.com/yuru7/NOTONOTO/main/LICENSE) を参照
- 各種ソースフォントのライセンスは、ソースフォント毎のディレクトリに同梱
