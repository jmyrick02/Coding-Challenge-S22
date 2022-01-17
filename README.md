# ACM Research Coding Challenge (Spring 2022)

## Sources
- https://github.com/hwd404/FOLD-R-PP (FOLD-R++ algorithm GitHub repo)
- https://arxiv.org/abs/2110.07843 (Research paper describing the FOLD-R++ algorithm by UTD's Dr. Gopal Gupta)

## Overview and Method
My classification has an accuracy of 100% on a test data set comprised of 20% of the original data set, with the other 80% devoted to training. I generated an explainable answer set programming (ASP) rule set using the FOLD-R++ algorithm. The benefit of this method is that it creates a human-comprehensible rule set to determine if a mushroom is poisonous or not, avoiding the black-box model of traditional machine learning classification.

One can see my code and output in the `coding-challenge.ipynb` file, which is a Jupyter Notebook. The code consists of setting up the model and importing and processing the data and the use of the model. The generated answer set programming rule set achieved 100% accuracy on the test data using only 4 default rules and 3 exception rules. Finally, in the last output, one can see the explanation for the classification of each mushroom in the test data set.

A concrete example:
```
Explanation for example number 37:
answer 1:
[T]class(X,'p') :- not [F]gill-size(X,'b'), [T]stalk-surface-below-ring(X,'y').
```
This states that test mushroom number 37 is poisonous because its gill size is not broad and its stalk surface below its ring is scaly. The model learned these rules only from the training data and the FOLD-R++ algorithm.
