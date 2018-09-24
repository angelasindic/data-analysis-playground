
Methods covered so far
----------------------
* Permutation Importance
* Partial Dependence Plots (PDP)
* SHapley Additive exPlanations (SHAP)

 
### Permutation Importance

Can be used to determine which features matter most.

- Discovers feature importance by randomly shuffle one column (feature) of the validation data.
- Measures the accuracy of the permuted data set
Therefore, the loss function is used to compare true target values with the prediction of the shuffled data set.
A significant accuracy degeneration would indicate a high predictive power and therefore the high importance of the feature. 

### Partial Dependence Plots (PDP)

PDPs can be used to visualize how certain features influence model prediction. PDPs can capture dependencies or associations of features in complex models, like coefficients in linear/logistic regression models.

PDP uses the trained model but then the value of one feature is repeatedly modified to build a series of predictions.  
We can apply this process to one are more training examples, the simplest case is to start with one training example, that is one row in the data set.

The examples of the notebook use [PDP plot](https://pdpbox.readthedocs.io/en/latest/), which is implemented based on:
* [Friedman, J. (2001). Greedy Function Approximation: A Gradient Boosting Machine. The Annals of Statistics, 29(5):1189–1232.](https://statweb.stanford.edu/~jhf/ftp/trebst.pdf)
* [Goldstein, A., Kapelner, A., Bleich, J., and Pitkin, E., Peeking Inside the Black Box: Visualizing Statistical Learning With Plots of Individual Conditional Expectation. (2015) Journal of Computational and Graphical Statistics, 24(1): 44-65](https://arxiv.org/abs/1309.6392)


### SHapley Additive exPlanations (SHAP)

SAHP is a [unified framework](http://papers.nips.cc/paper/7062-a-unified-approach-to-interpreting-model-predictions) 
that interprets predictions to overcome the problem that complex models cannot be used to explain model behavior.
To create more transparency of a model's output, SHAP assigns each feature an importance value for a particular prediction.

A quite nice explanation of the theory behind SHAP can be found in this [blog post]
(https://towardsdatascience.com/one-feature-attribution-method-to-supposedly-rule-them-all-shapley-values-f3e04534983d).

Example Notebooks 
-----------------



Installation and Usage
----------------------
### Installation of python packages
`pip install -r requirements.txt`

Also additional installation of graphviz is necessary:
* Mac using homebrew
`brew install graphviz`
* Ubuntu
`sudo apt-get install graphviz`


### Download data
* Download the data files from .... into the `data` directory.  
    * You can find the data [here]().

