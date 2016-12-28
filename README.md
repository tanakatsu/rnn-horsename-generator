# rnn-horsename-generator

This is forked from [yusuketomoto/chainer-char-rnn](https://github.com/yusuketomoto/chainer-char-rnn).


## Requirement
- [Chainer](https://github.com/pfnet/chainer)

```
$ pip install chainer
```

## Train
Start training the model using `train.py`, for example

```
$ python train.py
```

The `--data_dir` flag specifies the dataset to use. By default it is set to `data/umaname` which consists of a subset of names of Japanese racehorses.

**Your own data**: If you'd like to use your own data create a single file `input.txt` and place it into a folder in `data/`. For example, `data/some_folder/input.txt`.



## Sampling
Given a checkpoint file (such as those written to cv) we can generate new text. For example:
```
$ python sample.py \
--vocabulary data/unaname/vocab.bin \
--model cv/some_checkpoint.chainermodel \
--primetext some_text
```
## References
- Original implementation: [https://github.com/karpathy/char-rnn]()
- yusuketomoto's implementation: [https://github.com/yusuketomoto/chainer-char-rnn]()

