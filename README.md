# How can be improved the Saber 11 results in Colombia?

*Google data analytics capstone - Case study*

*Fabian Enrique Pedreros Camargo*

## Introduction

This case study aims to put into practice everything learned in the Google Data Analytics certification by applying a data analytics process to a real-world problem.

This case study is done to put into practice:

* Going through the Ask, Prepare, Process, Analyze, and Share phases of the data analysis process
* Stating a business task clearly
* Importing data from a real dataset
* Documenting any data cleaning that is perform on the dataset
* Analyzing the data 
* Creating data visualizations from the analysis
* Summarizing key findings from the analysis
* Documenting the conclusions and recommendations
* Creating and publishing the case study 

## Ask

In this phase we define what the project would look like and what would qualify as successful result. In this case we are going to solve these questions:

* What topic are you exploring?

We are going to work with the total results of a exam done in Colombia called ICFES between 2018 and 2021, and some demographic information about the students.

The Saber 11, popularly known as ICFES (not to be confused with the Instituto Colombiano para la Evaluación de la Educación), is a high school exit exam administered annually in grade 11 in the Colombian high school. The exam is standardized, similar to the SAT and ACT exams taken by high school students in the United States and the German Abitur or Selectividad in Spain. The purpose of the exam is to evaluate students' aptitude in five subjects: critical reading, mathematics, social studies, science and English.

The ICFES exam scores students using percentiles and an overall score ranging from 1 to 500 points, while the score for each subject ranges from 1 to 100 points. Scores are calculated based on the three-parameter logistic model [1].

* What is the problem you are trying to solve?

We are trying to solve a question hypothesized by the Ministry of Education, an entity that seeks to establish educational policies in order for students to perform better in the Saber 11 exam.

The main objective is to establish how ICFES results can be improved in Colombia.

To answer the main question it is necessary to divide it into more specific questions.

How are the results in the five subjects?
Are there any subjects in which students perform worse?
Are there differences in the overall results that can be explained by demographic variables?
What demographic groups should be prioritized in the improvement of education in order to obtain better overall ICFES scores?
What policies can be suggested in order to improve the global score?

* What metrics will you use to measure your data to achieve your objective?

I'm going to use the results by subject and the overall result per student.


* Who are the stakeholders?

The stakeholders are officials working in the Ministry of Education, who seek to understand the behavior of the Saber 11 results, in the period between 2018 and 2021, in order to establish educational policies to improve the performance of Colombian students in that exam.


* Who is your audience?

The audience are the same stakeholders.


* How can your insights help your client make decisions?

The reflections aim to understand the behavior of the results, helping to establish whether there are differences in scores by demographic variables and to establish which groups need prioritization in order to implement educational policies.

## Prepare

In the prepare phase we find the appropriate data to resolve the problem and stored properly

* Where is your data located?

The data is taken from Kaggle, this is published under the data set call ‘ICFES Colombia 2018 - 2021’ by Sorelys. The link to access the dataset is shared below ‘ICFES Colombia 2018 - 2021’

The data set is downloaded in a CSV file and save it locally in a set of folders to ensure data integrity. The archive name is ‘icfes_data.csv’

* How is the data organized?

The data is organized in a single CSV file. This have a tabular structure, with 84 columns and 1,650,063 rows. 

* Are there issues with bias or credibility in this data? Does your data ROCCC?

In this case I cannot be sure if the data is reliable, because I could not find the original dataset, the Kaggle dataset has no information to validate the origin of the data. But for the project it is well constructed. The data is current, we have the results of the last tests performed in Colombia, because of the Covid 19 pandemic these have not been performed with the normal periodicity.

* How are you addressing licensing, privacy, security, and accessibility?

This data is for open used and does not have any licensing.

* How did you verify the data’s integrity?

This data is cataloged as external data and its source is secondary, given that it is collected by a natural person from the ICFES institute through the Colombian government's open data services. 

* How does it help you answer your question?

These data have the results of the last 'Saber 11' tests conducted in Colombia, and demographic information that can be used to establish some behaviors related to some characteristics of the students, this can help me to make some differentiation between groups that perform better and those that do not.

With this data, a scorecard can be constructed, which stakeholders can use to view the behavior of test results over time and segregate by the different variables.

Because we have 84 different variables, it is necessary to shorten the variables to be used. I have selected the group of variables that I think are interesting and can be used to group the students' results.

* Are there any problems with the data?

Some values are in Spanish that Im going to translate them into English. There is missing data that needs to be handled in the best way.

### Metadata

![image](https://user-images.githubusercontent.com/32172901/183161766-28ffe9b0-1ab3-4849-8f14-2e6bf6f21934.png)
![image](https://user-images.githubusercontent.com/32172901/183162102-54348623-4dec-402b-9b70-944e6e705287.png)
![image](https://user-images.githubusercontent.com/32172901/183162189-872b7b82-ab66-4ba8-845c-f829d56430fd.png)
![image](https://user-images.githubusercontent.com/32172901/183162283-ae4544d5-ccdf-4d8e-8c22-b51166708a60.png)
![image](https://user-images.githubusercontent.com/32172901/183162395-76edcb65-bfcc-453c-8523-2ca636138cee.png)
![image](https://user-images.githubusercontent.com/32172901/183162488-41792144-2208-4911-bd5c-c02a86b97769.png)
![image](https://user-images.githubusercontent.com/32172901/183162580-dbb1e573-71c4-4b54-98a8-8c3518017fda.png)
![image](https://user-images.githubusercontent.com/32172901/183162697-ca19c4a2-f9d6-479c-b909-e77895a7bb40.png)

### Variables to be used

* ESTU_GENERO
* PERIODO
* ESTU_TIENEETNIA
* ESTU_DEPTO_RESIDE
* FAMI_ESTRATOVIVIENDA
* FAMI_EDUCACIONPADRE
* FAMI_EDUCACIONMADRE
* FAMI_TIENEINTERNET
* FAMI_TIENECOMPUTADOR
* FAMI_COMELECHEDERIVADOS
* FAMI_COMECARNEPESCADOHUEVO
* FAMI_COMECEREALFRUTOSLEGUMBRE
* ESTU_HORASSEMANATRABAJA
* COLE_GENERO
* COLE_NATURALEZA
* COLE_CALENDARIO
* COLE_BILINGUE
* COLE_CARACTER
* COLE_AREA_UBICACION
* COLE_JORNADA
* COLE_DEPTO_UBICACION
* PUNT_LECTURA_CRITICA
* PUNT_MATEMATICAS
* PUNT_C_NATURALES
* PUNT_SOCIALES_CIUDADANAS
* PUNT_INGLES
* PUNT_GLOBAL
* ESTU_ETNIA
* ESTU_LIMITA_MOTRIZ

## Process

In the process phase we check, transform and clean the data. 

● What tools are you choosing and why?

My tool of choice for data cleansing and transformation is Python, we learned R in certification but I feel more confident with this language and using Jupyter Notebooks.

● Have you ensured your data’s integrity?

Yes, all the data cleansing process is documented in the Jupyter Notebook called “ICFES Analysis Google Certification Capstone Project.ipynb”

● What steps have you taken to ensure that your data is clean?

* Clean the data
  * Find NA and set what to do with it
  * Validate by variable the data type
  * Validate by variable the data structure
  * Validate by variable the range
  * Validate by variable the categorical values
  * Validate duplicate records
* Validate the data is in the required format and structure
  * Which values should be modified, such as associating numeric values, splitting or concatenating text strings
* Validate that the data are sufficient and meet the requirements outlined for the solution of the problem.
* Ensure that the data are representative and unbiased.
* Store at the site to be

* How can you verify that your data is clean and ready to analyze?

I validated the data while cleaning it, and used some tools to see if the data meets the requirements.

* Have you documented your cleaning process so you can review and share those results?

Yes, the process is documented, can be share and replicated.










