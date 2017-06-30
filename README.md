# Age-Gender-Classifier
An Age and Gender Classifier with a Fully-Connected artificial Neural Network


## Prerequisite

### Files and dataset
First, you should download the [Adience Dataset](http://www.openu.ac.il/home/hassner/Adience/data.html) (faces.tar.gz or aligned.tar.gz compressed files). 

You should also clone the [AgeGenderDeepLearning](https://github.com/GilLevi/AgeGenderDeepLearning) repository. Only the ***Folds*** repository will be necessary for the process; it contains the ***.txt files***, labels of the Adience Benchmark in separated age and gender files {***age_test.txt, age_train.txt, age_train_subset.txt, age_val.txt, gender_test.txt, gender_train.txt, gender_train_subset.txt, gender_val.txt***}.

Both files should be extracted and made available at the same location, otherwise make sure that the files paths are accessible from the Ipython Notebook file. And also update the ***folds_path*** variable with the correct *Fold path name* and the ***images_root_directory*** variable with the correct Adience */face* or */aligned* repositories path. This will ensure the creation of the ***Unified Dataset***.

You could also instead clone this repository where the ***Folds*** directory is already available with Ipython Notebook files.

``
git clone https://github.com/Kjeanclaude/Age-Gender-Classifier.git
cd Age-Gender-Classifier/
``

### Packages
For this work you will need to install these Frameworks:
- Python 2 or 3
- [TFlearn](http://tflearn.org/installation/)
-	[Tensorflow](https://www.tensorflow.org/install/)
