# Create your first ML model
Create your first ML model

<text>Consider the following sets of numbers. Can you see the relationship between them?</text>

![image](https://user-images.githubusercontent.com/51197053/141091315-ce62101b-b707-4021-9568-bed669df3561.png)


<text>As you look at them, you might notice that the value of X is increasing by 1 as you read left to right and the corresponding value of Y is increasing by 3. You probably think that Y equals 3X plus or minus something. Then, you'd probably look at the 0 on X and see that Y is 1, and you'd come up with the relationship Y=3X+1.</text>

<text>That's almost exactly how you would use code to train a model to spot the patterns in the data!</text>

<text>Now, look at the code to do it.</text>

<text>How would you train a neural network to do the equivalent task? Using data! By feeding it with a set of X's and a set of Y's, it should be able to figure out the relationship between them.</text>

<text>Start with your imports. Here, you're importing TensorFlow and calling it tf for ease of use.</text>

<text>Next, import a library called numpy, which represents your data as lists easily and quickly.</text>

<text>The framework for defining a neural network as a set of sequential layers is called keras, so import that, too.</text>


```
import tensorflow as tf
import numpy as np
from tensorflow import keras
```

