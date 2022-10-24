# [survey]acoustic-feature-extraction-using-spectrum


## Librosa
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

## essentia

### Low-level
<https://essentia.upf.edu/streaming_extractor_music.html>

- loudness_ebu128 : ERU R128?に基づいたラウドネス算出
- average_loudness
- dynamic_complexity : ラウドネスの変動量計算
- spectral_rms
- spectral_flux : パワースペクトルがどれだけ早く変化しているかを示す指標. オーディオ信号の音色決定やオンセット検出などに用いられる<https://en.wikipedia.org/wiki/Spectral_flux>
- spectral_centroid,spectral_kurtosis,pectral_spread,spectral_skewness : スペクトロ形状についての統計量.centroid以外はどう応用できるか不明
- spectral_rolloff
- spectral_decrease
- hfc : 高周波成分の測定に用いられる
- spectral_strongpeak　： スペクトルのstrong peakの計算.strong peakとはmax peakと振幅の半分の間の帯域幅の比率を表す
- zerocrossingrate　： ゼロクロス率を計算. 信号の雑音成分の多さを表せる
- spectral_energy : スペクトルのエネルギー算出
- spectral_energyband_low,spectral_energyband_middle_low,spectral_energyband_middle_high,spectral_energyband_high　： 各帯域におけるスペクトルエネルギーの算出
- barkbands : 27のBarkバンドにおけるスペクトルエネルギー
- melbands : 40のmelバンドにおけるスペクトルエネルギー
- melbands128 : 128個のmelバンドにおけるスペクトルエネルギー
- erbbands : 40個のERBバンドのスペクトルエネルギー
- mfcc : mel frequency cepstrum 係数
- gfcc : ガンマトーン特徴ケプストラム係数
- barkbands_crest,barkbands_flatness_db : Bark bandのエネルギーに対して計算されたcrestとflatness
- barkbands_kurtosis,barkbands_skewness,barkbands_spread : Bark bands のエネルギーに対する中心モーメント統計量
- melbands_crest,melbands_flatness_db : Melバンドのエネルギーに対して計算されたcrestとflatness
- melbands_kurtosis,melbands_skewness,melbands_spread : Melバンドのエネルギーに対する中心モーメント統計量
- erbbands_crest,erbbands_flatness_db : ERBバンドのエネルギーで計算されたcrestとflatness
- erbbands_kurtosis,erbbands_skewness,erbbands_spread : ERBバンドのエネルギーに対する中心モーメントの統計量
- dissonance : 信号のスペクトルピークから不協和度を計算
- spectral_entropy : エントロピーの計算. 音声認識で有声・無声の判定に使われる
- pitch_salience : 音程の顕著性を計算. 純音の場合は０に近づき、倍音成分が豊富だと１に近づく
- spectral_complexity : スペクトル複雑度を計算(入力スペクトルのピークが多い=複雑らしい)
- spectral_contrast_coeffs,spectral_contrast_valleys : スペクトル・コントラスト特徴量

## opensmile
### Audio features (low-level)
LibrosaとEssentiaに載っている項目が多いため説明は省略

- Frame Energy
- Frame Intensity / Loudness (approximation)
- Critical Band spectra (Mel/Bark/Octave, triangular masking filters)
- Mel-/Bark-Frequency-Cepstral Coefficients (MFCC)
- Auditory Spectra
- Loudness approximated from auditory spectra
- Perceptual Linear Predictive (PLP) Coefficients
- Perceptual Linear Predictive Cepstral Coefficients (PLP-CC)
- Linear Predictive Coefficients (LPC)
- Line Spectral Pairs (LSP, aka. LSF)
- Fundamental Frequency (via ACF/Cepstrum method and via Subharmonic-Summation (SHS))
- Probability of Voicing from ACF and SHS spectrum peak
- Voice-Quality: Jitter and Shimmer
- Formant frequencies and bandwidths
- Zero and Mean Crossing rate
- Spectral features (arbitrary band energies, roll-off points, centroid, entropy, maxpos, minpos, variance (= spread), skewness, kurtosis, slope)
- Psychoacoustic sharpness, spectral harmonicity
- CHROMA (octave-warped semitone spectra) and CENS features (energy-normalised and smoothed CHROMA)
- CHROMA-derived features for Chord and Key recognition
- F0 Harmonics ratios

## Pypl
<https://brookemosby.github.io/Signal_Analysis/Signal_Analysis.features.html>
- get_F0
- get_HNR
- get_Jitter

## 
### TIMBRE MODELS

<https://www.audiocommons.org/2018/07/15/audio-commons-audio-extractor.html>

<https://www.audiocommons.org/2018/07/15/audio-commons-audio-extractor.html#:~:text=As%20described%20in-,deliverable%20D5.2,-%2C%20a%20number%20of>

- brigtness : 音の明るさを計算. スペクトルセントロイドとスペクトルエネルギー比で算出
- hardness : 硬さを計算.硬いものや大きな力を使って作られたという音を表す(?)
- depth : 音の深さを計算.低周波のスペクトル重心や低周波エネルギーの割合、低周波ロールオンを分析している
- roughness : 音の質感が不均一であったり不規則である音を表す
- boominess : 音の大きさ、奥行き、響きが感じられる音を表す
- warmth 温かみのある音を表す(おそらく倍音成分の出方を見ているか)
- sharpness : 音の鋭さを表す.(これも倍音成分?)
- reverb : 信号にリバーブがかかっているかどうか判定
