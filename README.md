# Introduction



The Kaldi open-source toolkit for automatic speech recognition, developed in 2009 and the subsequent follow-up trilogy Icefall, K2 and Lhotse in 2021 have shown the rapid evolution of the algorithms in speech technologies. To adapt to the new and rapid changes such as large language models (LLMs), Hugging Face, and robust frameworks like Pythorch, this project aims to give a fresh scope according to the new necessities of the speech research community. 

# Projects

## Icefall

## K2

## Lhotse

## Contextual ASR
Developed recipes for Contextual ASR. This is the process by which an ASR system is provided with contextual information derived from metadata associated with the audio, typically in the form of a list of words or phrases likely to be spoken, with the goal of improving the recognition accuracy of named entities and other infrequent terms. Our work on Contextual ASR is recognized for introducing the ConEC dataset ([ConEC](https://github.com/huangruizhe/ConEC)), followed by a method for improving neural biasing beyond shallow language model fusion ([Pull request - Neural Biasing](https://github.com/k2-fsa/icefall/pull/1763)).

## GPU-accelerated Guided Source Separation
Improved implementation of [GSS](https://github.com/desh2608/gss) that leverages the power of modern GPU-based pipelines, such as batched processing of frequencies and segments. This allows us to perform detailed ablation studies over several parameters of the GSS algorithm. There are reproducible pipelines for speaker-attributed transcription of popular meeting benchmarks: LibriCSS, AMI, and AliMeeting.

## Omni-temporal Classification (OTC)
Design and implementation of Omni-temporal Classification (OTC), a novel training criterion that explicitly incorporates label uncertainties originating from such weak supervision, code was committed to Icefall.

## ASR + LID
Created a multitask learning framework that synchronizes Language Identification (LID) with ASR, utilizing a neural transducer architecture. We demonstrate the efficacy of our proposed approach on conversational multilingual (Arabic, Spanish, Mandarin) and CS (Spanish-English, Mandarin-English) test sets ([Pull request - ASR SEAME Recipe](https://github.com/k2-fsa/icefall/pull/1582)).

## k2 codes
- Fast parallel computation of longest common prefixes for eﬃcient pattern matching ([kmp-LCP](https://github.com/k2-fsa/k2/pull/804)).

## lhotse Recipes
- [Fleurs](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/fleurs.py)
- [radio stations](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/radio.py)
- [SBCASE](https://github.com/lhotse-speech/lhotse/blob/master/lhotse/recipes/sbcsae.py)
- a functional recipe for [Geolocation](https://github.com/geolocation-from-speech/icefall/tree/geolocation/egs/radio/geolocation) dataset using Lhotse and Icefall

## Icefall Recepies
- [SPGISpeech](https://github.com/k2-fsa/icefall/tree/master/egs/spgispeech/ASR)
- [An Icefall recipe](https://github.com/k2-fsa/icefall/tree/master/egs/fluent_speech_commands/SLU) for [Fluent Speech Commands](https://www.isca-archive.org/interspeech_2019/lugosch19_interspeech.pdf), a speech dataset which transcribes short utterances (such as ”turn the lights on in the kitchen”) into action frames (such as ”action”: ”activate”, ”object”: ”lights”, ”location”: ”kitchen”).
