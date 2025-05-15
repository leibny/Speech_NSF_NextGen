# 🔹 Introduction
<p align="center">
  <a href="https://github.com/k2-fsa/icefall">
    <img src="https://github.com/user-attachments/assets/925352f5-ffe9-4f33-873f-c8851a7b0ddb" alt="Icefall" width="100"/>
  <a href="https://github.com/k2-fsa/k2">
    <img src="https://github.com/user-attachments/assets/d31f899e-3b76-462a-b516-6d8f44978347" alt="K2" width="100"/>
  <a href="https://github.com/lhotse-speech/lhotse">  
    <img src="https://github.com/user-attachments/assets/756c82a2-b7f3-4a90-ae21-ca754fd90fbf" alt="Lhotse" width="100"/>
</p>


The Kaldi open-source toolkit for automatic speech recognition, developed in 2009 and the subsequent follow-up trilogy Icefall, K2 and Lhotse in 2021 have shown the rapid evolution of the algorithms in speech technologies. To adapt to the new and rapid changes, such as large language models (LLMs), Hugging Face, and robust frameworks like Pytorch, this project aims to give a fresh scope according to the new necessities of the speech research community. 

#### Acknowledgments:
<img src="https://github.com/user-attachments/assets/d5796c3a-bf9c-4876-b1fe-d49689f8b133" alt="NSF Official Logo" width="50"/>
U.S. National Science Foundation, NSF-CCRI project: CCRI: ENS: Next Generation Tools for Spoken Language Science & Technology 

# 🔹 Projects

<p align="center">
  <a href="https://github.com/k2-fsa/icefall">
    <img src="https://github.com/user-attachments/assets/925352f5-ffe9-4f33-873f-c8851a7b0ddb" alt="Icefall" width="200"/>
</p>

### 🎨 Continuous Streaming Multi-Talker ASR
[We investigated](https://arxiv.org/abs/2109.08555) Streaming Unmixing and Recognition Transducer (SURT) for continuous streaming multitalker ASR, and demonstrated the effectiveness of dual-path LSTMs and Transformers for generalization to diverse session lengths (recipes for the [LibriCSS](https://github.com/k2-fsa/icefall/tree/master/egs/libricss/SURT), [AMI and ICSI](https://github.com/k2-fsa/icefall/tree/master/egs/ami/SURT) datasets).

###  🎨 SPGISpeech
We developed an [Icefall recipe](https://github.com/k2-fsa/icefall/tree/master/egs/spgispeech/ASR) and trained models ([zipformer](https://huggingface.co/desh2608/icefall-asr-spgispeech-zipformer) and [stateless transducer](https://huggingface.co/desh2608/icefall-asr-spgispeech-pruned-transducer-stateless2) models on Hugging Face) for [SPGISpeech](https://arxiv.org/abs/2104.02014), a dataset consisting of 5,000 hours of recorded company earnings calls and their respective transcriptions.

###  🎨 Contextual ASR
Developed recipes for Contextual ASR. This is the process by which an ASR system is provided with contextual information derived from metadata associated with the audio, typically in the form of a list of words or phrases likely to be spoken, with the goal of improving the recognition accuracy of named entities and other infrequent terms. Our work on Contextual ASR is recognized for introducing the ConEC dataset ([ConEC](https://github.com/huangruizhe/ConEC)), followed by a method for improving neural biasing beyond shallow language model fusion ([Pull request - Neural Biasing](https://github.com/k2-fsa/icefall/pull/1763)).


### 🎨 Omni-temporal Classification (OTC)
Training ASR systems requires large amounts of well-curated paired data. However, human annotators usually perform "non-verbatim" transcription, which can result in poorly trained models. We designed and implemented Omni-temporal Classification ([OTC](https://ieeexplore.ieee.org/abstract/document/10389684)), a novel training criterion that explicitly incorporates label uncertainties originating from such weak supervision. This allows the model to effectively learn speech-text alignments while accommodating errors present in the training transcripts ([OTC w/ BPE units](https://github.com/k2-fsa/icefall/blob/master/icefall/otc_graph_compiler.py), [OTC w/ phone units](https://github.com/k2-fsa/icefall/blob/master/icefall/otc_phone_graph_compiler.py)).

###  🎨 ASR + LID
Created a multitask learning framework that synchronizes Language Identification (LID) with ASR, utilizing a neural transducer architecture. We demonstrate the efficacy of our proposed approach on conversational multilingual (Arabic, Spanish, Mandarin) and CS (Spanish-English, Mandarin-English) test sets ([Pull request - ASR SEAME Recipe](https://github.com/k2-fsa/icefall/pull/1582)).

### 🎨 Geolocation
A functional recipe for [Geolocation](https://github.com/geolocation-from-speech/icefall/tree/geolocation/egs/radio/geolocation) dataset using Lhotse and Icefall


### 🎨 Icefall Recipies

- [Kneser-Ney smoothed language model](https://github.com/k2-fsa/icefall/blob/e79833aad278f09792deceab5962b09ae4f56378/icefall/shared/make_kn_lm.py)
- [Librispeech](https://github.com/k2-fsa/icefall/tree/e79833aad278f09792deceab5962b09ae4f56378/egs/librispeech) - partial contribution
- [MGB2](https://github.com/k2-fsa/icefall/tree/master/egs/mgb2/ASR)
- [N-gram entropy running](https://github.com/k2-fsa/icefall/blob/e79833aad278f09792deceab5962b09ae4f56378/icefall/shared/ngram_entropy_pruning.py#L4)
- [An Icefall recipe](https://github.com/k2-fsa/icefall/tree/master/egs/fluent_speech_commands/SLU) for [Fluent Speech Commands](https://www.isca-archive.org/interspeech_2019/lugosch19_interspeech.pdf), a speech dataset which transcribes short utterances (such as ”turn the lights on in the kitchen”) into action frames (such as ”action”: ”activate”, ”object”: ”lights”, ”location”: ”kitchen”).

### 🎨 JHU Collaborators
- **\#11** Piotr Żelasko, [18 commits](https://github.com/k2-fsa/icefall/commits?author=pzelasko) 🟩 993 ++ 🔴 838 --
- **\#15** Ruizhe Huang, [7 commits](https://github.com/k2-fsa/icefall/commits?author=huangruizhe) 🟩 95 ++ 🔴 74 --
- **\#38** Dongji Gao, [2 commits](https://github.com/k2-fsa/icefall/commits?author=DongjiGao) 🟩 9,565 ++ 🔴 9 --
- **\#43** Henry Li Xinyuan, [1 commit](https://github.com/k2-fsa/icefall/commits?author=HSTEHSTEHSTE) 🟩 2,124 ++ 🔴 3 --
- **\#67** Amir Hussein, [1 commit](https://github.com/k2-fsa/icefall/commits?author=AmirHussein96) 🟩 6,114 ++ 🔴 1 --
- **\#100** Jan "yenda" Trmal, [1 commit](https://github.com/k2-fsa/icefall/commits?author=jtrmal) 🟩 1 ++ 🔴 1 --

### 🎨 External Collaborators
- **\#2** Dan Povey, [200 commits](https://github.com/k2-fsa/icefall/commits?author=danpovey) 🟩 13,323 ++ 🔴 4,485 --
_______________________________________________________________________________________
<p align="center">
  <a href="https://github.com/k2-fsa/k2">
    <img src="https://github.com/user-attachments/assets/d31f899e-3b76-462a-b516-6d8f44978347" alt="K2" width="200"/>
</p>


### 🎨 k2 codes
- Fast parallel computation of longest common prefixes for eﬃcient pattern matching ([kmp-LCP](https://github.com/k2-fsa/k2/pull/804)).

### 🎨 JHU Collaborators
- **\#12** Piotr Żelasko, [4 commits](https://github.com/k2-fsa/k2/commits?author=pzelasko) 🟩 9,458 ++ 🔴 276 --
- **\#13** Jan "yenda" Trmal, [4 commits](https://github.com/k2-fsa/k2/commits?author=jtrmal) 🟩 9,314 ++ 🔴 267 --
- **\#15** Yiming Wang, [3 commits](https://github.com/k2-fsa/k2/commits?author=freewym) 🟩 234 ++ 🔴 67 --
- **\#20** Desh Raj, [2 commits](https://github.com/k2-fsa/k2/commits?author=desh2608) 🟩 435 ++ 🔴 29 --
- **\#27** Mahsa Yarmohammadi, [2 commits](https://github.com/k2-fsa/k2/commits?author=mahsa7823) 🟩 169 ++ 🔴 51 --
- **\#35** Dongji Gao, [1 commit](https://github.com/k2-fsa/k2/commits?author=DongjiGao) 🟩 27 ++ 🔴 10 --

  ### 🎨 External Collaborators
- **\#2** Dan Povey, [214 commits](https://github.com/k2-fsa/k2/commits?author=danpovey) 🟩 73,771 ++ 🔴 30,586 --



_______________________________________________________________________________________
<p align="center">
  <a href="https://github.com/lhotse-speech/lhotse">  
    <img src="https://github.com/user-attachments/assets/756c82a2-b7f3-4a90-ae21-ca754fd90fbf" alt="Lhotse" width="200"/>
</p>


### 🎨 GPU-accelerated Guided Source Separation
Improved implementation of [GSS](https://github.com/desh2608/gss) that leverages the power of modern GPU-based pipelines, such as batched processing of frequencies and segments. This allows us to perform detailed ablation studies over several parameters of the GSS algorithm. There are reproducible pipelines for speaker-attributed transcription of popular meeting benchmarks: LibriCSS, AMI, and AliMeeting.



### 🎨 Lhotse Recipes

- [recipes/aishell3.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/aishell3.py) speech/asr
- [recipes/atcosim.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/atcosim.py) speech/asr
- [recipes/but_reverb_db.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/but_reverb_db.py)  reverberation database
- [recipes/chime6.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/chime6.py) speech/asr
- [recipes/csj.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/csj.py) speech/asr
- [recipes/cmu_kids.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/cmu_kids.py)
- [recipes/dipco.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/dipco.py) speech/asr
- [recipes/edacc.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/edacc.py) speech/asr
- [recipes/gigast.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/gigaspeech.py) speech-translation
- [recipes/himia.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/himia.py) speaker-verification
- [recipes/librilight.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/librilight.py) speech/asr
- [recipes/must_c.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/must_c.py) speech-translation
- [recipes/speechcommands.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/speechcommands.py) speech/hotword-detection
- [recipes/uwb_atcc.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/uwb_atcc.py) speech/asr
- [recipes/xbmu_amdo31.py](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/xbmu_amdo31.py) speech/asr


- [Fleurs](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/fleurs.py)
- [radio stations](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/radio.py)
- [SBCASE](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/sbcsae.py)

### 🎨 JHU Collaborators
- **\#1** Piotr Żelasko, [1,221 commits](https://github.com/lhotse-speech/lhotse/commits?author=pzelasko) 🟩 110,336 ++ 🔴 43,656 --
- **\#2** Desh Raj, [248 commits](https://github.com/lhotse-speech/lhotse/commits?author=desh2608) 🟩 29,279 ++ 🔴 12,783 --
- **\#4** Jan (Yenda) Trmal, [33 commits](https://github.com/lhotse-speech/lhotse/commits?author=jtrmal) 🟩 2,093 ++ 🔴 651 --
- **\#6** Amir Hussein, [28 commits](https://github.com/lhotse-speech/lhotse/commits?author=AmirHussein96) 🟩 2,747 ++ 🔴 1766 --
- **\#13** Matthew Wiesner, [13 commits](https://github.com/lhotse-speech/lhotse/commits?author=AmirHussein96) 🟩 3,425 ++ 🔴 627 --
- **\#24** Yiming Wang, [7 commits](https://github.com/lhotse-speech/lhotse/commits?author=freewym) 🟩 215 ++ 🔴 37 --
- **\#39** Dominik Klement, [2 commits](https://github.com/lhotse-speech/lhotse/commits?author=domklement) 🟩 1602 ++ 🔴 0 --
- **\#53** Matthew Maciejewski, [1 commit](https://github.com/lhotse-speech/lhotse/commits?author=mmaciej2) 🟩 1,217 ++ 🔴 0 --
- **\#74** Henry Li Xinyuan, [1 commit](https://github.com/lhotse-speech/lhotse/commits?author=HSTEHSTEHSTE) 🟩 146 ++ 🔴 0 --
- **\#76** Dongji Gao, [1 commit](https://github.com/lhotse-speech/lhotse/commits?author=DongjiGao) 🟩 5 ++ 🔴 3 --





