# Neural Networking #
We will start with what a NN is meant to do.
NNs are something that helps humans identify trends in large data sets that we otherwise wouldn’t be able to see.
They can perform complex actions and decisions that save humans a lot of time. We technically could do it, but a NN can do it in a fraction of the time.
The NN makes these decisions based on its understanding from the data sets it was trained on.

NN’s accomplish these tasks by converting the data set into numeric input.
Sometimes these conversions are very complicated but other times they are simply a 1 or a 0 for something being present or not present. 
Each individual neuron has its own mathematical formula that contributes to the system.
W1*X1 + W2*X2 + … Wn*Xn + Bias
Each neuron is further related to fellow neurons by a degree of strength (weight), with some neurons being very related and others being mildly related.
All neurons must have some degree of relation however. 

Neurons are organized in a layered system, with every node being connected
Networks can have 2 or many layers, but every neuron within a layer must be connected to all the neurons in the layer before and after it. 

Each neuron carries data through the layers that contributes to a NN output.
Sometimes certain neurons may not be fired by a specific input, and this is okay. If a set of neurons was meant to determine the presence of stripes, they would likely stay at a value of 0 if the current subject was a mono colored object.
The presence of this zero is relevant to the output of the system. Here zero isn’t a null response, it is an indication that something is not present within this particular sample. 

The accuracy of a NN improves as the system evolves. 
This is done through training a NN on a data set, but sometimes a hands on correction is required. 
In a training approach, the testing machine knows the key and the NN is expected to guess the correct answer. 

A NN only works in its respective field.
If a NN is designed to differentiate between photos of dogs and hamburgers, it would not be able to adequately process a cat.
Likewise, if a dog was dressed up as a hamburger the NN would likely draw a blank or respond inconsistently to the data. 

In closing, NNs convert our world into numerical data that they can understand at lightning speeds. While this allows them to understand complex interactions at speeds that humans cannot, they are also cripplingly specialized into a particular purpose. 

# Data Cleansing #
DC is the process of looking at a large data set and improving its quality. 
This is often done by separating data that is incorrect or incomplete from relevant, accurate samples.
Sometimes this means altering the data to make it more consistent with the rest of the data set, but most often dirty data is simply discarded from the data set. 

Why do we cleanse the data?
Because NNs are trained using data sets, it is important that they are as accurate as possible. If these data sets have flaws within them, the network will too. 
Sometimes if the data is too corrupt the NN will never be able to adequately guess unknown data because its training set was ill equipped to teach it.
In a world where perfection is the goal, we cannot afford having a misinformed NN running the show.

There are 2 major ways to treat abnormalities: Absolute and Fuzzy
Absolute is a strategy of instantly discarding data that does not fit a set of criteria. An example of this would be to discard any cars made after 2017 in a data set based on safety rating on new cars. 
Fuzzy is a strategy that doesn’t draw such a hard line. It assigns a given datum a value between 0 and 1 in regard to its fittingness into the data set. The science here is deciding where to place the cut off point.
If your system was slightly fuzzy then your cutoff may be .75, but if your system was very fuzzy it may be cut off at .45 or .50.

In conclusion, DC is the process of analyzing data sets for anomalies and incompletions to refine our training data for a NN. These data sets are what the NN learns from, so it is imperative that our teaching materials be as relevant as possible. Finally, we can accomplish this goal by sorting out data strictly or fuzzily depending on the situation. 








# Heuristics #
The Smart Can software makes its decisions using a heuristic process. This means that it does not always comply with what is strictly logical, but operates under a set of soft rules to try and get the most optimal outcome through trial and error. 
This likely means that there will be a lot of disagreement between the operator and the software in the beginning, but that this would improve overtime. 
We need to ask the developers of this application if this is an appropriate determination of what would actually happen. (If they even know yet)

Furthermore, heuristic models are focused on a shorter term goal rather than the biggest picture. This concession had to be made in this program because no program could realistically be expected to make the most optimal decisions regarding every single aircraft within a short period of time.

Based on my understanding, we don’t have anything else left in that software to define. This one was pretty loose, but it was a term I hadn’t heard before so I figured it would be worthwhile to include it in the final document. 
