# normalizing-flows-tutorial
Based on the code from: 

See the blog posts (<a href="http://blog.evjang.com/2018/01/nf1.html">Part 1</a>, <a href="http://blog.evjang.com/2018/01/nf2.html">Part 2</a>) for more information.


### Nov 18
For continuous flows: 
1. Markov (Additive Noise, complex noise patterns), Hidden Markov noise are not difficult to learn flow for 
   (Sequence lengths are currently small: 3,4, no. of iterations required ~50000 even in these simple cases for planar flows. 
    For more complex flows such as NVP, the number of iterations are 4-5x lower)
   
Issues: 
1. Tensorflow 2.0 does not have native support for the tf.Bijectors, so currently using 1.5.1 version. 
2. Bijector API seems quite convenient for continuous flows, need to extend it for discrete flows. 

What can be the different discrete flow models? 
- Do we need quantized at each stage, or can we have bijection in continuous domain all along, and quantize at the end? 

   
  
   

