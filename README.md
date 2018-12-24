
|Layer (type)                   | Output Shape       | Param #   | Connected to
|----------------|
|in_0 (InputLayer)              | (None, 50, 50, 1)  | 0         |
|in_1 (InputLayer)              | (None, 50, 50, 1)  | 0         |
|model_1 (Model)                | (None, 400)        | 19100157  | in_0[0][0]
|                               |                    |           | in_1[0][0]
|inps_joined (Concatenate)      | (None, 800)        | 0         | model_1[1][0]
|                               |                    |           | model_1[2][0]
|dense_1 (Dense)                | (None, 128)        | 102528    | inps_joined[0][0]
|dense_2 (Dense)                | (None, 128)        | 102528    | inps_joined[0][0]
|FC-BN-In-0 (BatchNormalization)| (None, 128)        | 512       | dense_1[0][0]
|FC-BN-In-1 (BatchNormalization)| (None, 128)        | 512       | dense_2[0][0]
|activation_13 (Activation)     | (None, 128)        | 0         | FC-BN-In-0[0][0]
|activation_14 (Activation)     | (None, 128)        | 0         | FC-BN-In-1[0][0]
|fl_0 (Dense)                   | (None, 1)          | 129       | activation_13[0][0]
|fl_1 (Dense)                   | (None, 1)          | 129       | activation_14[0][0]
==================================================================================================
Total params: 19,306,495
Trainable params: 19,294,265
Non-trainable params: 12,230
