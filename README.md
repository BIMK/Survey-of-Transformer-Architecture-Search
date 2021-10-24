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
<table>
<thead>
  <tr>
    <th>Category</th>
    <th>Task</th>
    <th>Method</th>
    <th>Search Space<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(3-level: Hyperparameter-level, Module-level, Architecture-level)</th>
    <th>Search Strategy&nbsp;&nbsp;&nbsp;&amp; Performance Estimation</th>
    <th>Publication</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="26">Natural Language<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Processing</td>
    <td rowspan="16">Improving Performace</td>
    <td> <a href="//www.baidu.com/"> Auto-Sizing  Transformer </a> </td>
    <td>H-level:&nbsp;&nbsp;&nbsp;Auto reducing the size of model in training</td>
    <td>Gradient optimization&nbsp;&nbsp;&nbsp;&amp; Train a supermodel </td>
    <td>arxiv 2019-10</td>
  </tr>
  <tr>
    <td>SandWich Transformer</td>
    <td>A-level: The permutation (order) of FFN and Self-Attention</td>
    <td>Random search &amp; Sample solutions, train and&nbsp;&nbsp;&nbsp;evaluate them</td>
    <td>arxiv 2020-4</td>
  </tr>
  <tr>
    <td>Multi-Pass Transformer</td>
    <td>A-level: information flow in&nbsp;&nbsp;&nbsp;Encoders<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(1. multi-pass encoder 2. information flow between these encoders)</td>
    <td>Random search &amp; Sample solutions, train and&nbsp;&nbsp;&nbsp;evaluate them</td>
    <td>arxiv 2020-9</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>Evolved Transformer</td>
    <td>M-level: cell search space</td>
    <td>EA &amp;&nbsp;&nbsp;&nbsp;Sample solutions, train them with early stopping&nbsp;&nbsp;&nbsp;for their evaluation</td>
    <td>arxiv 2017</td>
  </tr>
  <tr>
    <td>AutoTrans</td>
    <td>M-level: 1.cell search space&nbsp;&nbsp;&nbsp;2.activation 3.Norm<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.heads number 5.relative dimension</td>
    <td>RL&nbsp;&nbsp;&nbsp;&amp; Sample solutions in a&nbsp;&nbsp;&nbsp;supermodel <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(one-shot method)</td>
    <td>arxiv 2020-9</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>CAS(Language Models with Transformers)</td>
    <td>M-level: Modification:&nbsp;&nbsp;&nbsp;1.AddLinear<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.AddLSTM 3.FixSubset </td>
    <td> Coordinate architecture search &amp; Sample solution, fine-tune&nbsp;&nbsp;&nbsp;and evaluate them</td>
    <td>arxiv 2019-10</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>NAS-BERT</td>
    <td>M-level: 1.Embedding Size 2.heads&nbsp;&nbsp;&nbsp;number <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.Hidden Size 4. SepConv 3 5 7 <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5. Identity</td>
    <td>Direct&nbsp;&nbsp;&nbsp;sample (selection) &amp;&nbsp;&nbsp;&nbsp;Sample solutions in a supermodel <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(one-shot method) and performance approximation</td>
    <td>arixv 2021-5</td>
  </tr>
  <tr>
    <td>AdaBert</td>
    <td>　</td>
    <td>　</td>
    <td>arxiv 2021-1</td>
  </tr>
  <tr>
    <td>AutoBERT-Zero</td>
    <td>　</td>
    <td>　</td>
    <td>arxiv 2021-7</td>
  </tr>
  <tr>
    <td>Length-Adaptive Transformer</td>
    <td>　</td>
    <td>　</td>
    <td>arxiv 2021-6</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td rowspan="7">Hardware-aware <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Deployment</td>
    <td> Fast Transformers</td>
    <td>M-level:1.Dimension of Q K V 2.&nbsp;&nbsp;&nbsp;heads number<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. LN mean value 4. Width of depth of FFN </td>
    <td>Sampling&nbsp;&nbsp;&nbsp;distribution optimization &amp;&nbsp;&nbsp;&nbsp;Sample solutions in a supermodel <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(one-shot method)</td>
    <td>arxiv 2020-8</td>
  </tr>
  <tr>
    <td>HAT</td>
    <td>M-level: 1. Layer num in&nbsp;&nbsp;&nbsp;encoder/decoder<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Dimension of embedding, hidden layer in FFN and  heads number<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.Arbitrary encoder-decoder attention (Link) </td>
    <td>EA&nbsp;&nbsp;&nbsp;&amp; Sample solutions in a supermodel (one-shot method)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;and surrogate hareware predictor</td>
    <td>arxiv 2020-5</td>
  </tr>
  <tr>
    <td>RankNAS</td>
    <td>M-level: 1. Layer num in&nbsp;&nbsp;&nbsp;encoder/decoder<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Dimension of embedding, hidden layer in FFN and  heads number<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.Arbitrary encoder-decoder attention (Link) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;---------------------Extra to HAT ---------------<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. Norm type(Pre-LN, Post-LN)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.RPR Len [8,12,16] ( the maximum relative position Representations)</td>
    <td>Random&nbsp;&nbsp;&nbsp;search/EA &amp; Sample&nbsp;&nbsp;&nbsp;solutions in a supermodel (one-shot method)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; and rank and select them by the  ranking model</td>
    <td>arxiv 2021-9</td>
  </tr>
  <tr>
    <td>DARTsFormer</td>
    <td>M-level: •  Standard Conv w × 1: for w in 3, 5, 7,&nbsp;&nbsp;&nbsp;11.<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Dynamic Conv w × 1: for w in 3, 7, 11, 15.<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Self Attention; • FFN.<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Cross Attention: Only available to decoder.<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Gated Linear Unit (GLU).<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Zero: Return a zero tensor of the input size.<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Identity: Return the input.</td>
    <td>Gradient&nbsp;&nbsp;&nbsp;optimization (Multi-split reversible network for reducing memory)<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&amp; Train a&nbsp;&nbsp;&nbsp;supermodel </td>
    <td>arxiv 2021-5</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>Quantization</td>
    <td>Mixed Precision&nbsp;&nbsp;&nbsp;Quantization Transformer</td>
    <td>H-level:&nbsp;&nbsp;&nbsp;1-bit, 2-bit, 4-bit and 8-bit</td>
    <td>Gradient optimization&nbsp;&nbsp;&nbsp;&amp; Train a supermodel </td>
    <td> ICASSP 2021</td>
  </tr>
  <tr>
    <td rowspan="2">Other</td>
    <td>TextNAS</td>
    <td>Not Transformer: 1. Convolutional Layers<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.Recurrent Layers 3.Pooling Layers<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.Multi-Head Self-Attention Layers</td>
    <td>RL&nbsp;&nbsp;&nbsp;same as ENAS &amp; Sample&nbsp;&nbsp;&nbsp;solutions in a supermodel <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(one-shot method)</td>
    <td>AAAI 2020</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td rowspan="9">Computer <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Vision</td>
    <td>　</td>
    <td>AutoFormer</td>
    <td>　</td>
    <td>　</td>
    <td>arxiv 2021-7 (ICCV)</td>
  </tr>
  <tr>
    <td>　</td>
    <td>GLiT</td>
    <td>　</td>
    <td>　</td>
    <td>arxiv 2021-8</td>
  </tr>
  <tr>
    <td>Multi-stage</td>
    <td>Vit-ResNAS</td>
    <td>　</td>
    <td>　</td>
    <td>arxiv 2021-9</td>
  </tr>
  <tr>
    <td>　</td>
    <td>PSViT</td>
    <td>　</td>
    <td>　</td>
    <td>arxiv 2021-8</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>Vanilla NAS for CNN</td>
    <td>NAT (not search for&nbsp;&nbsp;&nbsp;Transformer)</td>
    <td>　</td>
    <td>　</td>
    <td>PAMI 2021 </td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td rowspan="3">Speech</td>
    <td rowspan="2">Speech&nbsp;&nbsp;&nbsp;Recognition</td>
    <td>Evolved&nbsp;&nbsp;&nbsp;Speech-Transformer</td>
    <td>M-level:&nbsp;&nbsp;&nbsp;cell space (same as Evolved Transformer) </td>
    <td>EA&nbsp;&nbsp;&nbsp;&amp; Sample solutions&nbsp;&nbsp;&nbsp;and  progressive dynamic hurdles (early&nbsp;&nbsp;&nbsp;stopping)</td>
    <td>INTERSPEECH 2020</td>
  </tr>
  <tr>
    <td>Streaming Transformer</td>
    <td>　</td>
    <td>　</td>
    <td>arxiv 2020-11</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td rowspan="3">Other</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
  <tr>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
    <td>　</td>
  </tr>
</tbody>
</table>
