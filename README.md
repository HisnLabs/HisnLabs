<p align="center">
  <img src="https://raw.githubusercontent.com/HisnLabs/Guardrino/main/assets/banner.png" alt="Guardrino by HisnLabs" width="100%">
</p>

<h1 align="center">HisnLabs · Guardrino</h1>

<p align="center">
  <b>AI security built in Dubai.</b><br>
  Guardrino guards your AI apps and agents in Arabic, its dialects, Arabizi and English.
</p>

<p align="center">
  <a href="https://hisnlabs.com/guardrino/en"><img alt="Website" src="https://img.shields.io/badge/website-hisnlabs.com-0f1417?style=for-the-badge"></a>
  <a href="https://huggingface.co/Hisnlabs"><img alt="Hugging Face" src="https://img.shields.io/badge/Hugging%20Face-Hisnlabs-f5a524?style=for-the-badge&logo=huggingface&logoColor=white"></a>
  <a href="https://x.com/hisnlabs"><img alt="X" src="https://img.shields.io/badge/X-@hisnlabs-000000?style=for-the-badge&logo=x&logoColor=white"></a>
  <a href="https://www.youtube.com/@Hisnlab"><img alt="YouTube" src="https://img.shields.io/badge/YouTube-@Hisnlab-FF0000?style=for-the-badge&logo=youtube&logoColor=white"></a>
  <a href="https://www.instagram.com/hisnlabs"><img alt="Instagram" src="https://img.shields.io/badge/Instagram-hisnlabs-E4405F?style=for-the-badge&logo=instagram&logoColor=white"></a>
  <a href="https://www.reddit.com/u/HisnLabs/"><img alt="Reddit" src="https://img.shields.io/badge/Reddit-u%2FHisnLabs-FF4500?style=for-the-badge&logo=reddit&logoColor=white"></a>
  <a href="https://huggingface.co/spaces/Hisnlabs/guardrino-demo"><img alt="Live demo" src="https://img.shields.io/badge/live%20demo-try%20it-14b8a6?style=for-the-badge"></a>
</p>

<img align="right" width="140" src="https://raw.githubusercontent.com/HisnLabs/HisnLabs/main/assets/made-in-uae-badge.png" alt="Made in UAE — Guardrino, the AI guardian">

### What Guardrino does
- **Stops prompt injection and jailbreaks**, including attacks hidden in documents, web pages and tool results
- **Masks Gulf personal data and secrets**: Emirates ID, iqama, IBAN, phone numbers, API keys
- **Follows the whole conversation** to catch slow, multi-message attacks
- **Runs on your own servers (Guardrino Sovereign) or in a cloud region in your country, or the nearest one available (Guardrino Cloud)**: the check itself never sends your messages anywhere else; where your AI model runs is your choice

**Works with:** OpenAI-compatible APIs (with streaming) · LiteLLM · MCP

<!-- arabic-comparison:start -->
### Built for Arabic. Guardrino catches nearly 9 in 10 Arabic attacks. The best-known English guards catch about 1 in 7.

<p dir="rtl" lang="ar"><b>مبنيّ للعربية. يرصد Guardrino قرابة 9 من كل 10 هجمات عربية، بينما لا ترصد أشهر أدوات الحماية الإنجليزية إلا نحو 1 من كل 7.</b></p>

| Model | Arabic attacks caught (of 7,874) | Arabizi attacks caught (of 1,523) | Safe messages blocked (of 31,348) |
|---|---|---|---|
| <img src="https://raw.githubusercontent.com/HisnLabs/HisnLabs/main/assets/made-in-uae-badge.png" height="24" alt="Made in UAE"> **Guardrino-t7 v7** | **6,814 of 7,874 (86.5%)** | **1,319 of 1,523 (87%)** | **804 of 31,348 (2.6%)** |
| **Guardrino-t7 v7, set to ArabGuard's false-block rate**<sup>‡</sup> | 6,520 of 7,874 (82.8%) | 1,214 of 1,523 (80%) | 519 of 31,348 (1.7%) |
| Ara-Prompt-Guard V1 (NAMAA, Arabic)<sup>†</sup> | 2,033 of 7,874 (25.8%) | 99 of 1,523 (7%) | 615 of 31,348 (2.0%) |
| ArabGuard (Egyptian)<sup>†</sup> | 1,553 of 7,874 (19.7%) | 2 of 1,523 (0%) | 519 of 31,348 (1.7%) |
| HARIS<sup>†</sup> | 561 of 7,874 (7.1%) | 0 of 1,523 (0%) | 459 of 31,348 (1.5%) |
| Prompt Guard 2 (Meta) | 1,128 of 7,874 (14.3%) | 73 of 1,523 (5%) | 882 of 31,348 (2.8%) |
| Protect AI v2 | 894 of 7,874 (11.4%) | 95 of 1,523 (6%) | 589 of 31,348 (1.9%) |

<sub><sup>‡</sup> The same model at a stricter threshold, so it blocks as few safe messages as ArabGuard.</sub><br>
<sub><sup>†</sup> Built for Arabic by another team, scored the same way.</sub><br>
<sub>Method: HisnLabs' own test set of 13,249 attacks and 31,348 safe messages, mostly Arabic. That favours a model trained on similar data, like ours, so this is not an independent test. Each model's threshold was set so it blocks 1 in 100 safe messages on a validation sample. Tested 26–27 October 2026. The outside models were built for English, for one dialect, or mainly for Modern Standard Arabic; this is not a criticism of them. One public source in the test set (arabic-guardrail, 2,271 attacks) may be in other models' training data, and its training split was in ours; without it, Guardrino-t7 catches 4,596 of 5,603 Arabic attacks (82%).</sub>
<!-- arabic-comparison:end -->

### Start here
| | |
|---|---|
| 🛡️ [**Guardrino**](https://github.com/HisnLabs/Guardrino) | Integrations, examples and the open model release |
| 🤗 [**Guardrino-t7 Open**](https://huggingface.co/Hisnlabs/guardrino-t7-open) | The open Arabic / Arabizi / English prompt-attack classifier |
| ✉️ **contact@hisnlabs.com** | Ask for a demo on your own traffic |

<!-- disclaimer:start -->
### Disclaimer

**Disclaimer.** Guardrino is a probabilistic security layer: it reduces risk, it does not remove it. It will sometimes miss an attack and sometimes block a legitimate message, and its results can change from one version to the next. It is not a content-moderation, medical, crisis or self-harm detection service, and it must not be the only safeguard for any decision that can cost money or cause harm to a person. Keep human oversight and your own safeguards in place. The models and code are provided "as is", without warranty of any kind. To the fullest extent permitted by applicable law, HISNLABS CYBER AI - FZCO accepts no liability for any loss or damage arising from content that Guardrino passed or blocked, including financial loss, reputational damage or harm to any person. Commercial use of the Guardrino gateway is governed by your agreement with HisnLabs.
<!-- disclaimer:end -->

<p align="center"><sub>فخورون بأننا نبني في الإمارات · Proud to be built in the UAE</sub></p>
