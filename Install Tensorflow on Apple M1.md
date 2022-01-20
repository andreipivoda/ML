# **Install TF on Apple M1**

### Make and activate Conda environment.
```
conda create --prefix ./env
conda activate ./env
```

### Install TensorFlow dependencies from Apple Conda channel.
```conda install -c apple tensorflow-deps```

### Install base TensorFlow (Apple's fork of TensorFlow is called tensorflow-macos).
```python -m pip install tensorflow-macos```

### Install Apple's tensorflow-metal to leverage Apple Metal (Apple's GPU framework) for M1, M1 Pro, M1 Max GPU acceleration.
```python -m pip install tensorflow-metal```


### Install common data science packages.
```conda install jupyter pandas numpy matplotlib scikit-learn```

### Start Jupyter Notebook.
```jupyter notebook```

Import dependencies and check TensorFlow version/GPU access.
```
import numpy as np
import pandas as pd
import sklearn
import tensorflow as tf
import matplotlib.pyplot as plt
```

### Check for TensorFlow GPU access
```print(f"TensorFlow has access to the following devices:\n{tf.config.list_physical_devices()}")```

### See TensorFlow version
```print(f"TensorFlow version: {tf.__version__}")```
