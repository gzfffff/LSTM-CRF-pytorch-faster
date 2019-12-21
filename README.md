# LSTM-CRF-pytorch-faster fd
This is an accelerated LSTM-CRF implementation based on the Pytorch official tutorial   (URL:https://pytorch.org/tutorials/beginner/nlp/advanced_tutorial.html). I have modified the dynamic planning part, including Viterbi decoding and partition function calculation. In the experiment, it has achieved a speed increase of more than 50 times compared to the original version.

The original version can only input one sample at a time when it is trained. In the most recent update, I modified the model to support parallel computing for batch, so that the training time was greatly improved again.

It is important to note that in the parallel version, the input tensor is shaped as [batchSize,timeStep,embedding], while in the original version, the input tensor is shaped as [timeStep,batchSize,embedding]
