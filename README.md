# Create your first ML model
Create your first ML model

<text>Consider the following sets of numbers. Can you see the relationship between them?</text>

![image](https://user-images.githubusercontent.com/51197053/141204519-0a695037-06b9-4cf2-aa69-e31321b27980.png)


<text>As you look at them, you might notice that the value of X is increasing by 1 as you read left to right and the corresponding value of Y is increasing by 2. You probably think that Y equals 2X plus or minus something. Then, you'd probably look at the 0 on X and see that Y is -1, and you'd come up with the relationship Y=2X-1.</text>

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
#### Define and compile the neural network

<text>Next, create the simplest possible neural network. It has one layer, that layer has one neuron, and the input shape to it is only one value.</text>

```
model = tf.keras.Sequential([keras.layers.Dense(units=1, input_shape=[1])])
```
Next, write the code to compile your neural network. When you do so, you need to specify two functions—a `loss` and an `optimizer`.

In this example, you know that the relationship between the numbers is Y=2X-1.

When the computer is trying to learn that, it makes a guess, maybe Y=10X-10. The loss function measures the guessed answers against the known correct answers and measures how well or badly it did.

Next, the model uses the `optimizer` function to make another guess. Based on the loss function's result, it tries to minimize the loss. At this point, maybe it will come up with something like Y=5X+5. While that's still pretty bad, it's closer to the correct result (the loss is lower).
