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


## Analize

In the process phase the data is analyzed trying to answer the mean questions. 

In this [link](https://github.com/FabianPedreros/GoogleCapstoneProyect/blob/main/ICFES%20Analysis%20Google%20Certification%20Capstone%20Project.ipynb) is the Jupyter Notebooks file with all the process and analysis phases, in such i conduct the data cleansing, data tranformation, univariate analysis and multivariate analysis.

● How should you organize your data to perform analysis on it?

I organized it in dataframes, it already came in tabular format.

● Has your data been properly formatted?

Yes, the formats were reviewed in the data cleaning phase and no need to modify the formats or structure was found.

● What surprises did you discover in the data?

I expected to see a higher correlation between qualitative variables with test scores, but these are low to medium, the maximum correlations found are 0.4.

● What trends or relationships did you find in the data?

 - The subjects in which students obtained the worst average results during 2018, 2019 and 2020 were Social Sciences, English and Natural Sciences with their corresponding average scores of 48.25, 49.67 and 49.48.
 - The student's total score can be explained by the maximum educational level attained by the father, and it is observed that the higher the educational level, the better the results. Students whose father has no education have an average score of 215.76, while those who finished high school have an average score of 253.0 and those who are the children of professionals with postgraduate degrees have an average score of 320.44.

- The student's total score can be explained by the maximum educational level attained by the mother, the higher the educational level, the better the results. Students whose mother has no education have an average score of 212.30, while those who finished high school have an average score of 250.0 and those who are children of professionals with graduate degrees have an average score of 315.7.
- It appears that there is a higher correlation between student scores with the educational level of the mother than with the educational level of the father. However, the data are not as strong.
- There are differences in the average overall scores obtained by the students depending on the journey in which they study, so we can divide them into three groups: 

  - The first group that we can observe is the one formed by the Saturday and night shifts, these two shifts have the worst average performance with means lower than 212 points.
  - The other group that has very similar behaviors is the afternoon, morning and single shifts, which in that order have the worst to the best performance, with mean scores of 247.9, 250.6 and 253.0 points respectively.
  - And the third group is that of full-day students, which is differentiated by having the best mean score of 282.0, despite having the highest standard deviation.

 - On average, a student without internet has an overall score of 231.91 points, while one who has internet access has an average of 362.7 points.
 - Students with computers at home have a better average result in the 'Saber 11' tests than their peers who do not have them, students with computers have an average score of 265.17 points and those without computers have an average score of 233.38 points.
 - When analyzing the differences in the overall scores by level of consumption of milk and milk products, we can see that students who consume these types of products on a daily basis have better results than those who do not or are not as constant in their consumption. Students who never or rarely consume them obtained average scores of 227.75 points, much lower than the 268.67 of those who do consume them on a daily basis.
 - The level of consumption of meat, fish or eggs shows a differentiated behavior, evidencing that students who consume these products on a daily basis obtain better average (and median) results than those who do not consume them or those who do not do so in such a constant manner. The higher the consumption of these products, the better results are obtained in the 'Saber 11' test.
- As we have seen with the consumption of other foods, students who have a daily consumption of cereals and legumes also obtain better average results, in this case the difference seems to be smaller, but it exists and should therefore be taken into account when considering policies to support students.
- The fact that a student works has negative effects on the score obtained in the 'Saber 11' exam, those who do not have to work have average scores of 206 points but the group that works up to 30 hours a week, have an average score that ranges between 236.97 and 238.50 points, but even more critical, those students who work more than 30 hours a week have average scores of 228.28, that is about 32 points less than those who do not work.
- We can see a difference in the results obtained between students who are from urban vs. rural schools, urban students have a better average performance, obtaining mean scores of 255.98 while rural students on average obtain 232.26. This means that there are differences in the population means of about 23 points in the overall score.
- There are marked differences in the scores obtained by the students according to their ethnicity, the tendency is that students with an ethnicity have lower scores than those who do not (None), especially the minority groups that present the lowest results, according to the average global score, are:

  - Sikuani, global score mean: 194.485095
  - Emberá, global score mean: 202.595009
  - Wayúu, global score mean: 204.531898
  - Cubeo, global score mean: 206.666667
  - Palenquero, global score mean: 210.626087

- As the social stratum increases, so does the global score obtained, for example, we can see how the average score of students in stratum one is 238.66, while those in stratum 6 obtain 291.47 points. The three subgroups with the worst performance from the lowest to the highest are:

  - Without stratum, with a mean score of 210.94
  - Stratum 1, with a mean score of 238.66
  - Stratum 2, with a mean score of 252.68

- Looking at the results obtained by the department in which the school is located, we can see how the average performance of each of these was, in order to identify geographically the territories in which policies should be implemented in order to improve education and therefore the results obtained in the 'Saber 11' test.The ten territories with the worst overall average results are listed below:

   - CHOCO: 208.793992
   - VAUPES: 211.288528
   - AMAZONAS: 219.208477
   - LA GUAJIRA: 225.301777
   - MAGDALENA: 226.712194
   - GUAINIA: 228.320217
   - VICHADA: 228.509985
   - GUAVIARE: 231.048853
   - BOLIVAR: 233.353061
   - CAUCA: 236.288295

 In this group, departments such as Choco, Vaupés and Amazonas stand out for their low performance.These are far from the global average results of 252.25 points and from those obtained by the top ten departments:

   - BOGOTÁ: 271.634496
   - SANTANDER: 267.065893
   - BOYACA: 263.909203
   - CUNDINAMARCA: 260.901961
   - NORTE SANTANDER: 259.054171
   - QUINDIO: 255.756395
   - RISARALDA: 255.550558
   - VALLE: 254.971947
   - HUILA: 253.18529
   - META: 251.997952


● How will these insights help answer your business questions?

**The way to improve the results obtained by students in the Saber 11 test, is through the application of policies that seek to address the population subgroups that have lower performance, as well as the attention to factors that affect student performance, guided by the points listed below:**

1. It is necessary to prioritize educational policies that help students in subjects such as Social Sciences, English and Natural Sciences, due to the fact that these have the lowest average scores in the Saber 11 test in the last three years (2018, 2019 and 2020).
2. Special attention should be paid to students whose parents have not completed high school, since this group obtains worse average results than students whose parents have at least completed high school.
3. It can be said that the students who need more support are those of the irregular shifts (Sabatine and night), but that a change in student policy is advisable to adopt the full day at the national level, since they are the students who have the best results in average in the 'Saber 11' tests.
4. We can indicate that students without internet access have worse average results than those who have internet at home, so education policies should encourage the use of internet for educational purposes and expand national coverage, that in this moment is estimated to be the 64 percent of the students.
5. Policies that help students to have access to computers in schools or public policies that facilitate the purchase of these appliances by families should be created, access to computers by students at home is estimated at 60%
6. Policies should focus on students who do not consume milk, milk products, meat, fish, eggs, cereals and legumes on a daily basis, as well as on the inclusion of these foods in school diets and on facilitating access to these types of foods in the basic basket of families, since there are differences in average global scores with peers who do.
7. The fact that a student works has negative effects on the score obtained in the 'Saber 11' exam, so efforts should be focused on students who work, even more so if they work more than 30 hours a day.
8. Students living in rural environments should receive support from educational institutions in order to improve learning and obtain better results in the 'Saber 11' test, this group of students have a lower global score that the urban students. 
9. All minority groups, with the exception of the gypsy communities and natives of Pasto, have much lower scores than those without ethnicity (253.65 average points), so it is recommended to generate educational policies that focus on these groups, remembering that they represent about 6 percent of the total number of students.
10. Students located in the next departments should be the focus of policies to improve their education, this have the lowest mean global scores: Choco, Vaupes, Amazonas, La Guajira, Magdalena, Guainia, Vichada, Guaviare, Bolivar and Cauca. In this group, departments such as Choco, Vaupés and Amazonas stand out for their low performance.
11. It is advisable to generate educational support policies for students who do not report stratum and those who belong to stratum 1 and 2, these three groups are the ones that historically have the lowest performances.

## Share

This step aims to effectively communicate the insights.

In this [link](https://github.com/FabianPedreros/GoogleCapstoneProyect/blob/main/082022%20Final%20Presentation%20Google%20Case%20Study.pptx) is the final presentation created to communicate the insights and recommendations.

* Were you able to answer the business question?

Yes, we were able to answer the main question of how to improve the results obtained in the ICFES or Saber 11 test, we specified the behavior of the results in each of the subjects, identifying which of them have the worst results, as well as identifying the subgroups according to the demographic variables that have lower performance, in order to establish which groups should be addressed and generally suggest policies that seek to address these subgroups. 

* What story does your data tell?

The data tell the story of the results obtained by students in the Saber 11 tests, of the social and economic differences that affect their general knowledge in the areas of mathematics, language, social sciences and natural sciences at the end of high school. 

* How do your findings relate to your original question?

They establish subgroups that need to be addressed for their low performance on the tests and suggest some policies to mitigate the conditions are related to these performances. 


* Who is your audience? What is the best way to communicate with them?

My fictitious audience is the politicians and public workers in charge of generating public policies at the national level regarding the education of Colombians. The best way to communicate the findings would be through a final report of the work and a presentation compiling the most relevant points and the proposals made.

* Can data visualization help you share your findings?

Yes, the visualization of the findings may be relevant, to show the differences in the mean scores obtained depending on each of the demographic variables.

* Is your presentation accessible to your audience?

It is but I have decided to keep the default colors that python generates the graphics with, so it is not shielded against color blindness problems. 


# Act

This step aims to organize the deliverables. 

* What is your final conclusion based on your analysis?

The conclusion is that there are subgroups of Colombian students that require greater attention and the creation of public education policies that allow them to improve conditions and obtain better results in the Saber 11 tests.

* How could your team and business apply your insights?

They help support the need to create public policies that seek to improve education in areas such as social sciences, natural sciences and English, the implementation of the full school day at the national level, encourage the use and facilitate access to internet and computers, and the improvement of nutrition; providing a more balanced diet in which food is consumed on a daily basis. As well as creating policies focused on students belonging to the lowest socioeconomic strata, students whose parents did not complete high school, a group of departments that have the lowest performance, and attention to ethnic minorities.

* What next steps would you or your stakeholders take based on your findings?

They need to take the findings an establish public policies, we can create a classification model to generated a tool that can classify a student at risk of failing the Saber 11 exam based on the demographic data, in order to offer guide and review educational gaps, or enter in national support programs. 

* Is there additional data you could use to expand on your findings?

Yes, it is necessary to include information on the student's performance in school, such as historical grades in subjects or student profile surveys.

## Bibliography

[1] Wikipedia, consulted: 20/07/2022 https://es.wikipedia.org/wiki/Examen_ICFES















