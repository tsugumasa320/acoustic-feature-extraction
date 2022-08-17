# [survey]acoustic-feature-extraction-using-spectrum

## Python Library

### Librosa
<https://librosa.org/doc/latest/feature.html>

- chroma_stft : 波形かスペクトログラムからクロマグラムを作成する（クロマグラムは、全周波数帯域のパワーを12音階に落とし込み、ある区間の時間における音の成分を可視化したもの）

- chroma_sqt : 定Q変換を用いてクロマグラムを作成

- chroma_cens : Chroma Energy Normalized（CENS）を計算 (ダイナミクス、音色、アーティキュレーションの特徴抽出？ 音声のマッチングや検索に用いられるらしい.）

- melspectrogram

- mfcc

- rms : Root Mean Square(音圧の指標として用いられる)

- spectral_centroid : スペクトルの重心を求める. 音の明るさと強いつながりを持つ<https://en.wikipedia.org/wiki/Spectral_centroid>

- spectral_bandwith : computes the order- p spectral bandwidth(?)

- spectral_contrast : スペクトログラムの周波数をいくつかのサブバンドに分割し、各サブバンドのピークと谷の平均エネルギーを比較することでエネルギーコントラストを推定する.低コントラストの場合はノイズらしく、高コントラストの場合は明瞭な信号であると推測される.

- spectral_flatness : スペクトラルの平坦度を算出する.音がどの程度ノイズに近いかを数値化したもの.スペクトラル平坦度
が高い(1に近い)ほどホワイトノイズに近いことを示す.

- spectral_rolloff : ロールオフ周波数(減衰傾度)の計算. 

### essentia

#### Low-level
<https://essentia.upf.edu/streaming_extractor_music.html>

- loudness_ebu128 : ERU R128?に基づいたラウドネス算出

- average_loudness

- dynamic_complexity : ラウドネスの変動量計算

- spectral_rms

- spectral_flux : パワースペクトルがどれだけ早く変化しているかを示す指標. オーディオ信号の音色決定やオンセット検出などに用いられる<https://en.wikipedia.org/wiki/Spectral_flux>

