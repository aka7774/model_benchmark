# model_benchmark

- モデルをとっかえひっかえして遊ぶ
- 自作マージモデルのテストをする

## あそびかた

- 女の子(鑑賞)用です

### sd_infotextsを使う

- https://github.com/aka7774/sd_infotexts
- edit_txt フォルダに実行したいフォルダの中身のテキストファイルをコピーする
- 「Infotexts」タブの「Generate」タブで「Model hash」「Model sha256」「VAE sha256」にチェックを入れて「Apply」
- テストしたいモデルを任意に選択する
- txt2imgのScriptで「Generate fro Infotexts」を選択してGenerate
- 一括生成された画像が output フォルダに出力される

## basic

- 基礎的なプロンプトや設定の効き具合をざっと知る
- 100項目弱
- 各画像の説明は basic.txt に記載
- SD1系かつDanbooruタグ対応モデルを想定
- ポジティブプロンプトの基本は masterpiece, best quality, 1girl
- ネガティブプロンプトの基本は (worst quality:1.4), (low quality:1.4) , (monochrome:1.1),
- Sampler は DPM++ 2M Karras
- Steps は 20
- Size は 512x768
- CFG Scale は 7
- Clip Skip、Eta、ENSDは1111の設定を反映するのでお好みで

# ToDo

## art編

- 一つの作品として完成されている絵を収録
- スレで流行ったもの、需要の高そうなものを中心にする
- 短いプロンプトで表現できているもの(加工しやすさのため)
- できるだけ自然なプロンプト(汎用性を持たせるため)
- 固有名詞は入れない(版権再現度とかは必要なら別枠で)
- NSFWのフォロー(体位の網羅など)

## 自動化

- apiを実装する
- クラウドでモデルをダウンロードして画像を生成して暗号化zipにしてDriveに保存して終了する
- supermergerとの連携?

## 自動評価

- なんらかのAI的な評価ツールの導入(結果につなげるのが難しそう)
