# Online-Evaluator

## LOGIC and CONCEPT:

The idea is basically to evalaute the subjective/descriptive answers from the model answer that is provided by the teacher.
Basically for the first attempt we have ceated a Python Flask App where student can give there answer.
Currently It has 3 general OOPS related questions. After submiting the data, it goes to Firebase.
And when the "givVal.py" script is executed it will evaluate and store in Firebase Database the answers of each question based on ML algorithm that we have implemented.

- At the core NB classifier is working. With 21 records available in it.

(This dataset is manually written by us and is based on random assumptions.)


### Here is that Dataset: https://github.com/pragya2002/Teaching-Made-Easy-HCI/blob/main/online%20evaluator/Modules/finaldataset.csv


## For doing this evaluation 3 Parameters have been used:
#### 1) Keywords
#### 2) Grammar
#### 3) Question Specific Things (QST)

##
- The dataset have 4 attributes viz. "keywords", "grammar", "qst"(Qusetion Specific Things) and "class".
"class" is the attribute that the ML Algorithm will predict after providing values of remaining 3 attributes.

- So,
the values of "keywords" and "qst" attributes defined as :(1-excellent,2-verygood,3-good,4-ok,5-poor,6-verypoor)

- The values of "grammar" attribute are defined as: (0-improper,1-proper) and finally

- The value of "class" ranges from 1 to 9. 
##

### 1. Keywords
Evaluation of Keywords based Cosine Similarity of "student's/user's answer" with "model answer".

Firstly texts (i.e. student's and model answer) converted into vectors. And from these two vectors the Cosine similarity is Calculated.

Now this gives value from 0 to 1. this is converted into numeric form (i.e. 0 to 100). And then keywords will get the value from 1-6


### 2. Grammar
For this, the number of grammatical mistakes are taken into consideration.

For this an API provided by https://textgears.com is used.

### 3. Question Specific Things (QST)
Fuzzy Logic is used to give the value of qst.

(FuzzyWuzzy library from https://github.com/seatgeek/fuzzywuzzy is used).

<br>

## Usage:
- First of all clone this repository using following command:

```git clone https://github.com/pragya2002/Teaching-Made-Easy-HCI.git```

or download https://github.com/pragya2002/Teaching-Made-Easy-HCI this repository. 

Then You can find the "requirements.txt" file at the root level of this project which contains all the requirements of this project. For installing these requirements, open the terminal and run the following command

```
cd path/to/Teaching-Made-Easy-HCI/online\ evaluator
pip install -r requirements.txt
```
<br>

- Now, as mentioned previously this project uses Firebase, so for the Firebase configurations:
  ##### 1. Create a firebase project at https://console.firebase.google.com
 
  ##### 2. Create "configurations.py" file at the root level and add the following:
  ```
  config = {
    "apiKey": "add your api key",
    "authDomain": "add your domain",
    "databaseURL": "add your Database url",
    "projectId": "add your project id",
    "storageBucket": "add your storage bucket",
    "messagingSenderId": "add your message Id"
  }
  ```
  ##### 3. Then go to your Firebase Database console click start in realtime database (select test mode if pop-up comes i.e. database rules must be true for read     and write both) and import the json file "temp.json" inside temp folder. (In temp.json just for an example three model answer and there answers given by 9           users/students are included. So you can evaluate/test them.)
  Now, next step is to run the programs
  
  ##### 4. So, To give the answers you can run Data_set_collector.py file inside the DataSetCollectorFlaskApp directory and can give your answers. It is a simple     flask app which lets users answer the subjective questions.

  (Also for evaluating your own questions, change the model answer in Firebase Database and the question in flask app and store them in the database as per requirements     and tests)

  ##### 5. The main algorithm is in "givVal.py" file inside the Modules directory. <br> Run that file and you will have the answers evaluated by the algorithm inside the Database and it will also print them in the terminal.


<br>

#### For any issues, drop an email - pragya.yss10@gmail.com
