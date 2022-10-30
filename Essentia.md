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

## Rhythm(自分の研究には関係ないので未記載)

## Math

## Statistics

## Tonal

## Music Similarity

## Fingerprinting

## Audio Problems

## Duration/silence

## Loudness/dynamics

## Extractors

## Synthesis

## Pitch

## Transformations

## Segmentation

## Machine Learning
