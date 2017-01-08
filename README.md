# Cryptol implementation of NORX v3.0

## About

This repository provides a Cryptol implementation of NORX v3.0,
written by [Tim Taubert](https://timtaubert.de/).

The NORX AEAD algorithm family was designed by:

  * [Jean-Philippe Aumasson](https://aumasson.jp)
  * [Philipp Jovanovic](https://zerobyte.io)
  * [Samuel Neves](http://eden.dei.uc.pt/~sneves/)

## Usage

First, pick either the 32 or 64-bit NORX implementation. Then:

```
$ cryptol
                        _        _
   ___ _ __ _   _ _ __ | |_ ___ | |
  / __| '__| | | | '_ \| __/ _ \| |
 | (__| |  | |_| | |_) | || (_) | |
  \___|_|   \__, | .__/ \__\___/|_|
            |___/|_| version 2.4.0 (054a3e2)

Loading module Cryptol

Cryptol> :load norx.cry
Loading module Cryptol
Loading module NORX32Impl
Loading module NORX

NORX> :prove
:prove p_a1
	Q.E.D.
:prove p_a2_1_4
	Q.E.D.
:prove p_a2_1_6
	Q.E.D.
:prove p_a2_2_4
	Q.E.D.
:prove p_a2_2_6
	Q.E.D.
:prove p_a2_3_4
	Q.E.D.
:prove p_a2_3_6
	Q.E.D.
:prove p_a2_4_4
	Q.E.D.
:prove p_a2_4_6
	Q.E.D.
:prove p_a2_5_4
	Q.E.D.
:prove p_a2_5_6
	Q.E.D.
:prove p_a2_6_4
	Q.E.D.
:prove p_a2_6_6
	Q.E.D.
:prove p_a2_7_4
	Q.E.D.
:prove p_a2_7_6
	Q.E.D.
:prove p_a2_8_4
	Q.E.D.
:prove p_a2_8_6
	Q.E.D.
:prove p_a2_9_4
	Q.E.D.
:prove p_a2_9_6
	Q.E.D.
:prove p_a2_10_4
	Q.E.D.
:prove p_a2_10_6
	Q.E.D.

NORX> :quit
```

```
$ saw norx3241.saw

Loading module Cryptol
Loading file "norx3241.saw"
Loading module NORX32Impl
Loading module NORX

NORX32-4-1: verify norx_init
Successfully verified @norx_init
Time: 1.357883s
NORX32-4-1: verify norx_absorb_data
Successfully verified @norx_absorb_data
Time: 0.908516s
Successfully verified @norx_absorb_data
Time: 1.958074s
Successfully verified @norx_absorb_data
Time: 1.709996s
Successfully verified @norx_absorb_data
Time: 3.149763s
NORX32-4-1: verify norx_encrypt_data
Successfully verified @norx_encrypt_data
Time: 1.198334s
Successfully verified @norx_encrypt_data
Time: 2.307122s
Successfully verified @norx_encrypt_data
Time: 2.062518s
Successfully verified @norx_encrypt_data
Time: 3.259155s
NORX32-4-1: verify norx_decrypt_data
Successfully verified @norx_decrypt_data
Time: 1.27186s
Successfully verified @norx_decrypt_data
Time: 2.128108s
Successfully verified @norx_decrypt_data
Time: 2.348125s
Successfully verified @norx_decrypt_data
Time: 3.474382s
NORX32-4-1: verify norx_finalise
Successfully verified @norx_finalise
Time: 2.020188s
```

## License

The NORX source code is released under the [CC0 license](https://creativecommons.org/publicdomain/zero/1.0/). The full license text is included in the file `LICENSE`.
