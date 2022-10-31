# Essentiaのオブジェクトメモ
<https://essentia.upf.edu/algorithms_reference.html>

## Envelope/SFX (Envelopeなので湯谷の研究には関係なさそう)
- AfterMaxToBeforeMaxEnergyRatio
- DerivativeSFX： 急なリリースフェーズを持つ衝撃音と非衝撃音を区別する. t
- Envelope: 非対称ローパス フィルターを適用して、信号のエンベロープを計算. t
- FlatnessSFX: 信号包絡線の平坦係数を計算
- LogAttackTime: 信号エンベロープのアタックタイムの対数 (基数 10) を計算
- MaxToTotal: 信号のエンベロープの最大値のインデックスとエンベロープの全長との比率を計算
- MinToTotal: 信号のエンベロープの最小値のインデックスとエンベロープの全長の比率を計算
- StrongDecay: オーディオ信号の強力な減衰を計算
- TCToTotal: 信号エンベロープの全長に対する時間重心の比率を計算

## Filters
- AllPass
- BandPass
- BandReject
- DCRemoval
- EqualLoudness: 等ラウドネス
- HighPass
- IIR
- LowPass
- MaxFilter
- MedianFilter
- MovingAverage

## Input/output
- AudioLoader
- AudioOnsetsMarker
- AudioWriter
- EasyLoader
- EqloudLoader
- FileOutput
- MetadataReader
- MonoLoader
- MonoWriter
- VectorInput
- YamlInput
- YamlOutput

## Standard
- AutoCorrelation: 信号の自己相関ベクトルを計算
- BPF: 離散xy座標間を線形補間
- BinaryOperator: 2つの配列を指定して、基本的な算術演算を要素ごとに実行します
- BinaryOperatorStream: 上記のストリーム版
- Clipper
- ConstantQ
- CrossCorrelation: 2つの信号の相互相関ベクトルを計算
- CubicSpline
- DCT: 離散コサイン変換
- Derivative: 入力信号の一次導関数を返します。つまり、各入力値に対して、前の値を引いた値を返します。
- FFT: アンプのみのSTFT
- FFTC: 複素数込みのSTFT
- FrameCutter: 入力バッファをフレームにスライス
- FrameGenerator
- FrameToReal
- IDCT
- IFFT
- IFFTC
- MinMax: 配列の最大最小を計算
- MonoMixer: stereoからmonoへ
- Multiplexer: 
- NSGConstantQ
- NSGConstantQStreaming
- NSGIConstantQ
- NoiseAdder: noiseを与える
- OverlapAdd
- PeakDetection
- PoolToTensor: PoolからTensorへ
- RealAccumulator
- Resample
- Scale: クリッピングすることで信号をスケーリングする
- Slicer
- Spline
- StereoDemuxer
- StereoMuxer
- StereoTrimmer
- TensorNormalize: MinMax法かstandard normで信号を正規化する
- TensorToPool: TensorからPoolへ
- TensorToVectorReal
- TensorTranspose: Tensorの転置ができる
- Trimmer
- UnaryOperator: 配列の基本的な計算
- UnaryOperatorStream
- VectorRealAccumulator
- VectorRealToTensor
- WarpedAutoCorrelation: オーディオ信号の歪んだ自己相関を計算
- Welch: スペクトル密度の計算.オーバーラップしている必要がある? y
- Windowing
- ZeroCrossingRate: ゼロ交差率の計算.Noisyさを表す指標としても使えそう. y

## Spectral(次はここから)
- BFCC: パーカッシブさを計算できるとある t
- BarkBands; 
- ERBBands
- EnergyBand
- EnergyBandRatio
- FlatnessDB: DBスケールの配列の平坦度 y
- Flux: スペクトルフラックス.音の立ち上がりの検出
- FrequencyBands
- GFCC
- HFC
- LogSpectrum
- MFCC
- MaxMagFreq: スペクトル内で最大の振幅を持つ周波数を計算
- MelBands
- Panning
- PowerSpectrum
- RollOff
- SpectralCentroidTime: Time領域でのスペクトル重心の計算
- SpectralComplexity: スペクトル複雑度.Noisyの指標に使えるか
- SpectralContrast: 
- SpectralPeaks
- SpectralWhitening
- Spectrum
- SpectrumToCent
- StrongPeak
- TensorflowInputMusiCNN
- TensorflowInputTempoCNN
- TensorflowInputVGGish
- TriangularBands
- TriangularBarkBands

## Rhythm(自分の研究には関係ないので未記載)

## Math
- CartesianToPolar
- Magnitude
- PolarToCartesian

## Statistics
- CentralMoments
- Centroid: スペクトル重心.明るさの指標に使われる
- Crest: 配列の最大値と算術平均の間の比率の計算
- Decrease: 
- DistributionShape: 分散、歪度、および尖度を計算 t
- Energy: 配列のエネルギー(信号の2乗)を計算
- Entropy: 配列のシャノン・エントロピーを計算. 自動音声認識における有声・無声の判定に利用
- Flatness: 幾何平均と算術平均の比として定義される，配列の平坦度を計算 t
- GeometricMean: 正の値の配列の幾何平均を計算
- Histogram
- InstantPower: 配列の瞬時累乗を計算
- Mean
- Median
- PoolAggregator: Poolに対して統計的な集約を行い、集約結果を新しい Pool に配置
- PowerMean
- RMS
- RawMoments
- SingleGaussian
- Variance
- Viterbi

## Tonal

- ChordsDescriptors
- ChordsDetection
- ChordsDetectionBeats
- Chromagram
- Dissonance: スペクトラムピークから不協和度を算出する
- HPCP
- HarmonicPeaks
- HighResolutionFeatures
- Inharmonicity: 非調和度.基本周波数の整数倍から離れる度合い.https://en.wikipedia.org/wiki/Inharmonicity
- Key
- KeyExtractor
- NNLSChroma
- OddToEvenHarmonicEnergyRatio
- PitchSalience
- SpectrumCQ
- TonalExtractor
- TonicIndianArtMusic
- Tristimulus
- TuningFrequency: チューニング周波数を推定
- TuningFrequencyExtractor

## Music Similarity

- ChromaCrossSimilarity
- CoverSongSimilarity
- CrossSimilarityMatrix

## Fingerprinting

- Chromaprinter

## Audio Problems

- ClickDetector
- DiscontinuityDetector
- FalseStereoDetector
- GapsDetector: オーディオのギャップ検出.Lossに使えるか?
- HumDetector
- NoiseBurstDetector
- SNR: signal noise ratio. y
- SaturationDetector
- StartStopCut
- TruePeakDetector

## Duration/silence

- Duration
- EffectiveDuration
- FadeDetection
- SilenceRate
- StartStopSilence

## Loudness/dynamics

- DynamicComplexity
- Intensity: 入力された音声信号をリラックス（-1）、モデレート（0）、アグレッシブ（1）のいずれかに分類. y
- Larm
- Leq
- LevelExtractor
- Loudness
- LoudnessEBUR128
- LoudnessEBUR128Filter
- LoudnessVickers
- ReplayGain

## Extractors

- BarkExtractor
- Extractor
- FreesoundExtractor
- LowLevelSpectralEqloudExtractor
- LowLevelSpectralExtractor
- MusicExtractor

## Synthesis

- HarmonicMask
- HarmonicModelAnal
- HprModelAnal
- HpsModelAnal
- ResampleFFT
- SineModelAnal
- SineModelSynth
- SineSubtraction
- SprModelAnal
- SprModelSynth
- SpsModelAnal
- SpsModelSynth
- StochasticModelAnal
- StochasticModelSynth

## Pitch

- MultiPitchKlapuri
- MultiPitchMelodia
- PitchCREPE
- PitchContourSegmentation
- PitchContours
- PitchContoursMelody
- PitchContoursMonoMelody
- PitchContoursMultiMelody
- PitchFilter
- PitchMelodia
- PitchSalienceFunction
- PitchSalienceFunctionPeaks
- PitchYin
- PitchYinFFT
- PitchYinProbabilistic
- PitchYinProbabilities
- PitchYinProbabilitiesHMM
- PredominantPitchMelodia
- Vibrato

## Transformations
- PCA
## Segmentation
- SBic: オーディオのセグメンテーション
## Machine Learning

- TensorflowPredict2D
- TensorflowPredict
- TensorflowPredictCREPE
- TensorflowPredictEffnetDiscogs
- TensorflowPredictMusiCNN
- TensorflowPredictTempoCNN
- TensorflowPredictVGGish
