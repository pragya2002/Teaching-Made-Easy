Contents:

- Integrating the frontend part of the online evaluator for fetching answers into the real time database in firebase with the help of flask. 
- Implementing the algorithm that is used to evaluate answers based on 3 parameters
  - `  `Keywords
  - `  `Grammar
  - `  `Question Specific Things (QST)




1) Create a new firebase project in this case named new:

![](Aspose.Words.5e9cca53-c690-4737-a0e3-bf81a779d048.001.png)











1) Import the given json file into the firebase realtime database of the project:

![](Aspose.Words.5e9cca53-c690-4737-a0e3-bf81a779d048.002.png)

















1) After importing the json:

![](Aspose.Words.5e9cca53-c690-4737-a0e3-bf81a779d048.001.png)







1) Make a config.py file which would contain details of the project and help in linking the flask code with the database:

![](Aspose.Words.5e9cca53-c690-4737-a0e3-bf81a779d048.001.png)

1) Code file responsible for fetching data from the webpage to the database:

![](Aspose.Words.5e9cca53-c690-4737-a0e3-bf81a779d048.003.png)


1) Output upon executing the python file using flaskthus giving us a host address for the web page:

![](Aspose.Words.5e9cca53-c690-4737-a0e3-bf81a779d048.004.png)


1) Opening the link just generated and giving the answers followed by the email id and then submit:

![](Aspose.Words.5e9cca53-c690-4737-a0e3-bf81a779d048.001.png)

1) Successful fetching of the data into the firebase database:

![](Aspose.Words.5e9cca53-c690-4737-a0e3-bf81a779d048.005.png)






1) Run the givVal.py file inside the Modules folder to get output of the evaluated answer:

![](Aspose.Words.5e9cca53-c690-4737-a0e3-bf81a779d048.006.png)

