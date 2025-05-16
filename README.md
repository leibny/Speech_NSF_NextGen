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

The project aims at implementing all core functions of the open-source Kaldi automatic speech recognition (ASR) toolkit natively in generic AI/deep learning frameworks, primarily PyTorch, so that new advances in deep learning (e.g., novel optimization algorithms) can be seamlessly leveraged by the speech research community. Furthermore, the project incorporates automatic differentiation through finite state transducers, a core Kaldi feature responsible for its state-of-the-art performance, permitting true end-to-end training of ASR systems. These and other enhancements will make it possible to achieve two currently incompatible goals: incorporating structured, external knowledge (e.g., dialog flow models, finite state grammars, pronunciation lexicons) into fully neural ASR systems, and end-to-end training of a hybrid ASR system via backpropagation. Other goals of this proposal include providing efficient yet user-friendly data preparation and model management tools for large-scale training of ASR systems and capabilities for robust conversation analysis and speaker diarization needed by researchers who use ASR as a tool for other scientific inquiries.

#### Acknowledgments:

[<img src="https://github.com/user-attachments/assets/d5796c3a-bf9c-4876-b1fe-d49689f8b133" alt="NSF Official Logo" width="50"/>](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2120435&HistoricalAwards=false)
 This project was supported by U.S. National Science Foundation Award Number:2120435, NSF-CCRI project: CCRI: ENS: Next Generation Tools for Spoken Language Science & Technology. 

# 🔹 Projects

<p align="center">
  <a href="https://github.com/lhotse-speech/lhotse">  
    <img src="https://github.com/user-attachments/assets/756c82a2-b7f3-4a90-ae21-ca754fd90fbf" alt="Lhotse" width="200"/>
</p>

Lhotse develops a modern approach to speech data preparation. Its design is inspired by data libraries commonly used in the ML community, such as pandas. Lhotse's philosophy may be summarized as ''simple things should be simple, complex things should be possible.'' 

### 🎨 JHU Contributors
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

### 🎨 GPU-accelerated Guided Source Separation (by [Desh Raj](https://desh2608.github.io/))
Improved implementation of [GSS](https://github.com/desh2608/gss) that leverages the power of modern GPU-based pipelines, such as batched processing of frequencies and segments. This allows us to perform detailed ablation studies over several parameters of the GSS algorithm. There are reproducible pipelines for speaker-attributed transcription of popular meeting benchmarks: LibriCSS, AMI, and AliMeeting.



### 🎨 Lhotse recipes

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


_______________________________________________________________________________________

<p align="center">
  <a href="https://github.com/k2-fsa/icefall">
    <img src="https://github.com/user-attachments/assets/925352f5-ffe9-4f33-873f-c8851a7b0ddb" alt="Icefall" width="200"/>
</p>

Icefall is the project where K2 and Lhotse ''meet''. It provides the speech and language research community a comprehensive collection of recipes for training modern speech processing systems on most of the popular speech data sets.  

### 🎨 JHU Contributors
- **\#11** Piotr Żelasko, [18 commits](https://github.com/k2-fsa/icefall/commits?author=pzelasko) 🟩 993 ++ 🔴 838 --
- **\#15** Ruizhe Huang, [7 commits](https://github.com/k2-fsa/icefall/commits?author=huangruizhe) 🟩 95 ++ 🔴 74 --
- **\#38** Dongji Gao, [2 commits](https://github.com/k2-fsa/icefall/commits?author=DongjiGao) 🟩 9,565 ++ 🔴 9 --
- **\#43** Henry Li Xinyuan, [1 commit](https://github.com/k2-fsa/icefall/commits?author=HSTEHSTEHSTE) 🟩 2,124 ++ 🔴 3 --
- **\#67** Amir Hussein, [1 commit](https://github.com/k2-fsa/icefall/commits?author=AmirHussein96) 🟩 6,114 ++ 🔴 1 --
- **\#100** Jan "yenda" Trmal, [1 commit](https://github.com/k2-fsa/icefall/commits?author=jtrmal) 🟩 1 ++ 🔴 1 --

### 🎨 External Contributors
- **\#2** Dan Povey, [200 commits](https://github.com/k2-fsa/icefall/commits?author=danpovey) 🟩 13,323 ++ 🔴 4,485 --

### 🎨 Continuous Streaming Multi-Talker ASR (by [Desh Raj](https://desh2608.github.io/))
[We investigated](https://arxiv.org/abs/2109.08555) Streaming Unmixing and Recognition Transducer (SURT) for continuous streaming multitalker ASR, and demonstrated the effectiveness of dual-path LSTMs and Transformers for generalization to diverse session lengths (recipes for the [LibriCSS](https://github.com/k2-fsa/icefall/tree/master/egs/libricss/SURT), [AMI and ICSI](https://github.com/k2-fsa/icefall/tree/master/egs/ami/SURT) datasets).

###  🎨 SPGISpeech (by [Desh Raj](https://desh2608.github.io/))
We developed an [Icefall recipe](https://github.com/k2-fsa/icefall/tree/master/egs/spgispeech/ASR) and trained models ([zipformer](https://huggingface.co/desh2608/icefall-asr-spgispeech-zipformer) and [stateless transducer](https://huggingface.co/desh2608/icefall-asr-spgispeech-pruned-transducer-stateless2) models on Hugging Face) for [SPGISpeech](https://arxiv.org/abs/2104.02014), a dataset consisting of 5,000 hours of recorded company earnings calls and their respective transcriptions.

###  🎨 MGB-2 (by [Amir Hussein](https://github.com/AmirHussein96))
We developed an [Icefall recipe](https://github.com/k2-fsa/icefall/tree/master/egs/mgb2/ASR) and trained a model ([conformer-ctc](https://huggingface.co/AmirHussein/icefall-asr-mgb2-conformer_ctc-2022-27-06) model on Hugging Face) for [Multi-Dialect Broadcast News Arabic Speech Recognition (MGB-2)](https://ieeexplore.ieee.org/abstract/document/7846277) challenge on Arabic multi-dialect broadcast media recognition.

###  🎨 Contextual ASR (by Ruizhe Huang, co-advised by Mahsa Yarmohammadi)
Developed recipes for Contextual ASR. This is the process by which an ASR system is provided with contextual information derived from metadata associated with the audio, typically in the form of a list of words or phrases likely to be spoken, with the goal of improving the recognition accuracy of named entities and other infrequent terms. Our work on Contextual ASR is recognized for introducing the ConEC dataset ([ConEC](https://github.com/huangruizhe/ConEC)), followed by a method for improving neural biasing beyond shallow language model fusion ([Pull request - Neural Biasing](https://github.com/k2-fsa/icefall/pull/1763)).


### 🎨 Omni-temporal Classification (OTC) (by Dongji Gao)
Training ASR systems requires large amounts of well-curated paired data. However, human annotators usually perform "non-verbatim" transcription, which can result in poorly trained models. We designed and implemented Omni-temporal Classification ([OTC](https://ieeexplore.ieee.org/abstract/document/10389684)), a novel training criterion that explicitly incorporates label uncertainties originating from such weak supervision. This allows the model to effectively learn speech-text alignments while accommodating errors present in the training transcripts ([OTC w/ BPE units](https://github.com/k2-fsa/icefall/blob/master/icefall/otc_graph_compiler.py), [OTC w/ phone units](https://github.com/k2-fsa/icefall/blob/master/icefall/otc_phone_graph_compiler.py)).

###  🎨 ASR + LID (by [Amir Hussein](https://github.com/AmirHussein96))
Created a multitask learning framework that synchronizes Language Identification (LID) with ASR, utilizing a neural transducer architecture. We demonstrate the efficacy of our proposed approach on conversational multilingual (Arabic, Spanish, Mandarin) and CS (Spanish-English, Mandarin-English) test sets ([Pull request - ASR SEAME Recipe](https://github.com/k2-fsa/icefall/pull/1582)).

### 🎨 Other recipes

- [Kneser-Ney language model smoothing](https://github.com/k2-fsa/icefall/blob/e79833aad278f09792deceab5962b09ae4f56378/icefall/shared/make_kn_lm.py)
- [Librispeech](https://github.com/k2-fsa/icefall/tree/e79833aad278f09792deceab5962b09ae4f56378/egs/librispeech) - partial contribution
- [Fluent Speech Commands recipe](https://github.com/k2-fsa/icefall/tree/master/egs/fluent_speech_commands/SLU)
- Recipe for [Geolocation](https://github.com/geolocation-from-speech/icefall/tree/geolocation/egs/radio/geolocation) dataset using Lhotse and Icefall

_______________________________________________________________________________________
<p align="center">
  <a href="https://github.com/k2-fsa/k2">
    <img src="https://github.com/user-attachments/assets/d31f899e-3b76-462a-b516-6d8f44978347" alt="K2" width="200"/>
</p>

K2 brings data structures and algorithms from the field of finite state automata (FSA) into the world of deep learning. It provides efficient CPU and GPU implementations of commonly used FSA operations and integrates them seamlessly with PyTorch's tensor and automatic differentiation mechanisms, thus admitting - and benefiting from - the inner complexity of the speech recognition, instead of trying to remove it.
### 🎨 JHU Contributors
- **\#12** Piotr Żelasko, [4 commits](https://github.com/k2-fsa/k2/commits?author=pzelasko) 🟩 9,458 ++ 🔴 276 --
- **\#13** Jan "yenda" Trmal, [4 commits](https://github.com/k2-fsa/k2/commits?author=jtrmal) 🟩 9,314 ++ 🔴 267 --
- **\#15** Yiming Wang, [3 commits](https://github.com/k2-fsa/k2/commits?author=freewym) 🟩 234 ++ 🔴 67 --
- **\#20** Desh Raj, [2 commits](https://github.com/k2-fsa/k2/commits?author=desh2608) 🟩 435 ++ 🔴 29 --
- **\#27** Mahsa Yarmohammadi, [2 commits](https://github.com/k2-fsa/k2/commits?author=mahsa7823) 🟩 169 ++ 🔴 51 --
- **\#35** Dongji Gao, [1 commit](https://github.com/k2-fsa/k2/commits?author=DongjiGao) 🟩 27 ++ 🔴 10 --

### 🎨 External Contributors
- **\#2** Dan Povey, [214 commits](https://github.com/k2-fsa/k2/commits?author=danpovey) 🟩 73,771 ++ 🔴 30,586 --

### 🎨 k2 codes
- Fast parallel computation of longest common prefixes for eﬃcient pattern matching ([kmp-LCP](https://github.com/k2-fsa/k2/pull/804)).
- Implementation of the Hybrid Autoregressive Transducer loss ([HAT](https://github.com/k2-fsa/k2/pull/1244)).
