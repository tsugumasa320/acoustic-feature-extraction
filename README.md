# acoustic-feature-extraction

## Python Library

### Librosa
<https://librosa.org/doc/latest/feature.html>

・chroma_stft : 波形かスペクトログラムからクロマグラムを作成する（クロマグラムは、全周波数帯域のパワーを12音階に落とし込み、ある区間の時間における音の成分を可視化したもの）

・chroma_sqt : 定Q変換を用いてクロマグラムを作成

・chroma_cens : Chroma Energy Normalized（CENS）を計算 (ダイナミクス、音色、アーティキュレーションの特徴抽出？ 音声のマッチングや検索に用いられるらしい。<https://librosa.org/doc/main/generated/librosa.feature.chroma_cens.html>）

