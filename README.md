Kaggle competition link:
https://www.kaggle.com/c/hpa-single-cell-image-classification

A goal of this code was to implement a full pipeline from getting data to train a model while using pytorch multiprocessing for improved speed. Using queue and multiprocessing from pytorch packages is useful for memory sharing. Normally it would copy objects when getting them from queue, but pytorch is sharing the memory between processes. - All this using Jupyter Notebook.

For future keep in mind:
* When training one should run through whole train and whole val, currently it does not. So results are not consistent.
* Currently multiprocessing is CPU bound, lowering image resolution might help a lot.
* Hyperparameters for model are default, might not be optimal.