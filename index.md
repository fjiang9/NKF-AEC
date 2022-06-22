# <center>Low-Complexity Acoustic Echo Cancellation with Neural Kalman Filtering</center>

<center>Dong Yang<sup>*</sup>, Fei Jiang<sup>*</sup>, Wei Wu, Xuefei Fang, and Muyong Cao （<sup>*</sup>Equal contribution）</center>
<center>Tencent Technology</center>

## Abstract

<div style="text-align: justify"> The Kalman filter has been adopted in acoustic echo cancellation due to its robustness to double-talk, fast convergence, and tracking ability. The performance of Kalman filter is closely related to the accuracy of the state noise covariance and the observation noise covariance, which are either manually designed or estimated according to the echo cancellation results. The estimation error may lead to unacceptable results, especially when the echo path suffers abrupt changes, the tracking performance of the Kalman filter could be degraded significantly. In this paper, we propose the neural kalman filtering (NKF), which uses neural networks to implicitly model the covariance of the state noise and observation noise and to output the Kalman gain in real-time. Experimental results on both synthetic test sets and real-recorded test sets show that, the proposed NKF has superior convergence and re-convergence performance while ensuring low near-end speech degradation comparing with the state-of-the-art Kalman filters. Moreover, the proposed model size is merely 9.4 K and the RTF is as low as 0.1284, which indicates that the NKF can be deployed in low-resource platforms. </div> 

<!-- <br>
<center><img src="images/diagram.png" width="600"></center>
<br> -->

## Samples from the ICASSP 2021 AEC Challenge Blind Test Set
### Without echo path change

<!-- <div style="text-align: justify"> Separated sources: </div> 
<p style="margin-bottom : 6px;">
</p> -->
<table align="center" style="width:100%; font-size:80%">
  <thead>
    <tr>
      <th>Mic</th>
      <th>Ref</th>
      <th>WebRTC-AEC3</th>
      <th>PFDKF</th>
      <th>TFDKF</th>
      <th>NKF</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/WebRTC-AEC3/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/WebRTC-AEC3/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/WebRTC-AEC3/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/WebRTC-AEC3/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/WebRTC-AEC3/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QU5LTTDCuU2iDv4NBKf-wg_doubletalk_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QU5LTTDCuU2iDv4NBKf-wg_doubletalk_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/WebRTC-AEC3/blind_test_set_clean_doubletalk/QU5LTTDCuU2iDv4NBKf-wg_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/QU5LTTDCuU2iDv4NBKf-wg_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/QU5LTTDCuU2iDv4NBKf-wg_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 120px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/QU5LTTDCuU2iDv4NBKf-wg_doubletalk.wav"></audio></td>
    </tr>
  </tbody>
</table>
<br>

### With echo path change


