# AnomalyDetectionRL


## Overview
Using Reinforcement Learning in order to detect anomalies and maybe a future response
The dataset used is NSL-KDD with data of multiple anomalies

Using deep Q-Learning with keras/tensorflow to generate the network

Code associated with the paper: "Adversarial environment reinforcement learning algorithm for intrusion detection", G Caminero, M Lopez-Martin, B Carro, 
Computer Networks, 2019
## Simple anomaly detection
- Detects normal or anomaly
- Train set in: [AD.py](https://github.com/gcamfer/Anomaly-ReactionRL/blob/master/estimators/Simple/AD.py)
- Test set in: [test.py](https://github.com/gcamfer/Anomaly-ReactionRL/blob/master/estimators/Simple/test.py)

## Multiple anomaly detection (37+1 labels)
- Detects each attack in the dataset
- Train set in: [multiAD.py](https://github.com/gcamfer/Anomaly-ReactionRL/blob/master/estimators/Multiple/multiAD.py)
- Test set in: [multi_test.py](https://github.com/gcamfer/Anomaly-ReactionRL/blob/master/estimators/Multiple/multi_test.py)

## Type anomaly detection (4+1 labels)
- Detects only the attack type between normal, DoS, Probe, R2L, U2R
- Train set in: [typeAD.py](https://github.com/gcamfer/Anomaly-ReactionRL/blob/master/estimators/Type/typeAD.py)
- Test set in: [type_test.py](https://github.com/gcamfer/Anomaly-ReactionRL/blob/master/estimators/Type/type_test.py)

- Train Dueling DDQN (tensorflow) in [typeAD_tf.py](https://github.com/gcamfer/Anomaly-ReactionRL/blob/master/estimators/Type/typeAD_tf.py)

### Adversarial/Multi Agent RL(AE-RL)
- Try to improve the inequality of attacks to produce better training
- Train set in: [adversarialAD.py](https://github.com/gcamfer/Anomaly-ReactionRL/blob/master/estimators/Multi-agent/adversarialAD.py)
- Test set in: [adversarial_test.py](https://github.com/gcamfer/Anomaly-ReactionRL/blob/master/estimators/Multi-agent/adversarial_test.py)

### A3C
- Train-Test in: [A3CtypeAD.py](https://github.com/gcamfer/Anomaly-ReactionRL/blob/master/estimators/A3C/A3CtypeAD.py)
- Summary in tensorboard: `tensorboard --logdir=tmp`

### Notebooks
- NSL-KDD adaption: [AE_RL_NSL-KDD.ipnb](https://github.com/gcamfer/Anomaly-ReactionRL/blob/master/Notebooks/AE_RL_NSL_KDD.ipynb)
- AWID adaption: [AE_RL_awid.ipnb](https://github.com/gcamfer/Anomaly-ReactionRL/blob/Notebooks/AE_RL_awid.ipnb)
