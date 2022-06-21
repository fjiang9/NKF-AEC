# <center>Low-Complexity Acoustic Echo Cancellation with Neural Kalman Filtering</center>

<center>Dong Yang<sup>*</sup>, Fei Jiang<sup>*</sup>, Wei Wu, Xuefei Fang, and Muyong Cao</center>
<center>Tencent Technology</center>

## Abstract

<div style="text-align: justify"> The Kalman filter has been adopted in acoustic echo cancellation due to its robustness to double-talk, fast convergence, and tracking ability. The performance of Kalman filter is closely related to the accuracy of the state noise covariance and the observation noise covariance, which are either manually designed or estimated according to the echo cancellation results. The estimation error may lead to unacceptable results, especially when the echo path suffers abrupt changes, the tracking performance of the Kalman filter could be degraded significantly. In this paper, we propose the neural kalman filtering (NKF), which uses neural networks to implicitly model the covariance of the state noise and observation noise and to output the Kalman gain in real-time. Experimental results on both synthetic test sets and real-recorded test sets show that, the proposed NKF has superior convergence and re-convergence performance while ensuring low near-end speech degradation comparing with the state-of-the-art Kalman filters. Moreover, the proposed model size is merely 9.4 K and the RTF is as small as 0.1284, which indicates that the NKF can be deployed in low-resource platforms. </div> 

<!-- <br>
<center><img src="images/diagram.png" width="600"></center>
<br> -->

## Audio Samples

<!-- <div style="text-align: justify"> This mixture audio clip is from 'Zeno - Signs' in MUSDB18 test partition: </div> 
<p style="margin-bottom : 6px;">
</p>
<center><audio controls="" preload="none">
  <source src="demo/mixture-1.wav">
</audio></center>
<div style="text-align: justify"> Separated sources: </div> 
<p style="margin-bottom : 6px;">
</p>
<table align="center">
  <thead>
    <tr>
      <th> </th>
      <th>Vocal</th>
      <th>Bass</th>
      <th>Drums</th>
      <th>Other</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Ground Truth</th>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/GT/vocals_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/GT/bass_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/GT/drums_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/GT/other_cut.wav"></audio></td>
    </tr>
    <tr>
      <th>Open-Unmix</th>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/openunmix/1_vocals_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/openunmix/1_bass_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/openunmix/1_drums_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/openunmix/1_other_22k_cut.wav"></audio></td>
    </tr>
    <tr>
      <th>Demucs(v2)</th>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/demucs/vocals_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/demucs/bass_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/demucs/drums_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/demucs/other_22k_cut.wav"></audio></td>
    </tr>
    <tr>
      <th>Wave-U-Net</th>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/waveunet/mixture-1_vocals_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/waveunet/mixture-1_bass_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/waveunet/mixture-1_drums_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/waveunet/mixture-1_other_22k_cut.wav"></audio></td>
    </tr>
    <tr>
      <th>Tasnet</th>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/tasnet/vocals_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/tasnet/bass_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/tasnet/drums_22k_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/tasnet/other_22k_cut.wav"></audio></td>
    </tr>
    <tr>
      <th>InstGlow (Ours)</th>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/instGlow/vocals_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/instGlow/bass_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/instGlow/drums_cut.wav"></audio></td>
      <td><audio controls="" preload="none" style="width: 130px;">
            <source src="demo/instGlow/other_cut.wav"></audio></td>
    </tr>
  </tbody>
</table>
<br> -->
