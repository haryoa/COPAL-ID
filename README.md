# 🏺COPAL-ID (Choice of Plausible Alternatives Local Nuances - Indonesia) 

![test](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)

Welcome folks! 🎉🎉

This repository contains data from our research: COPAL-ID: Indonesian Language Reasoning with Local Culture and Nuances [Arxiv Link](https://arxiv.org/abs/2311.01012)! 

Our dataset comprises 559 instances that test Common Sense Reasoning (CSR). This task focuses on Indonesian local nuances and culture and is presented in COPA style. Here are a few examples of our data:

|Premise|Choice 1|Choice 2|Question Type|Label|
|-------|---|--|--|--|
|Penumpang angkutan umum ingin turun di jalan.|Penumpang teriak "kanan"|Penumpang teriak "kiri"|effect|Choice 2
|Dia merasa masuk angin|Dia membuka jendela untuk meperbaiki sirkulasi udara|Dia meminta tolong untuk kerokan|effect|Choice 2|
|Kemarin malam, ia baru selesai jaga lilin.|Ia adalah orang yang taat beribadah|Ia percaya dengan ilmu hitam|cause|Choice 2|
Ia dibawa ke kantor polisi akibat mencuri televisi|Ia tertangkap basah membawa televisi|Ia membawa televisi dengan tangan merah|cause|Choice 1|

## How to run our benchmark

You can use `lm-evaluation-harness` (install from this repository: https://github.com/EleutherAI/lm-evaluation-harness) and select `copal_id_standard` or `copal_id_colloquial` tasks.

For instance, run this command directly on your `cli`:

**Standard COPAL ID**
```
lm_eval --model hf --model_args pretrained=MODEL --tasks copal_id_standard --device cuda:0 --batch_size 8
```

**Colloquial COPAL ID**
```
lm_eval --model hf --model_args pretrained=MODEL --tasks copal_id_colloquial --device cuda:0 --batch_size 8
```

Change `MODEL` and the arguments accordingly.

## Data

Our data can be downloaded on [Hugging Face](https://huggingface.co/datasets/haryoaw/COPAL) or you can just clone this repository and get the content of `/data`.

1. `test_copal.csv` contains COPAL-ID
2. `test_copal_colloquial.csv` contains the colloquial version of COPAL-ID

Further detailed information will be provided in the future!


## Code

We use `lm-evaluation-harness` instead.

## Cite Our Work

```
@article{wibowo2023copal,
  title={COPAL-ID: Indonesian Language Reasoning with Local Culture and Nuances},
  author={Wibowo, Haryo Akbarianto and Fuadi, Erland Hilman and Nityasya, Made Nindyatama and Prasojo, Radityo Eko and Aji, Alham Fikri},
  journal={arXiv preprint arXiv:2311.01012},
  year={2023}
}
```

## Team

![Cultured](img/cultured.png)


1. Haryo Akbarianto Wibowo @ MBZUAI
2. Erland Hilman Fuadi @ Independent Researcher
3. Made Nindyatama Nityasya @ Independent Researcher
4. Radityo Eko Prasojo @ Independent Researcher
5. Alham Fikri Aji @ MBZUAI
