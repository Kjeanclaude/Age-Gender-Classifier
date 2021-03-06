# Age-Gender-Classifier
An Age and Gender Classifier with a Fully-Connected artificial Neural Network

I used this personal project as my **capstone project** for the Udacity's [Machine Learning Engineer Nanodegree Program](https://www.udacity.com/course/machine-learning-engineer-nanodegree--nd009). It is the equivalent of a Master of Engineering thesis. 
You could find the observations of my reviewer [HERE](https://github.com/Kjeanclaude/Age-Gender-Classifier/blob/master/Observations_of_my_reviewer.pdf).

- ***Full implementation code in python available here, open to research and further improvements.***


## Prerequisite

### Packages
For this work you will also need to install these Frameworks:
- Python 2 or 3
- [TFlearn](http://tflearn.org/installation/)

``
pip install tflearn
``

-	[Tensorflow](https://www.tensorflow.org/install/)

### Files and datasets
**I.** First, you should download the [Adience Dataset](http://www.openu.ac.il/home/hassner/Adience/data.html) (**faces.tar.gz (1.2Gb)** or **aligned.tar.gz (2.6Gb)** compressed files). 

You should also clone the [AgeGenderDeepLearning](https://github.com/GilLevi/AgeGenderDeepLearning) repository. Only the ***Folds*** repository will be necessary for the process; it contains the ***.txt files***, labels of the Adience Benchmark in separated age and gender files {***age_test.txt, age_train.txt, age_train_subset.txt, age_val.txt, gender_test.txt, gender_train.txt, gender_train_subset.txt, gender_val.txt***}.

Both files should be extracted and made available at the same location, otherwise ***make sure that the files paths are accessible from the Ipython Notebook files***. And also update the ***folds_path*** variable with the correct *Fold path name* and the ***images_root_directory*** variable with the correct Adience */face* or */aligned* repositories paths. This will ensure the creation of the ***Unified Dataset***.

Pay attention on the directory separators when writing the files' paths for Python 2 or Python 3. See the example below :

```python
if int(PyVersion[0])==2:
    folds_path='Age-Gender-Classifier/Folds/train_val_txt_files_per_fold' 
    print("Jean-Claude, I got in python 2")
else:
    folds_path='Age-Gender-Classifier\\Folds\\train_val_txt_files_per_fold'
    print("Jean-Claude, I got in python 3")
```

**II.** You could also instead clone this repository where the ***Folds*** directory is already available with Ipython Notebook files.

```
git clone https://github.com/Kjeanclaude/Age-Gender-Classifier.git
cd Age-Gender-Classifier/
# And also Extract the /face and/or /aligned datasets here.
```

And then simply execute the IPython Notebooks in your preferred environment (Anaconda, Virtual environment, etc.).

```ipython
cd Age-Gender-Classifier/
jupyter notebook AgeGenderPrediction-OneHotModel-Py2-3.ipynb
# and/or
jupyter notebook AgeGenderPrediction-TuplesModel-Py2-3.ipynb
```

**III.** Now you can work with the ***age_gender_unified_dataset.pickle*** file already separated in ***age_gender_dataset (features)*** <br/>and ***age_gender_labels (2-hot labels)*** . 
<br/>It contains unique images which have both gender and age information in the Adience Dataset.
<br/>You can download the ***age_gender_unified_dataset.pickle*** file [HERE](https://drive.google.com/open?id=0B5GQQIZDsDCcaXl1dGVpZmtSSHM)(2.39Go), in the same location as the pickle notebook files (***AgeGenderPrediction-OneHotModel-Py23-PickleFile.ipynb*** or ***AgeGenderPrediction-TuplesModel-Py23-PickleFile.ipynb***).
<br/>Or create your own pickle file from the previous notebooks (***AgeGenderPrediction-OneHotModel-Py2-3.ipynb***), using the code provided in ***I.4- Training and Test sets creation***.
<br/>==> And then simply execute the IPython pickle Notebooks in your preferred environment (Anaconda, Virtual environment, etc.).
```ipython
cd Age-Gender-Classifier/
jupyter notebook AgeGenderPrediction-OneHotModel-Py23-PickleFile.ipynb
# and/or
jupyter notebook AgeGenderPrediction-TuplesModel-Py23-PickleFile.ipynb
```
<br/>Because of the ***checksum*** the images should not have the same order if you choose to built your own pickle file from the code I provided above. To verify that you have the original ***age_gender_unified_dataset.pickle*** file I built, you should have the following images for the first image of the unified dataset, and for the second image of the training set.
<br/>![alt tag](https://github.com/Kjeanclaude/Age-Gender-Classifier/blob/master/Sample_From_The_Unified_Dataset_Pickle.png)


<br/>The Methods **I**, **II** and **III** have to be done alternatively (not cumulable), please choose your preferred method.

---
<br/>

For more details, you should also find the proposal and the report PDF files on this repository.

---
### Roadmap

| Tasks | Date | Update |
| --- | --- | --- |
| Report | 30/06/2017 | 05/07/2017 |
| Write an example of prediction label interpretation function | 05/07/2017 | ... |
| Write an example of age prediction ranges function | 24/07/2017 | ... |
| Increase the Unified Dataset and make it available in a compressed file, with usage script | 01/09/2017 | 03/09/2017 |
| Provide a mobile app demo of the age and gender classifier | ... | ... |

---
## Citations

Please, cite me in your publications if it helps your research.
<br/>I appreciate, but do not require, attribution.
<br/>The following is a [BibTeX](http://www.bibtex.org/) and plaintext reference for my
[Age-Gender-Classifier](https://github.com/Kjeanclaude/Age-Gender-Classifier/blob/master/report.pdf).

```
@techreport{Kjeanclaude2017agegenderclassifier,
  title={Age-Gender-Classifier: An Age and Gender Classifier 
  with a Fully-Connected artificial Neural Network},
  author={Kouassi Konan Jean-Claude},
  year={2017},
  institution={Udacity, Machine Learning Engineer Nanodegree},
}

K. K. Jean-Claude,
"Age-Gender-Classifier: An Age and Gender Classifier with a Fully-Connected artificial Neural Network,"
Udacity, Machine Learning Engineer Nanodegree, Tech. Rep., July 2017.
```
---
---
```
==> "Intellectuals solve problems, geniuses prevent them."
==> "The difference between stupidity and genius is that genius has its limits." 
```
[Albert-Einstein](http://www.movemequotes.com/top-21-albert-einstein-quotes/) :angel:
