## Suphanthipong-J

I work on state-of-health (SOH) estimation for lithium-ion batteries: deep learning that uses only the data a
battery management system records during an ordinary charge, and that can tell when its own estimate should not be
trusted.

### Featured work

**Charge-only SOH estimation of lithium-ion cells: failure analysis and label-free reliability screening**

- Conv1D–BiLSTM estimator that uses only constant-current charge data, evaluated by leave-one-battery-out on 23 NASA
  and NCA-18650 cells (median R² 0.87; 7 of 23 cells below R² 0.5)
- An analysis of the cells on which it fails: noisy SOH trajectories, features that track SOH weakly, and in one
  cell the voltage at which charges start
- A label-free score from a network pretrained on the order of a cell's charges that ranks failing cells below
  working ones (AUC 0.96–0.99 over three pretraining seeds); the cells it flags change with the seed, so it is
  preliminary evidence, not a validated detector
- Exploratory tests without retraining on the Oxford and CALCE datasets: the degradation trend is followed but its
  rate is under-estimated
- Runs with ONNX Runtime on an NVIDIA Jetson Orin Nano (about 1.4 ms per estimate for the five-model ensemble)

The code will be made public after publication.

### Tools

Python · TensorFlow / Keras · scikit-learn · NumPy · pandas · SciPy · ONNX Runtime · NVIDIA Jetson
