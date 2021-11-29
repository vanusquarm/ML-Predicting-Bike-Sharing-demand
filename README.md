# Predict Bike Sharing Demand with AutoGluon
This project is built with Sagemaker Studio
Requirements
- Notebook should be using a ml.t3.medium instance (2 vCPU + 4 GiB)
- Notebook should be using kernal: Python 3 (MXNet 1.8 Python 3.7 CPU Optimized)
Install packages
  !pip install -U pip
  !pip install -U setuptools wheel
  !pip install -U "mxnet<2.0.0" bokeh==2.0.1
  !pip install autogluon --no-cache-dir
  # Without --no-cache-dir, smaller aws instances may have trouble installing
