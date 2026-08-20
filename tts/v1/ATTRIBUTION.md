# Attribution and licenses

Voice models and phonemizer data served from this directory for the Kick
element engine's `tts` widget. Each asset keeps the license of its upstream
source; this file records those licenses and the notices they require.

Nothing here is authored by Kick. Assets are redistributed unmodified except
where noted.

## en-US — `en_US-libritts_r-medium`

| | |
|---|---|
| Files | `tts/v1/en-US/en_US-libritts_r-medium.onnx`, `.onnx.json`, `tokens.txt` |
| Voice model | [Piper](https://github.com/rhasspy/piper) VITS model, from [rhasspy/piper-voices](https://huggingface.co/rhasspy/piper-voices) |
| Training data | [LibriTTS-R](http://www.openslr.org/141/) (OpenSLR 141) |
| License | **CC BY 4.0** — https://creativecommons.org/licenses/by/4.0/ |
| Repackaging | Converted for the sherpa-onnx runtime by [k2-fsa/sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) (Apache-2.0); ONNX metadata added, weights unchanged |

**Required notice (CC BY 4.0).** Reproduce the following wherever this voice is
used in a product:

> Voice model trained on LibriTTS-R: Y. Koizumi et al., "LibriTTS-R: A Restored
> Multi-Speaker Text-to-Speech Corpus" (2023), derived from LibriTTS (H. Zen et
> al., 2019) and LibriVox public-domain audiobooks. Licensed under CC BY 4.0
> (https://creativecommons.org/licenses/by/4.0/). Model trained with Piper
> (MIT) and repackaged with sherpa-onnx (Apache-2.0). Modified: trained into a
> speech-synthesis model and converted to ONNX.

CC BY 4.0 requires the creator credit, the license notice, a link to the
license, and an indication that changes were made. Training a model on the
corpus is a change, so the modification statement is not optional.

## pt-BR — `pt_BR-cadu-medium`

| | |
|---|---|
| Files | `tts/v1/pt-BR/pt_BR-cadu-medium.onnx`, `.onnx.json` |
| Voice model | Piper VITS model, from [rhasspy/piper-voices](https://huggingface.co/rhasspy/piper-voices) |
| Training data | [OHF-Voice/voice-datasets](https://github.com/OHF-Voice/voice-datasets) |
| License | **CC0 1.0** — https://creativecommons.org/publicdomain/zero/1.0/ |

CC0 waives copyright, so no notice is required. Credit is given voluntarily.

Note: this is a male voice, and the Piper voice set contains no female
Brazilian Portuguese voice. The widget serves `pt-BR` + `female` with this
voice and reports a fallback diagnostic.

## Phonemizer data — `espeak-ng-data`

| | |
|---|---|
| File | `tts/v1/shared/espeak-ng-data.zip` |
| Source | [espeak-ng/espeak-ng](https://github.com/espeak-ng/espeak-ng), as distributed with the sherpa-onnx Piper model packages |
| License | **GPL-3.0-or-later** — https://www.gnu.org/licenses/gpl-3.0.html |

> ⚠️ **This is a copyleft license.** Both the espeak-ng library and its data
> files are GPL-3.0. Any product that links espeak-ng must comply with GPL-3.0,
> which for a proprietary application generally means providing corresponding
> source. The Piper models above declare `phoneme_type: espeak` and require
> espeak-ng phonemization at synthesis time.
>
> Legal review is required before shipping espeak-ng inside a closed-source
> application. Redistributing these data files from this host carries the same
> obligation: recipients must receive the GPL-3.0 terms and access to the
> corresponding source (https://github.com/espeak-ng/espeak-ng).

## Tooling licenses

| Project | License | Role |
|---|---|---|
| [rhasspy/piper](https://github.com/rhasspy/piper) | MIT | Voice training and model format |
| [k2-fsa/sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) | Apache-2.0 | ONNX packaging and inference runtime |
| [espeak-ng](https://github.com/espeak-ng/espeak-ng) | GPL-3.0-or-later | Text-to-phoneme conversion — see warning above |

## Where these notices must appear

CC BY 4.0 attribution has to be reachable by the end user, not just present in
this repository. A third-party-licenses screen in the app, or a linked notices
page in the streaming dashboard, satisfies it. Serving this file alone does not.
