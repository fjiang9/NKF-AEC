# <center>Low-Complexity Acoustic Echo Cancellation with Neural Kalman Filtering</center>

<center>Dong Yang<sup>*</sup>, Fei Jiang<sup>*</sup>, Wei Wu, Xuefei Fang, and Muyong Cao</center>
<center>Tencent Technology</center>
<center> (<sup>*</sup>Equal contribution)</center>

## Abstract

<div style="text-align: justify; width: 100%"> The Kalman filter has been adopted in acoustic echo cancellation due to its robustness to double-talk, fast convergence, and tracking ability. The performance of Kalman filter is closely related to the accuracy of the state noise covariance and the observation noise covariance, which are either manually designed or estimated according to the echo cancellation results. The estimation error may lead to unacceptable results, especially when the echo path suffers abrupt changes, the tracking performance of the Kalman filter could be degraded significantly. In this paper, we propose the neural kalman filtering (NKF), which uses neural networks to implicitly model the covariance of the state noise and observation noise and to output the Kalman gain in real-time. Experimental results on both synthetic test sets and real-recorded test sets show that, the proposed NKF has superior convergence and re-convergence performance while ensuring low near-end speech degradation comparing with the state-of-the-art Kalman filters. Moreover, the proposed model size is merely 5.3 K and the RTF is as low as 0.09, which indicates that the NKF can be deployed in low-resource platforms. </div> 

## Results
### Synthetic Test Set
<center><img src="figures/fig_erle.png" width="1200"></center>
<center> (Averaged ERLE curves of the synthetic double-talk test set. Abrupt echo path change occurs at the shaded region. RNN-AEC refers to the baseline model of Interspeech 2021 AEC challenge.)</center>
<center><img src="figures/fig_spec.png" width="1200"></center>
<center> (Mel spectrograms of the first test sample below.)</center>

#### Double-talk with abrupt echo path change
<table align="center" style="width:130%; font-size:80%">
  <thead>
    <tr>
      <th style="width:100px">Mic</th>
      <th>GT</th>
      <th>PNLMS</th>
      <th>PFDKF</th>
      <th>TFDKF</th>
      <th>RNN-AEC</th>
      <th>Meta-AF</th>
      <th>NKF (proposed)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test99_-1.05dB_epc4.21s__mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test99_-1.05dB_epc4.21s__gt.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/syn_test_dt_epc/test99_-1.05dB_epc4.21s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/syn_test_dt_epc/test99_-1.05dB_epc4.21s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/syn_test_dt_epc/test99_-1.05dB_epc4.21s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/syn_test_dt_epc/test99_-1.05dB_epc4.21s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/syn_test_dt_epc/test99_-1.05dB_epc4.21s.wav"></audio></td>      
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test99_-1.05dB_epc4.21s.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test199_-0.67dB_epc3.51s__mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test199_-0.67dB_epc3.51s__gt.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/syn_test_dt_epc/test199_-0.67dB_epc3.51s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/syn_test_dt_epc/test199_-0.67dB_epc3.51s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/syn_test_dt_epc/test199_-0.67dB_epc3.51s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/syn_test_dt_epc/test199_-0.67dB_epc3.51s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/syn_test_dt_epc/test199_-0.67dB_epc3.51s.wav"></audio></td>      
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test199_-0.67dB_epc3.51s.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test299_-4.37dB_epc4.25s__mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test299_-4.37dB_epc4.25s__gt.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/syn_test_dt_epc/test299_-4.37dB_epc4.25s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/syn_test_dt_epc/test299_-4.37dB_epc4.25s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/syn_test_dt_epc/test299_-4.37dB_epc4.25s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/syn_test_dt_epc/test299_-4.37dB_epc4.25s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/syn_test_dt_epc/test299_-4.37dB_epc4.25s.wav"></audio></td>      
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test299_-4.37dB_epc4.25s.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test399_8.36dB_epc4.15s__mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test399_8.36dB_epc4.15s__gt.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/syn_test_dt_epc/test399_8.36dB_epc4.15s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/syn_test_dt_epc/test399_8.36dB_epc4.15s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/syn_test_dt_epc/test399_8.36dB_epc4.15s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/syn_test_dt_epc/test399_8.36dB_epc4.15s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/syn_test_dt_epc/test399_8.36dB_epc4.15s.wav"></audio></td>      
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test399_8.36dB_epc4.15s.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test499_-4.47dB_epc4.31s__mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test499_-4.47dB_epc4.31s__gt.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/syn_test_dt_epc/test499_-4.47dB_epc4.31s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/syn_test_dt_epc/test499_-4.47dB_epc4.31s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/syn_test_dt_epc/test499_-4.47dB_epc4.31s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/syn_test_dt_epc/test499_-4.47dB_epc4.31s.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/syn_test_dt_epc/test499_-4.47dB_epc4.31s.wav"></audio></td>      
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/syn_test_dt_epc/test499_-4.47dB_epc4.31s.wav"></audio></td>
    </tr>
  </tbody>
</table>


### Blind Test Set of ICASSP 2021 AEC Challenge
#### Without echo path change
<!-- <div style="text-align: justify"> Separated sources: </div> 
<p style="margin-bottom : 6px;">
</p> -->
<table align="center" style="width:130%; font-size:80%">
  <thead>
    <tr>
      <th>Mic</th>
      <th>Ref</th>
      <th>PNLMS</th>
      <th>PFDKF</th>
      <th>TFDKF</th>
      <th>RNN-AEC</th>
      <th>Meta-AF</th>
      <th>NKF (proposed)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk.wav"></audio></td>      
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk.wav"></audio></td>  
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk.wav"></audio></td>  
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk.wav"></audio></td> 
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk.wav"></audio></td> 
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk.wav"></audio></td>
    </tr>
  </tbody>
</table>

#### With echo path change
<table align="center" style="width:130%; font-size:80%">
  <thead>
    <tr>
      <th>Mic</th>
      <th>Ref</th>
      <th>PNLMS</th>
      <th>PFDKF</th>
      <th>TFDKF</th>
      <th>RNN-AEC</th>
      <th>Meta-AF</th>
      <th>NKF (proposed)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_with_movement_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_with_movement_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_with_movement.wav"></audio></td>      
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/q2x99Trf80SQ4ZJo9I01_A_doubletalk_with_movement.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_with_movement_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_with_movement_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_with_movement.wav"></audio></td>  
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/QG4-PpzI-EmU-Qzb-7pSow_doubletalk_with_movement.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_with_movement_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_with_movement_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_with_movement.wav"></audio></td>  
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/qJuAkf-g00CNrazjR6-JIg_doubletalk_with_movement.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_with_movement_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_with_movement_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_with_movement.wav"></audio></td> 
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/QLaGxunnbUKP8t_ZHZAG4w_doubletalk_with_movement.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_with_movement_mic.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/test_wavs/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_with_movement_lpb.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PNLMS/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/PFDKF/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/TFDKF/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/RNN-AEC/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_with_movement.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/Meta-AF/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_with_movement.wav"></audio></td> 
      <td><audio controls="" preload="none" style="width: 100px;">
            <source src="demo/NKF/blind_test_set_clean_doubletalk/QtLE7-zrVkmlqiDjKli0kQ_doubletalk_with_movement.wav"></audio></td>
    </tr>
  </tbody>
</table>


