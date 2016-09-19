# timeseries_gan
A tensorflow implementation of GAN ( exactly InfoGAN or Info GAN ) to one dimensional ( 1D ) time series data.
We've applied InfoGAN model ([https://arxiv.org/abs/1606.03657](https://arxiv.org/abs/1606.03657) ) 
to one dimensional time series data for classifying time series data through unsupervised way.  

## Dependencies

1. tensorflow >= rc0.10 
1. [sugartensor](https://github.com/buriburisuri/sugartensor) >= 0.0.1

## Dependencies

1. tensorflow >= rc0.10 
1. [sugartensor](https://github.com/buriburisuri/sugartensor) >= 0.0.1

## Sample Data

Unfortunately, I cannot share sample time series data but you can use any csv formatted time series data as following.

<pre><code>
time,series1,series2
1,11.1,21.1
2,12.2,22.2
3,13.0,23.1
     .
     .
     .
</code></pre>

This file should be saved at 'asset/data/sample.csv' before you train the network. 

## Training the network

Execute
<pre><code>
python train.py
</code></pre>
to train the network. You can see the result ckpt files and log files in the 'asset/train' directory.
Launch tensorboard --logdir asset/train/log to monitor training process.

## Generating sample time series data
 
Execute
<pre><code>
python generate.py
</code></pre>
to generate sample time series data.  The graph image of generated time series data will be saved in the 'asset/train' directory.

## Generated time series data sample

This graph of time series was generated by InfoGAN network. 
You may know that it's difficult to discriminate generated time series data from real time series data.
 
<p align="center">
  <p>Real time series data</p>
  <img src="https://raw.githubusercontent.com/buriburisuri/timeseries_gan/master/png/real.png" width="350"/>
</p>
<p align="center">
  <p>Fake time series data</p>
  <img src="https://raw.githubusercontent.com/buriburisuri/timeseries_gan/master/png/fake.png" width="350"/>
</p>  
<p align="center">
  <p>Decomposed time series data</p>
  <img src="https://raw.githubusercontent.com/buriburisuri/timeseries_gan/master/png/decompose.png" width="350"/>
</p>  
  

## Other resources

1. [Original GAN tensorflow implementation](https://github.com/buriburisuri/sugartensor/blob/master/sugartensor/example/mnist_gan.py)
1. [InfoGAN tensorflow implementation](https://github.com/buriburisuri/sugartensor/blob/master/sugartensor/example/mnist_info_gan.py)
1. [EBGAN tensorflow implementation](https://github.com/buriburisuri/ebgan)


# Authors
Namju Kim (njkim@jamonglab.com) at Jamonglabs Co., Ltd.
