# Survey-of-Transformer-Architecture-Search (TAS)

## Introduction
This is a summary of Neural Architecture Search (NAS) on Transformer, named TAS.

Papers are divided into the following categories based on Domain Specific:

1.**Natrual Language Processing (NLP)**
2.**Computer Vision (CV)**
3.**Automatic Speech Recognition (ASR)**
4.**Other**

Each TAS work is introduced from three aspects: Search Space, Search Strategy, and Estimation Strategy, which are key compoments of NAS and also important for TAS.


More details of each work has been summarized in our [survey paper](), coming soon.

## Summary of TAS
<table class="tg">
<thead>
  <tr>
    <th class="tg-uzvj">Category</th>
    <th class="tg-wa1i">Task</th>
    <th class="tg-wa1i">Method</th>
    <th class="tg-amwm">Search Space<br>(3-level: Hyperparameter-level, Module-level, Architecture-level)</th>
    <th class="tg-wa1i">Search Strategy &amp; Performance Estimation</th>
    <th class="tg-wa1i">Publication</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-nrix" rowspan="29">Natural Language<br>Processing</td>
    <td class="tg-nrix" rowspan="19">Improving Performace</td>
    <td class="tg-wa1i"><a href="https://aclanthology.org/D19-5625/">Auto-Sizing  Transformer</a></td>
    <td class="tg-amwm">H-level: Auto reducing the size of model in training</td>
    <td class="tg-baqh">Gradient optimization &amp; Train a supermodel </td>
    <td class="tg-lhti">arxiv 2019-10</td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://aclanthology.org/2020.acl-main.270/">SandWich Transformer</a></td>
    <td class="tg-amwm">A-level: The permutation (order) of FFN and Self-Attention</td>
    <td class="tg-baqh">Random search &amp; Sample solutions, train and evaluate them</td>
    <td class="tg-lhti">arxiv 2020-4</td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2009.11382">Multi-Pass Transformer</a></td>
    <td class="tg-amwm">A-level: information flow in Encoders<br>(1. multi-pass encoder 2. information flow between these encoders)</td>
    <td class="tg-baqh">Random search &amp; Sample solutions, train and evaluate them</td>
    <td class="tg-lhti">arxiv 2020-9</td>
  </tr>
  <tr>
    <td class="tg-wa1i"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="http://proceedings.mlr.press/v97/so19a.html">Evolved Transformer</a></td>
    <td class="tg-amwm">M-level: cell search space</td>
    <td class="tg-baqh">EA &amp; Sample solutions, train them with early stopping for their evaluation</td>
    <td class="tg-lhti">ICML 2019</td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://link.springer.com/chapter/10.1007/978-3-030-88480-2_14">AutoTrans</a></td>
    <td class="tg-amwm">M-level: 1.cell search space 2.activation 3.Norm<br>4.heads number 5.relative dimension</td>
    <td class="tg-baqh">RL &amp; Sample solutions in a supermodel <br>(one-shot method)</td>
    <td class="tg-lhti">arxiv 2020-9</td>
  </tr>
  <tr>
    <td class="tg-wa1i"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/1904.09408">CAS</a></td>
    <td class="tg-amwm">M-level: Modification: 1.AddLinear<br>2.AddLSTM 3.FixSubset </td>
    <td class="tg-baqh"> Coordinate architecture search &amp; Sample solution, fine-tune and evaluate them</td>
    <td class="tg-lhti">arxiv 2019-10</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2105.14444">NAS-BERT</a></td>
    <td class="tg-amwm">M-level: 1.Embedding Size 2.heads number <br>3.Hidden Size 4. SepConv 3 5 7 <br>5. Identity</td>
    <td class="tg-baqh">Direct sample (selection) &amp; Sample solutions in a supermodel <br>(one-shot method) and performance approximation</td>
    <td class="tg-lhti">KDD 2021</td>
  </tr>
  <tr>
    <td class="tg-wa1i"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2001.04246">AdaBert</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">arxiv 2021-1</td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2107.07445">AutoBERT-Zero</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">arxiv 2021-7</td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2010.07003">Length-Adaptive Transformer</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">arxiv 2021-6</td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://aclanthology.org/2021.acl-long.400/">AutoTinyBERT</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">ACL 2021</td>
  </tr>
  <tr>
    <td class="tg-wa1i"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-wa1i"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2109.08668">Primer</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">NeurIPS 2021</td>
  </tr>
  <tr>
    <td class="tg-nrix" rowspan="7">Hardware-aware <br>Deployment</td>
    <td class="tg-amwm"> <a href="https://arxiv.org/abs/2008.06808">Fast Transformers</a></td>
    <td class="tg-amwm">M-level:1.Dimension of Q K V 2. heads number<br>3. LN mean value 4. Width of depth of FFN </td>
    <td class="tg-baqh">Sampling distribution optimization &amp; Sample solutions in a supermodel <br>(one-shot method)</td>
    <td class="tg-lhti">arxiv 2020-8</td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://aclanthology.org/2020.acl-main.686/">HAT</a></td>
    <td class="tg-amwm">M-level: 1. Layer num in encoder/decoder<br>2. Dimension of embedding, hidden layer in FFN and  heads number<br>3.Arbitrary encoder-decoder attention (Link) </td>
    <td class="tg-nrix">EA &amp; Sample solutions in a supermodel (one-shot method)<br>and surrogate hareware predictor</td>
    <td class="tg-lhti">ACL 2020</td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2109.07383">RankNAS</a></td>
    <td class="tg-amwm">M-level: 1. Layer num in encoder/decoder<br>2. Dimension of embedding, hidden layer in FFN and  heads number<br>3.Arbitrary encoder-decoder attention (Link) <br>---------------------Extra to HAT ---------------<br>4. Norm type(Pre-LN, Post-LN)<br>5.RPR Len [8,12,16] ( the maximum relative position Representations)</td>
    <td class="tg-baqh">Random search/EA &amp; Sample solutions in a supermodel (one-shot method)<br> and rank and select them by the  ranking model</td>
    <td class="tg-lhti">arxiv 2021-9</td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2105.14669">DARTsFormer</a></td>
    <td class="tg-amwm">M-level: •  Standard Conv w × 1: for w in 3, 5, 7, 11.<br>• Dynamic Conv w × 1: for w in 3, 7, 11, 15.<br>• Self Attention; • FFN.<br>• Cross Attention: Only available to decoder.<br>• Gated Linear Unit (GLU).<br>• Zero: Return a zero tensor of the input size.<br>• Identity: Return the input.</td>
    <td class="tg-baqh">Gradient optimization (Multi-split reversible network for reducing memory)<br>&amp; Train a supermodel </td>
    <td class="tg-lhti">arxiv 2021-5</td>
  </tr>
  <tr>
    <td class="tg-wa1i"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-wa1i"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-nrix">Quantization</td>
    <td class="tg-wa1i"><a href="https://ieeexplore.ieee.org/abstract/document/9414076">Mixed Precision Quantization Transformer</a></td>
    <td class="tg-amwm">H-level: 1-bit, 2-bit, 4-bit and 8-bit</td>
    <td class="tg-baqh">Gradient optimization &amp; Train a supermodel </td>
    <td class="tg-5frq"> ICASSP 2021</td>
  </tr>
  <tr>
    <td class="tg-nrix" rowspan="2">Other</td>
    <td class="tg-wa1i"><a href="https://ojs.aaai.org/index.php/AAAI/article/view/6462">TextNAS</a></td>
    <td class="tg-hmil">Not Transformer: 1. Convolutional Layers<br>2.Recurrent Layers 3.Pooling Layers<br>4.Multi-Head Self-Attention Layers</td>
    <td class="tg-baqh">RL same as ENAS &amp; Sample solutions in a supermodel <br>(one-shot method)</td>
    <td class="tg-lhti">AAAI 2020</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-nrix" rowspan="9">Computer <br>Vision</td>
    <td class="tg-nrix"></td>
    <td class="tg-wa1i"><a href="https://openaccess.thecvf.com/content/ICCV2021/html/Chen_AutoFormer_Searching_Transformers_for_Visual_Recognition_ICCV_2021_paper.html">AutoFormer</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">ICCV 2021</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-wa1i"><a href="https://openaccess.thecvf.com/content/ICCV2021/html/Chen_GLiT_Neural_Architecture_Search_for_Global_and_Local_Image_Transformer_ICCV_2021_paper.html">GLiT</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">ICCV 2021</td>
  </tr>
  <tr>
    <td class="tg-nrix">Multi-stage</td>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2109.00642">Vit-ResNAS</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">ICCV 2021</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2108.03428">PSViT</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">arxiv 2021-8</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"><a href="https://arxiv.org/abs/2106.13700">ViTAS</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">arxiv 2021-6</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"><a href="https://openaccess.thecvf.com/content/CVPR2021/html/Ding_HR-NAS_Searching_Efficient_High-Resolution_Neural_Architectures_With_Lightweight_Transformers_CVPR_2021_paper.html">HR-NAS</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">CVPR 2021</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-nrix">Vanilla NAS for CNN</td>
    <td class="tg-wa1i"><a href="https://ieeexplore.ieee.org/abstract/document/9447923">NAT (not search for Transformer)</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">PAMI 2021 </td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2103.12424">BossNAS</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
  <tr>
    <td class="tg-nrix" rowspan="6">Speech</td>
    <td class="tg-nrix" rowspan="2">Speech Recognition</td>
    <td class="tg-wa1i"><a href="http://www.interspeech2020.org/uploadfile/pdf/Tue-1-8-5.pdf">Evolved Speech-Transformer</a></td>
    <td class="tg-amwm">M-level: cell space (same as Evolved Transformer) </td>
    <td class="tg-baqh">EA &amp; Sample solutions and  progressive dynamic hurdles (early stopping)</td>
    <td class="tg-lhti">INTERSPEECH 2020</td>
  </tr>
  <tr>
    <td class="tg-wa1i"><a href="https://ieeexplore.ieee.org/abstract/document/9383517">Streaming Transformer</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">SLT 2020</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"><a href="https://arxiv.org/abs/2104.05390">Improved Conformer via NAS</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">arxiv 2021-4</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-wa1i"><a href="https://arxiv.org/abs/2104.02868">DARTS-Conformer</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">arxiv 2021-8</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"><a href="https://ieeexplore.ieee.org/abstract/document/9414403">LightSpeech</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">ICASSP 2021</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
  </tr>
  <tr>
    <td class="tg-nrix" rowspan="3">Other</td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"><a href="https://arxiv.org/abs/2108.12821">Analyzing and Mitigating Interference</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">arxiv 2021-8</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"><a href="https://arxiv.org/abs/2110.04035">UNINET</a></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti">arxiv 2021-10</td>
  </tr>
  <tr>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-nrix"></td>
    <td class="tg-lhti"></td>
  </tr>
</tbody>
</table>
