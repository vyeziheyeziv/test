# TimbreTransfer

## 1. Thesis Model
Thesis model for music transfer and disentanglement of pitch and timbre

**Models**

There are three kinds of models here:
1. **Evaluated model**: The evaluated model in thesis with several unused layers.

  ( because the version of "model_state.pt" used in the evaluation includes several unused testing layers, I still added it here to make the inference in 1.2.2 can be run )
2. **Small-size model**: The small-size model has the same model architecture as the evaluated model, only the layers have been changed to a smaller size, and all unused layers are removed.
3. **Full-size model**: The same model architecture as evaluated model without unused model.

**Training**

* Requires A100 GPU in Colab

* Download dataset and upload the dataset to Google Drive:

  https://drive.google.com/file/d/1nH1o0ocUejHARVmqp2-yZRuou_C0odNN/view?usp=drive_link (39.31GB)

  https://drive.google.com/file/d/1Vi_1q07LhFcXtpV44w1koEv3kCrr0cQq/view?usp=drive_link (23.68GB)

* Manually set "dataset_path" and "model_save_path" in the second cell of 1.4.2.

  ( "dataset_path" is the path of the two zipped dataset, and model weights and TensorBoard records will all be saved in "model_save_path" )

* Training of full-size model: 1.1 -> 1.4.1 -> 1.4.2

**Inference**

* Inference of evaluated model: 1.1 -> 1.2.1 -> 1.2.2
* Inference of small-size model: 1.1 -> 1.3.1 -> 1.3.2
* Inference of full-size model(after training): 1.4.3

**External Dependencies**

This model originates from [ss-vq-vae](https://github.com/cifkao/ss-vq-vae/tree/main), below are the differences:

- Model architecture has been modified, Transformer encoder is added for content encoder, and the new model is based on beta-VAE.
- Loss function has been customized for the new training method and added another reconstruction loss.
- Some other customization details.
