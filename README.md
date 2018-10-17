# ML Flask api
Using scikit learn to build a simple logistic regression model from the Iris data set and persist the model with pickle. [Pickle](https://docs.python.org/3/library/pickle.html) is a Python module that allows us to serialize a Python object structure. In this case, we will pickle the model we generated with scikit learn. We then use [Flask](http://flask.pocoo.org/) as our api backend to serve our pickled model. Once our backend is up and running, we can make calls against the api on the `/predict` route to generate responses from our model.

## Endpoint
### /predict
Our predict endpoint will return a JSON object with the class probabilities of our input variables.

Use the accompanying Jupyter notebook to make requests against the endpoint.

**Sample input:**

(Adjust input values to get your own unique response against the model)
```
input_data = {"sepalLength": 5.2, 
              "sepalWidth": 4.5, 
              "petalLength": 1.4, 
              "petalWidth": 4.2}
```


**Sample output:**
```
[{'name': 'Iris-Setosa', 'value': 93.48},
 {'name': 'Iris-Versicolour', 'value': 0.01},
 {'name': 'Iris-Virginica', 'value': 6.5}]
```
