# mingzhi-assets

明知AI剪辑（[crawfordxx/mingzhi](https://github.com/crawfordxx/mingzhi)）的可再分发素材：配乐（CC0）、字体（SIL OFL）、模型。
启动器首次运行时从这里下载（jsDelivr 在前，raw.githubusercontent.com 其次），不需要手动操作。

英文简介见文末 / English summary at the bottom.

## 用途与约定

- 只放许可明确允许再分发的文件；每个文件原样不改（配乐除外，见下）。
- 单个文件不超过 20 MB（jsDelivr 的限制）。更大的文件（例如 LXGW 文楷 24 MB、Noto Serif SC 24 MB、SenseVoice 模型 228 MB）不在这里，启动器直接用它们的原始来源。
- 内容按标签发布，标签永不移动：`v1` 对应本目录现有内容。要换文件会发新标签，旧标签继续可用。
- 下载地址：`https://cdn.jsdelivr.net/gh/crawfordxx/mingzhi-assets@v1/<路径>`，或 `https://raw.githubusercontent.com/crawfordxx/mingzhi-assets/v1/<路径>`。
- 所有文件的 sha256 见下表和根目录的 `SHA256SUMS`（`shasum -a 256 -c SHA256SUMS` 可校验）。

## 配乐（CC0 1.0）

作者 [HoliznaCC0](https://opengameart.org/users/holizna)，发布在 OpenGameArt，许可为 [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/)（[全文](licenses/CC0-1.0.txt)，公有领域贡献，可自由使用、修改、再分发，包括商用，无需署名；这里仍保留来源）。
转码方式：从原始压缩包取出对应曲目，用 ffmpeg 转为 MP3，立体声、44.1 kHz、192 kbps（`-vn -map_metadata -1 -ac 2 -ar 44100 -b:a 192k`），只写入标题与作者标签。CC0 允许修改，所以转码后的文件同样是 CC0。共 19 首。

| 文件 | 曲目 | 原始来源（OpenGameArt） | 大小 | sha256 |
|---|---|---|---|---|
| `music/families.mp3` | Families | [Chill Beats (Collection)](https://opengameart.org/content/chill-beats-collection) | 3.3 MB | `7d1124254c1b9163bf968226c4a69db3daf4a6a338d6ff612b1786a279ded1fb` |
| `music/opinions.mp3` | Opinions | [Chill Beats (Collection)](https://opengameart.org/content/chill-beats-collection) | 3.8 MB | `b2f4814a7cad4b14f69a5e8acfdf39257d06912c60d44c08a9366d88f99a7426` |
| `music/old-age.mp3` | Old Age | [Chill Beats (Collection)](https://opengameart.org/content/chill-beats-collection) | 4.9 MB | `f0ea08ffe1c37f38484c77bf2067312a3196e54ea4f127a141af339004ce06f9` |
| `music/dream-pop.mp3` | Dream Pop | [Chill Beats (Collection)](https://opengameart.org/content/chill-beats-collection) | 5.5 MB | `bb7b43384ac4843c1f263d9c8e98e34c42c2b1d24bf3fd042f6a69da92dd5e97` |
| `music/autumn.mp3` | Autumn | [Chill Beats (Collection)](https://opengameart.org/content/chill-beats-collection) | 3.9 MB | `495329971d9ee1a6323f089e87fa87ac22517d9fbf617d0eb7c63769c1e7f1b4` |
| `music/poor-but-happy.mp3` | Poor, But Happy | [Happy Lo-Fi (Lofi Collection)](https://opengameart.org/content/happy-lo-fi-lofi-collection) | 2.9 MB | `7d35876d16f82443a8e07d58b664509408ab7fc983289ce930299181a96ce954` |
| `music/blue-skies.mp3` | Blue Skies | [Happy Lo-Fi (Lofi Collection)](https://opengameart.org/content/happy-lo-fi-lofi-collection) | 4.0 MB | `0452b64d443389d81333a7a9b32622ff8b9491eb4324e09a829fd3166044edb3` |
| `music/letting-go.mp3` | Letting Go Of The Past | [Happy Lo-Fi (Lofi Collection)](https://opengameart.org/content/happy-lo-fi-lofi-collection) | 4.1 MB | `3553abda66d40b74373c2240fa0b9950a471feace8fd7f4ace465bb9f50210e7` |
| `music/puppy-love.mp3` | Puppy Love | [Happy Lo-Fi (Lofi Collection)](https://opengameart.org/content/happy-lo-fi-lofi-collection) | 3.4 MB | `cc0c39b0b60acb40a6360b12573a11351a4b19108a051d19358e18ab405dec93` |
| `music/clouds.mp3` | Clouds | [Happy Lo-Fi (Lofi Collection)](https://opengameart.org/content/happy-lo-fi-lofi-collection) | 5.3 MB | `53806c7dc3a658adb5bea976c691a64d848b191ec611a36866c773e97b9a8b5e` |
| `music/a-little-off.mp3` | Happy, but a little off | [Happy Lo-Fi (Lofi Collection)](https://opengameart.org/content/happy-lo-fi-lofi-collection) | 2.7 MB | `d915a461e8d17138ccbb30ae03d11ffd3f7051409ba116eb12581564a5e057a9` |
| `music/new-shoes.mp3` | New Shoes | [Happy Lo-Fi (Lofi Collection)](https://opengameart.org/content/happy-lo-fi-lofi-collection) | 3.6 MB | `907fdd07c1d443ea24767bd56f89b75f78330fd9a46d067bd9fae8d89f3f39ec` |
| `music/back-in-the-80s.mp3` | Back In The 80s | [Happy Pop Electronic (Collection)](https://opengameart.org/content/happy-pop-electronic-collection) | 5.5 MB | `c55562654a83090d8101db1a604a2f7c2e06e063b097fed1ff02c5c8ecded9c3` |
| `music/earth.mp3` | Earth | [Happy Pop Electronic (Collection)](https://opengameart.org/content/happy-pop-electronic-collection) | 4.6 MB | `ef9172f03793fbf3a2af0509b8f1d260e1d611f86fa27b19a1efc0f32541656b` |
| `music/small-town-on-pluto.mp3` | A Small Town On Pluto | [Happy Pop Electronic (Collection)](https://opengameart.org/content/happy-pop-electronic-collection) | 5.3 MB | `736a3280f20b341eadea51db9e3f8960aa56c6c8a3574566fb3fba35ed6c3367` |
| `music/happy-dance.mp3` | Happy Dance | [Happy Pop Electronic (Collection)](https://opengameart.org/content/happy-pop-electronic-collection) | 3.6 MB | `8ef08431c67f9e35b28ccb506c863c6d5963d85d3192c67e7d12ab3aaab324a8` |
| `music/earth-people.mp3` | transcendental earth people | [Happy Pop Electronic (Collection)](https://opengameart.org/content/happy-pop-electronic-collection) | 3.5 MB | `e5624f12fc7164ceddc48c2501b8cc94aa6cd1877e1268ca6d7f76a9e95e9f02` |
| `music/bouncing.mp3` | Bouncing | [Happy Pop Electronic (Collection)](https://opengameart.org/content/happy-pop-electronic-collection) | 2.0 MB | `34e0925f1eb6e1c55a7b3b27b0ca2b95c22b35879a89be6169fa0644df271fda` |
| `music/love-love-love.mp3` | Love Love Love | [Happy Pop Electronic (Collection)](https://opengameart.org/content/happy-pop-electronic-collection) | 4.0 MB | `0b535a806f0df8b97e9892f1f040b15667a5c277bc2a07aedb075d481ca3a596` |

## 字体（SIL Open Font License 1.1）

四款字体均为上游原文件，未经修改，随附各自的 OFL 全文。按 OFL，字体可以免费使用、嵌入、再分发，但不能单独出售，保留字体名（Reserved Font Name）的字体不得以修改版沿用原名。

| 文件 | 字体 | 许可 | 来源 | 大小 | sha256 |
|---|---|---|---|---|---|
| `fonts/NotoSansSC-VF.ttf` | Noto Sans SC（可变字体） | SIL OFL 1.1（[全文](licenses/OFL-notosanssc.txt)） | [上游](https://github.com/google/fonts/tree/1d0e46c7933245c8180fe83e47917961c913bbdb/ofl/notosanssc) | 16.9 MB | `a3041811a78c361b1de50f953c805e0244951c21c5bd412f7232ef0d899af0da` |
| `fonts/ZCOOLKuaiLe-Regular.ttf` | 站酷快乐体 ZCOOL KuaiLe | SIL OFL 1.1（[全文](licenses/OFL-zcoolkuaile.txt)） | [上游](https://github.com/google/fonts/tree/1d0e46c7933245c8180fe83e47917961c913bbdb/ofl/zcoolkuaile) | 1.4 MB | `812a6fc1fe54b6d73a419245c32dfeba8aa33104d5be90d1cf6af082007cb71d` |
| `fonts/ZCOOLQingKeHuangYou-Regular.ttf` | 站酷庆科黄油体 ZCOOL QingKe HuangYou | SIL OFL 1.1（[全文](licenses/OFL-zcoolqingkehuangyou.txt)） | [上游](https://github.com/google/fonts/tree/1d0e46c7933245c8180fe83e47917961c913bbdb/ofl/zcoolqingkehuangyou) | 7.9 MB | `54f0c0df4308cd74cd0f2fd3494ae054dbc4a1fd6fa7d71f4807eb4cdd8b4136` |
| `fonts/SmileySans-Oblique.ttf` | 得意黑 Smiley Sans（Oblique，v2.0.1） | SIL OFL 1.1（保留字体名 Smiley / 得意黑）（[全文](licenses/OFL-smiley-sans.txt)） | [上游](https://github.com/atelier-anchor/smiley-sans/releases/tag/v2.0.1) | 2.5 MB | `b447d7e781f08bc95c4c9f23ba71ed2b8ebb639aa7184485c71c4ca5afcd25c4` |

## 模型

| 文件 | 模型 | 许可 | 来源 | 大小 | sha256 |
|---|---|---|---|---|---|
| `models/silero_vad.onnx` | Silero VAD（语音活动检测） | MIT（[全文](licenses/LICENSE-silero-vad-MIT.txt)） | [snakers4/silero-vad](https://github.com/snakers4/silero-vad)；文件取自 [sherpa-onnx asr-models](https://github.com/k2-fsa/sherpa-onnx/releases/tag/asr-models) | 0.6 MB | `9e2449e1087496d8d4caba907f23e0bd3f78d91fa552479bb9c23ac09cbb1fd6` |
| `models/rvm_mobilenetv3_fp32.onnx` | RobustVideoMatting（MobileNetV3，fp32，抠像） | GPL-3.0（[全文](licenses/LICENSE-RobustVideoMatting-GPL-3.0.txt)） | [PeterL1n/RobustVideoMatting](https://github.com/PeterL1n/RobustVideoMatting) release v1.0.0；上游源码即对应源码 | 14.3 MB | `88d4531297118f595bf2fd60f6f566aec2e559393802d1f436c380f0cbbd2828` |

`rvm_mobilenetv3_fp32.onnx` 按 GPL-3.0 再分发：随附 GPL-3.0 全文，对应源码见上游仓库 [PeterL1n/RobustVideoMatting](https://github.com/PeterL1n/RobustVideoMatting)。
SenseVoice 模型（FunASR Model Open Source License）体积 228 MB，超过 20 MB 限制，且许可需单独逐条核对，因此不放在这里。

## English summary

Redistributable assets for the "Mingzhi AI Cut" launcher ([crawfordxx/mingzhi](https://github.com/crawfordxx/mingzhi)): 19 CC0 music tracks by HoliznaCC0 (OpenGameArt, transcoded to 192 kbps stereo MP3), 4 unmodified SIL OFL 1.1 fonts, and two models (Silero VAD, MIT; RobustVideoMatting, GPL-3.0 with upstream source linked). Every file is at most 20 MB so it can be served by jsDelivr. Files are published under immutable tags (`v1`); sha256 sums are in the tables above and in `SHA256SUMS`. Files larger than 20 MB or with licences that need separate review are intentionally not mirrored here.
