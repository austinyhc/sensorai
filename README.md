# Welcome to sensorai
> Make deep learning is more accessibe to apply for sensors on low-cost edge devices


## 1% Better Everyday

- estimate an optimal learning rate for your model given your data using a Leanring Rate Finder
- utilize learning rate schedules such as the [triangular policy](https://arxiv.org/abs/1506.01186), the [1cycle policy](https://arxiv.org/abs/1803.09820), and [SGDR](https://arxiv.org/abs/1608.03983) to effectively minimize loss and improve generalization
- load and preprocess waveform-baesd data from a variety of formats
- inspect data points that were misclassified and [provide explanations](https://eli5.readthedocs.io/en/latest/) to help improve your model
- leverage a simple prediction API for saving and deploying both models and data-preprocessing steps to make predictions on new raw data

## Installing

`pip install sensorai`

Last but not least, it is highly recommended by `nbdev` to run `nbdev_install_git_hooks` after first clone a repo. This sets up git hooks, which clean up the notebooks to removce the extraneous metadata stored in the notebooks which causes unnecessary merge conflicts.

Also, before submitting a PR, chech that the local library and notebooks match. The script `nbdev_diff_nbs` can let you know if there is a difference between the local library and the notebooks.
- If you made a change to the notebooks in one of the exported cells, you can export it to the library with `nbdev_build_lib` or `make fastai`
- If you made a change to the library, you can export it back to the notebooks with `nbdev_update_lib`.

## Tests

To run the tests in parallel, launch:

`nbdev_test_nbs` or `make test`

For all the tests to pass, you'll need to install the following optional dependencies:
```bash
pip install "sentencepiece<0.1.90" wandb tensorboard albumentations pydicom opencv-python scikit-image pyarrow kornia \
    catalyst captum neptune-cli
```

Tests are written using `nbdev`, for example see the documentation for `test_eq`.

## Docker Container
> Do I need to create my own docker images?
