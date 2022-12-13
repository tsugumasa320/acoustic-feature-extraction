# torchaudio.functional の Filterについてのメモ
<https://pytorch.org/audio/stable/functional.html>

[双2次フィルタ (Biquad Filter) の周波数特性（振幅・位相）の一覧](https://www.wizard-notes.com/entry/music-analysis/biquad-filter-frequency-responses)

## Filtering

allpass_biquad : Design two-pole all-pass filter. all-passフィルターは全周波数帯域を通すものらしい

band_biquad : Design two-pole band filter. two-poleのバンドフィルター（バンドパスと違う？）

bandpass_biquad : Design two-pole band-pass filter.

bandreject_biquad : Design two-pole band-reject filter.

bass_biquad : Design a bass tone-control effect.

biquad : Perform a biquad filter of input tensor.

contrast : Apply contrast effect. コンプレッションと同様に、オーディオ信号をより大きく聴こえるように修正するエフェクトです。

dcshift : Apply a DC shift to the audio.

deemph_biquad : Apply ISO 908 CD de-emphasis (shelving) IIR filter.

dither : Apply dither

equalizer_biquad : Design biquad peaking equalizer filter and perform filtering.

filtfilt : Apply an IIR filter forward and backward to a waveform.

flanger : Apply a flanger effect to the audio.

gain : Apply amplification or attenuation to the whole waveform.

highpass_biquad : Design biquad highpass filter and perform filtering. t

lfilter : Perform an IIR filter by evaluating difference equation.

lowpass_biquad : Design biquad lowpass filter and perform filtering. t

overdrive : Apply a overdrive effect to the audio. t

phaser : Apply a phasing effect to the audio.

riaa_biquad : Apply RIAA vinyl playback equalization.

treble_biquad : Design a treble tone-control effect.