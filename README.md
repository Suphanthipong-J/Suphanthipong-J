## Suphanthipong-J

I work on state-of-health (SOH) estimation for lithium-ion batteries: deep learning that uses only the data a
battery management system records during an ordinary charge, and that can tell when its own estimate should not be
trusted.

### Featured work

**Charge-only battery SOH estimation with label-free reliability screening**

- Conv1D–BiLSTM network pretrained on the order of a cell's charges without labels, then fine-tuned on SOH
- Two label-free screens that withhold the estimate for cells the model is likely to get wrong
- Evaluated by leave-one-battery-out on 23 NASA and NCA-18650 cells, and without retraining on the Oxford and CALCE
  datasets (mean R² 0.905 and 0.735)
- Runs with ONNX Runtime on an NVIDIA Jetson Orin Nano (about 1.4 ms per estimate for the five-model ensemble)

The code will be made public after publication.

### Tools

Python · TensorFlow / Keras · scikit-learn · NumPy · pandas · SciPy · ONNX Runtime · NVIDIA Jetson
