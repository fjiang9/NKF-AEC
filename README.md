# NKF-AEC
This is the official repository of our work "Low-Complexity Acoustic Echo Cancellation with Neural Kalman Filtering" [[arXiv](https://arxiv.org/abs/2207.11388)]. \
:point_right: More results are shown on our [**Demo website**](https://fjiang9.github.io/NKF-AEC/).
## AEC Inference with the pre-trained model
The inference code and pre-trained model of NKF-AEC is released in the [_src_](https://github.com/fjiang9/NKF-AEC/tree/gh-pages/src) folder. Try NKF-AEC by running:
```
python nkf.py -x ref.wav -y mic.wav -o res.wav
```
Note: 
- NKF-AEC is a linear acoustic echo canceller.
- Time delay compensation (TDC) is necessary before running NKF if the time delay is significant (e.g., the ICASSP 2021 AEC challenge blind test set), which can be done by the [GCC-PHAT algorithm](https://ieeexplore.ieee.org/document/1162830), the [audio fingerprinting technology](https://ieeexplore.ieee.org/document/6309461), or the *WebRtcAecm_AlignedFarend* function in [WebRTC](https://webrtc.googlesource.com/src//+/eea928836755bd37dbe8ef058ca4856422d90eec/modules/audio_processing/aecm/aecm_core.h?autodive=0%2F%2F%2F%2F). In such scenarios, just add the __-a__ argument to the above command.
- The training data of the pre-trained model are derived from a small part of the AEC challenge corpus, which is introduced in the paper.
- The sampling rate of the audio is supposed to be 16 kHz.
## Cite our work
If you find this repository helpful, please cite our work:
```
@article{
 yang2022low,
 title={Low-Complexity Acoustic Echo Cancellation with Neural Kalman Filtering},
 author={Yang, Dong and Jiang, Fei and Wu, Wei and Fang, Xuefei and Cao, Muyong},
 journal={arXiv preprint arXiv:2207.11388},
 year={2022}
}
```
