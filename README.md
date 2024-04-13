# AAMNet

## Requirements

- `torch==1.7.1`
- `torchvision==0.8.2`
- `opencv-python==4.4.0.42`

## Datasets
We use IU X-Ray datasets in our paper.

For `IU X-Ray`, you can download the dataset from [here](https://drive.google.com/file/d/1c0BXEuDy8Cmm2jfN0YYGkQxFZd2ZIoLg/view?usp=sharing) and then put the files in `data/iu_xray`.

NOTE: The `IU X-Ray` dataset is of small size, and thus the variance of the results is large.

## Train

Run `bash train_iu_xray.sh` to train a model on the IU X-Ray data.

or Run the following code in a terminal

```cmd
python main_train.py
```



## Test

Run `bash test_iu_xray.sh` to test a model on the IU X-Ray data.

or Run the following code in a terminal

```cmd
python main_test.py
```

Follow [CheXpert](https://github.com/MIT-LCP/mimic-cxr/tree/master/txt/chexpert) or [CheXbert](https://github.com/stanfordmlgroup/CheXbert) to extract the labels and then run `python compute_ce.py`. Note that there are several steps that might accumulate the errors for the computation, e.g., the labelling error and the label conversion. We refer the readers to those new metrics, e.g., [RadGraph](https://github.com/jbdel/rrg_emnlp) and [RadCliQ](https://github.com/rajpurkarlab/CXR-Report-Metric).
