---
title: "DarKnight: An accelerated framework for privacy and integrity preserving deep learning using trusted hardware"
collection: publications
permalink: /publications/2021-10-18-darknight
excerpt:
date: 2021-10-18
venue: '2021 IEEE/ACM 54th International Symposium on Microarchitecture (MICRO)'
paperurl: 'https://dl.acm.org/doi/abs/10.1145/3466752.3480112'
citation: 'Hanieh Hashemi, Yongqin Wang, and Murali Annavaram. 2021. DarKnight: An Accelerated Framework for Privacy and Integrity Preserving Deep Learning Using Trusted Hardware. In MICRO-54: 54th Annual IEEE/ACM International Symposium on Microarchitecture (MICRO).'
---
Privacy and security-related concerns are growing as machine learning reaches diverse application domains. The data holders want to train or infer with private data while exploiting accelerators, such as GPUs, that are hosted in the cloud. Cloud systems are vulnerable to attackers that compromise the privacy of data and integrity of computations. Tackling such a challenge requires unifying theoretical privacy algorithms with hardware security capabilities. This paper presents DarKnight, a framework for large DNN training while protecting input privacy and computation integrity. DarKnight relies on cooperative execution between trusted execution environments (TEE) and accelerators, where the TEE provides privacy and integrity verification, while accelerators perform the bulk of the linear algebraic computation to optimize the performance. In particular, DarKnight uses a customized data encoding strategy based on matrix masking to create input obfuscation within a TEE. The obfuscated data is then offloaded to GPUs for fast linear algebraic computation. DarKnight’s data obfuscation strategy provides provable data privacy and computation integrity in the cloud servers. While prior works tackle inference privacy and cannot be utilized for training, DarKnight’s encoding scheme is designed to support both training and inference.
[Download paper here](https://dl.acm.org/doi/abs/10.1145/3466752.3480112)

