# Support Vector Machine (SVM) Classification with Iris Dataset

## Libraries Used
- **numpy**: Used for numerical operations.
- **matplotlib.pyplot**: Used for plotting graphs (decision boundary).
- **sklearn.datasets**: Provides access to sample datasets (we use `load_iris()`).
- **sklearn.model_selection.train_test_split**: Splits data into training and testing sets.
- **sklearn.svm.SVC**: The Support Vector Classifier (SVC) for classification.
- **sklearn.metrics.accuracy_score**: Evaluates model performance.

## Dataset Overview
- **`datasets.load_iris()`**: Loads the Iris dataset, which contains 150 samples of iris flowers with 4 features each.
- **`X = iris.data[:, :2]`**: We use only the first two features (sepal length and sepal width) for easy 2D visualization.
- **`y = iris.target`**: The target labels:
  - 0 → Setosa
  - 1 → Versicolor
  - 2 → Virginica

## Data Splitting
- **`train_test_split()`** splits the dataset into:
  - 80% for training (`X_train`, `y_train`)
  - 20% for testing (`X_test`, `y_test`)
- **`random_state=42`** ensures reproducibility (same split every time).

## Model Initialization and Training
- **`SVC(kernel='linear')`**: Initializes an SVM classifier with a linear kernel (best for linearly separable data).
- **`svm_model.fit(X_train, y_train)`**: Trains the model using the training data.

  - ### Other Kernel Options
    - `'linear'`: Straight-line separation.
    - `'rbf'`: Non-linear, curved separation using radial basis function.
    - `'poly'`: Uses polynomial curves for separation.

## Making Predictions
- **`predict(X_test)`**: The trained model makes predictions on the test dataset.
- **`accuracy_score(y_test, y_pred)`**: Compares predicted labels (`y_pred`) with actual labels (`y_test`).
- Prints accuracy score (e.g., 83% = 0.83).

## Visualization
- Creates a mesh grid covering the feature space for plotting decision boundaries.
- The step size (`h = 0.02`) determines grid resolution.

### Plotting
- **`plt.contourf()`**: Draws the decision boundary.
- **`plt.scatter()`**: Plots the actual data points.
- **`plt.show()`**: Displays the graph.

### Graph Output
- The decision boundary is drawn.
- Different species are colored in different regions.
- Data points (flowers) are marked in the scatter plot.
