Contents:

- Integrating the frontend part of the online evaluator for fetching answers into the real time database in firebase with the help of flask. 
- Implementing the algorithm that is used to evaluate answers based on 3 parameters
  - Keywords
  - Grammar
  - Question Specific Things (QST)




1) Create a new firebase project in this case named new:

![](screenshots/Aspose.Words.c95b4e34-7cda-48ee-90b8-9035cc662319.001.png)











1) ![](screenshots/Aspose.Words.c95b4e34-7cda-48ee-90b8-9035cc662319.002.png)Import the given json file into the firebase realtime database of the project:


1) After importing the json:








![](screenshots/Aspose.Words.c95b4e34-7cda-48ee-90b8-9035cc662319.003.png)

1) ![](screenshots/Aspose.Words.c95b4e34-7cda-48ee-90b8-9035cc662319.004.png)Make a config.py file which would contain details of the project and help in linking the flask code with the database:

1) Code file responsible for fetching data from the webpage to the database:![](screenshots/Aspose.Words.c95b4e34-7cda-48ee-90b8-9035cc662319.005.png)

1) ![](screenshots/Aspose.Words.c95b4e34-7cda-48ee-90b8-9035cc662319.006.png)Output upon executing the python file using flask thus giving us a host address for the web page:




1) Opening the link just generated and giving the answers followed by the email id and then submit:

![](screenshots/Aspose.Words.c95b4e34-7cda-48ee-90b8-9035cc662319.003.png)

1) Successful fetching of the data into the firebase database:

![](screenshots/Aspose.Words.c95b4e34-7cda-48ee-90b8-9035cc662319.007.png)



1) Run the givVal.py file inside the Modules folder to get output of the evaluated answer:

![](screenshots/Aspose.Words.c95b4e34-7cda-48ee-90b8-9035cc662319.008.png)

