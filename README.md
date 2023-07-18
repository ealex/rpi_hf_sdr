# rpi_hf_sdr
This is a tentative rehash of https://github.com/bg3mdo/pisdr_hat.
This will be a receive-only module.
The **sound card's** output will be used as the system's audio output.

The entire front-end is based on the [qrp-labs](http://qrp-labs.com/receiver) receiver module, without the isolation transformers.

The project will use a [CX2047LNL](https://productfinder.pulseelectronics.com/api/open/part-attachments/datasheet/CX2047LNL) front-end transformer in a balanced configuration.

The mixer is a [SN74CBTLV3253PWR](https://www.ti.com/lit/ds/symlink/sn74cbtlv3253.pdf)

The clock generator is based on a [MS5351](https://qrp-labs.com/images/synth/ms5351m.pdf) - a SI5351 clone that't actually available and seems to have better specs: [MS5351M performance](https://qrp-labs.com/synth/ms5351m.html)

The amplification is done with a set of [LM4562MAX](https://www.ti.com/lit/ds/symlink/lm4562.pdf).

The sound card is based on [DA7212](https://www.renesas.com/kr/en/document/dst/da7212-datasheet), I'll initially test with a [IQAudio Codec Zero](https://www.sparkfun.com/products/17740) module and an existing HF SDR with similar architecture, then continue with it if it's good enough
