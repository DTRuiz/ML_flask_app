# ML Flask api
Using scikit learn to build a simple logistic regression model for the Iris data set, we persist the model with pickle. We then use Flask as our api backend to serve our pickled model.

# Endpoint
### /predict
Our predict endpoint will return a JSON object with the class probabilities of our input variables.

You can use the accompanying Jupyter notebook to make requests against the endpoint.

Sample input:
```
input_data = {"sepalLength": 5.2, 
              "sepalWidth": 4.5, 
              "petalLength": 1.4, 
              "petalWidth": 4.2}
```


Sample output:
```
[{'name': 'Iris-Setosa', 'value': 93.48},
 {'name': 'Iris-Versicolour', 'value': 0.01},
 {'name': 'Iris-Virginica', 'value': 6.5}]
```