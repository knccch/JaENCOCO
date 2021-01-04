# JaEnCOCO
This is the Japanese translation for the Ambiguous COCO dataset.

## How to Construct Each Dataset
In order to construct a full English-Japanese validation and testing dataset, you will need to combine this data with the English Ambiguous COCO sentences.

There are two main folders that correspond to the validation data and the test data.
First, we will explain the files in each folder:
("*" indicates either "validation" or "test,"  depdending on  whether you are in the validation or test folder)

1. *Data.ja: This file contains the unsegmented Japanese sentences.
2. *Data.tok.ja: This file contains the Japanese sentences segmented by [Mecab](https://taku910.github.io/mecab/).
3. *FileNames.txt: This file contains the corresponding image file names.
4. *Index.txt: Thi file contains the corresponding sentence indices for the original Ambiguous COCO sentences.

Now, we will explain how to combine this data with the English Ambiguous COCO sentences:

1. Download the Ambiguous COCO captions and images. Links to the dataset can be found at [the WMT 2017 Multimodal MT task page](http://www.statmt.org/wmt17/multimodal-task.html)
(Look under the "Datasets" section of this webpage)

2. By matching the provided sentence IDs for the validata and test data with the sentence IDs for the English captionns, you can associate the Japanese sentences with thier corresponding English translations. From this you should be able to construct a validation file with 230 English sentennces and a test file with 231 English sentences.

3. The provided image file name list in each folder can be used to link each sentence to the corresponding image. (the file names are ordered in the samme order as the sentences. i.e., The first file name in the validation set corresponds to the first validatoin sentence, etc.)


## Citation
If you use this dataset, please cite the following paper:
```
Andrew Merritt, Chenhui Chu, Yuki Arase.
A Corpus for English-Japanese Multimodal Neural Machine Translation with Comparable Sentences.
arXiv:2010.08725.
```
