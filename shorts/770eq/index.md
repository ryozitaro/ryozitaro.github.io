---
title: ATH-WS770の音質をスタジオ級にする
---

### まえがき

（スタジオ級は言い過ぎたかな…）  
音楽を聴きながら作業を行うこと、僕はよくあります。ATH-WS770 を以前から使っていたものの、音質について「う～ん…低音をキレよく上品に出しつつ他の帯域の音をもっと綺麗に出せたらうれしい」と思っていたのでフリーソフトで出音改善を図ってみました。  
ピンポイントで ATH-WS770 を作業用ヘッドホンとして使っている人は自分以外にあまりいないのでは？とは思いますが、一人にでも同じようなこと思っている人に届いたらうれしいです。

### 本題

長時間使ってエージングが済んでいる状態が前提です。  
※ **かなり変わるのでそのままの音に慣れている人は慣れるまで違和感がものすごく多いと思います。**

Equalizer APO をインストールしてください。  
詳しい使い方や音が変わらないなどのトラブルシューティングは Google it!  
`C:\Program Files\EqualizerAPO\config`にある`config.txt`の内容を以下に書き換えます。

```text
GraphicEQ: 20 0; 25 0; 31.5 -10; 40 -12; 50 -15; 62 -17; 80 -17; 100 -15; 125 -14; 160 -13; 200 -12; 250 -11; 315 -10; 400 -10; 500 -9; 650 -12; 800 -17; 890 -17; 1000 -17; 1250 -16; 1600 -14; 2000 -16; 2500 -14; 3150 -7; 3350 -4; 3750 -7; 4250 -12; 4600 -8; 5000 -3; 5500 -9; 6250 -9; 7000 -12; 8000 -10; 9000 -8; 10000 -3; 11000 -12; 12000 -18; 13750 -16; 14500 -16; 16000 -12; 18500 -3; 20000 -1
GraphicEQ: 20 0; 25 0; 31.5 4; 40 5; 50 3; 63 3; 80 5; 100 2; 125 0
Filter: ON PK Fc 1700 Hz Gain 3 dB Q 0.8
Filter: ON PK Fc 12000 Hz Gain 2 dB Q 0.8
Filter: ON PK Fc 16000 Hz Gain 2 dB Q 0.8
GraphicEQ: 25 0; 40 1.8; 63 2.6; 100 2.2; 160 2.2; 250 1; 400 0.6; 630 0.6; 1000 1.4; 1600 0.6; 2500 -1; 4000 0; 6300 0.6; 10000 0.2; 16000 0
```

これだけです。  
変更後は聞こえる音量がかなり下がっていますが、音質調整の副作用なのであまり気にしないでください。僕の場合は Windows の音量を 30 ～ 40 くらいに上げています 😌

それぞれブロックの役割は一番上から、

- フラット化
- 低域強調用
- 声を前に持ってくる用
- 明瞭度上げる用
- 明瞭度上げる用 2
- ちょっとした味付け

となっています。なので、一番上以外はオプションみたいな扱いです。  
音に慣れたら自己流に改変したりしてみて楽しんでみてください 😉
