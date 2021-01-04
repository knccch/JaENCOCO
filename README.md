# JaEnCOCO
This is the Japanese translation for the Ambiguous COCO dataset.

Our dataset is based on the original Ambiguous COCO dataset. We do not own the copyrights of images, English captions, and annotations in the dataset. Please visit the authors' web pages and follow their instructions to download them.

We are going to have an [Ambiguous MS COCO Japanese-English Multimodal Task](http://lotus.kuee.kyoto-u.ac.jp/WAT/ambiguous-mscoco/) at [WAT 2021](http://lotus.kuee.kyoto-u.ac.jp/WAT/WAT2021/index.html)!

## License
Our dataset is released under the [Creative Commons Attribution-ShareAlike (CC BY-SA) license](https://creativecommons.org/licenses/by-sa/4.0/legalcode).

## Dataset Description
There are two main folders that correspond to the validation data and the test data.
First, we will explain the files in each folder:
("*" indicates either "validation" or "test,"  depdending on  whether you are in the validation or test folder)

1. *Data.ja: This file contains the unsegmented Japanese sentences.
2. *Data.tok.ja: This file contains the Japanese sentences segmented by [Mecab](https://taku910.github.io/mecab/).
3. *FileNames.txt: This file contains the corresponding image file names.
4. *Index.txt: Thi file contains the corresponding sentence indices for the original Ambiguous COCO sentences.

In order to construct a full English-Japanese validation and testing dataset, you will need to combine this data with the English Ambiguous COCO sentences.
Now, we will explain how to combine this data with the English Ambiguous COCO sentences:

1. Download the Ambiguous COCO captions and images. Links to the dataset can be found at the [WMT 2017 Multimodal MT task page](http://www.statmt.org/wmt17/multimodal-task.html)
(Look under the "Datasets" section of this webpage)

2. By matching the provided sentence IDs for the validata and test data with the sentence IDs for the English captions, you can associate the Japanese sentences with thier corresponding English translations. From this you should be able to construct a validation file with 230 English sentennces and a test file with 231 English sentences.

3. The provided image file name list in each folder can be used to link each sentence to the corresponding image. (the file names are ordered in the samme order as the sentences. i.e., The first file name in the validation set corresponds to the first validatoin sentence, etc.)


## Reference
If you use this dataset, please cite the following [paper](https://arxiv.org/pdf/2010.08725.pdf):

Andrew Merritt, Chenhui Chu, Yuki Arase.
A Corpus for English-Japanese Multimodal Neural Machine Translation with Comparable Sentences.
arXiv:2010.08725.
```
@misc{merritt2020corpus,
      title={A Corpus for English-Japanese Multimodal Neural Machine Translation with Comparable Sentences}, 
      author={Andrew Merritt and Chenhui Chu and Yuki Arase},
      year={2020},
      eprint={2010.08725},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```

## Acknowledgment
This work was supported by Microsoft Research Asia Collaborative Research Grant and Grant-in-Aid for Young Scientists #19K20343, Japan.
