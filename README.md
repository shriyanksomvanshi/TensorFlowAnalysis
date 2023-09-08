# TensorFlowAnalysis
New repo for TensorFlow practice

Source: 1.	https://www.tensorflow.org/tfx/model_analysis/get_started  

### Overview
- TensorFlow Model Analysis (TFMA) is a tool for model evaluation.
- Target Audience: Machine Learning Engineers or Data Scientists.
- Functions both as a standalone library or as a component of a TFX (TensorFlow Extended) pipeline.
- Evaluates models on large data sets in a distributed manner using metrics defined during training. Metrics are compared over 
 different data slices and can be visualized in Jupyter or Colab notebooks.
- TFMA utilizes Apache Beam for distributed computations on large data, unlike some tools like TensorBoard that offer model 
introspection.

### Model Types Supported
- Designed for TensorFlow-based models, but can be extended for other frameworks.
- No longer requires an "EvalSavedModel" for usage.
- TFMA now focuses on the serving model, meaning it won't automatically evaluate training-time metrics unless using a Keras 
 model.
## Supported model types:
- TF2 (keras): Training Time Metrics (Y*), Post Training Metrics (Y)
- TF2 (generic): N/A, Post Training Metrics (Y)
- EvalSavedModel (estimator): Training Time Metrics (Y), Post Training Metrics (Y)
- None (pd.DataFrame, etc): N/A, Post Training Metrics (Y)

### Examples

## Single Model Evaluation:
- For distributed evaluations, use an Apache Beam pipeline with a distributed runner.
 Model Validation:
- To compare a candidate and baseline model, adjust the config and provide both models to tfma.run_model_analysis.
Visualization
- Results can be visualized in a Jupyter notebook using included TFMA frontend components.

# TensorFlow Model Analysis (TFMA) is a toolkit designed for assessing TensorFlow models. It offers the capability to evaluate models across vast data sets in a distributed fashion, employing the identical metrics set during training. Users can analyze these metrics across various data segments and display the results in Jupyter notebooks.

### Installation

The recommended way to install TFMA is using the [PyPI package](https://pypi.org/project/tensorflow-model-analysis/): 
