
# Adverse Reaction of Vaccination : Side Effects Clustering and Risk Prediction methods

Proposal By :

Sharath Srinivas

Chetan B Desai

Saideep Malgireddy

![images](https://user-images.githubusercontent.com/60420184/153628674-3a71f712-4f3c-4055-9570-c4a0b5329312.jpg)


## Introduction
There are no vaccine, drug or medical devices which are completely free from the side effects. Vaccine protects many people in Fighting the pandemic like Covid-19. So Its important for any healthcare proffesionals or End users of Vaccine must be aware of the side effects and to prevent any life threathening situtaions.

Anyone who has received a vaccine and had an adverse reaction should file a VAERS report online, even though they are unsure that the vaccine is to blame. So, This project makes use of data from the Vaccine Adverse Event Reporting System (VAERS), which was designed by the Food and Drug Administration (FDA) and the Centers for Disease Control and Prevention (CDC) to receive reports concerning vaccine-related adverse events.


## Background


## Goals

The goal of this Project is to group various vaccination adverse events. The project's goal is to first gain a thorough understanding of the most common types of adverse reactions, and then to determine suitable manufacturer of a particular vaccine which has least side effects based on their medical history, allergies, gender and age. Classification based on common symptoms and patient information to anticipate the need for urgent care. Clustering (unsupervised machine learning) is used to segment individuals based on undesirable reactions.We plan on providing Web interative application using python Dash, Django or Flask for patients and medical professionals which helps them to determine best suitable vacination based on their health records to reduce the life threatening incidents to decide on their vaccine immunization. 

## Data Preprocessing
Using glob to separate VAERSDATA.CSV,VAERSVAX.CSV,VAERSSYMPTOMS.CSV files from the raw data obtained from VAERS website,
checking the information of the dataframe to be consider,
Storing the data back in the drive for further consideration,
Taking care of Missing values, 
Taking care of Categorical Features, 
Normalization of data set.


## EDA(Exploratory Data Analysis)

This project makes use of data from the Vaccine Adverse Event Reporting System (VAERS), which was designed by the Food and Drug Administration (FDA) and the Centers for Disease Control and Prevention (CDC) to receive reports concerning vaccine-related adverse events. Medical practitioners are urged to report adverse events, and VAERS data may include coincidental events that are unrelated to the vaccine.In addition, due to the human factor in data input, we should expect incomplete examples.

<a href="https://vaers.hhs.gov/data/datasets.html">Dataset</a> 

<a href="https://vaers.hhs.gov/docs/VAERSDataUseGuide_November2020.pdf">Data Guide</a>

The VAERS data can be accessed by downloading raw data in comma-separated value (CSV) files.
The following datasets consists of 3 files from year 2010 to 2022: VAERSDATA, VAERSSYMPTOMS, and VAERSVAX. 

VAERSDATA provides the event IDs (VAERS ID) as well as personal information such as age, gender, symptom, allergy type, medical history, deceased, hospitalized, and life threat.

VAERSSYMPTOMS contains The events' IDs and symptom keywords retrieved from the symptom text in VAERSDATA.

VAERSVAX inscribes vaccine types and vaccine manufacturers.

We have select below vaccine as part of our project : 

1. COVID19 (COVID19 VACCINE)
2. VARZOS (VARICELLA-ZOSTER VACCINE )
3. HEP (HEPATITIS B VACCINE)
4. FLU (INFLUENZA)



#### Steps Carried out as a part of Exploratory Data Analysis:

1) Considering the respective vaccines data from the drive where we stored our data as a part of Preprocessing techniques.
2) Then Describing the Data, checked for duplicate values or missing data, dropping the columns which are not required for our modelling.
3) Converting the Date columns to the Datetype, converting sex to binary 0 for female, 1 for male, 2 for not known, applying regular expression to clean the columns such as "SYMPTOM_TEXT", "OTHER_MEDS", "HISTORY" etc.
4) We filtered only the vaccine data which is after january 2021, we created a new column serious from serious = vaers_covid[['DIED', 'L_THREAT', 'HOSPITAL', 'X_STAY', 'DISABLE', 'BIRTH_DEFECT']].copy() and named 1 being life threatening and 0 being Life threatening.
5) We plotted age distributions and the box plot to identify the outliers in them, we considered the age group of vaccines to be between 18 to 100,
![download (1)](https://user-images.githubusercontent.com/11175353/166147134-d5fdff80-b7b5-4967-8189-ac53ac916da5.png)
6) Distribution of adverse event severity based on age.
![download (2)](https://user-images.githubusercontent.com/11175353/166147333-e525258e-5c10-4039-bc96-bdae3f87a80b.png)
7) Seriousness plot of vaccines based on vaccine manufacturers
![Screenshot 2022-05-01 075105](https://user-images.githubusercontent.com/11175353/166147139-8fc7545f-6010-4c3a-a4af-efe2dd89f66f.png)
8) Compairing the seriousness between the genders
![Screenshot 2022-05-01 075136](https://user-images.githubusercontent.com/11175353/166147140-1fa667c7-1a4a-4bd0-8f52-35b488507fc5.png)
9)Seriousness plot based on age category and also the gender distribution
![Screenshot 2022-05-01 075237](https://user-images.githubusercontent.com/11175353/166147142-cfb65898-324a-41bc-9950-3b3e00cbe241.png)
10) PLot of death vs age category for genders.
![Screenshot 2022-05-01 075410](https://user-images.githubusercontent.com/11175353/166147143-e5caaf90-689f-416d-a468-4c114129d367.png)
11) Word cloud for covid vaccine in its shape
![Screenshot 2022-05-01 075439](https://user-images.githubusercontent.com/11175353/166147144-40f016a4-a34d-45c1-8ac3-e4197cc634f2.png)

 













### Team Roles and Responsibilities

**Chetan B Desai (Captain)** ***: Project Manager***

◈ Data Cleaning Clean Textual data using Natural processing Language

◈ Classification: SVM and K-nearest neighbor

◈ Clustering : K Means 

**Sharath K Srinivas** ***: Deliverable Manager***

◈ Exploratory data analysis

◈ Classification: Multi-layer Perceptron classifier and Random forest

◈ Clean Textual data using Natural processing Language

◈ Clusturing Interpretation 

**Saideep Reddy** ***: Reference Manager and Project Editor***

◈ Logistic Regression and Decision tree

◈ Model Comparison

◈ User Interface using plotly or flask

#### Weekly Meetings

Along with all the task assigned above we also sceduled a weekly meeting on Tuesdays, Fridays and Sundays from 11:00 Am to 2:00 PM to discuss the staus of the project and to resolve any issues regarding the same. 

## Reference 

[1]. https://www.cdc.gov/coronavirus/2019-ncov/vaccines/safety/adverse-events.html

[2]. https://pubmed.ncbi.nlm.nih.gov/15071280/


youtube vedio link for EDA first phase: https://youtu.be/VX2x8jXAEHY
