
# Analyzing the Medical Appointment No Shows Kaggle Dataset
### by Mário Damhur

Also, you can check the blog post about this project: [medium](https://mriodamhur.medium.com/data-analysis-of-medical-appointment-no-show-in-brazil-e05bda56d173) 

## CRISP-DM

### Business Understanding

A person makes a doctor appointment, receives all the instructions and no-show. Who to blame?
Some questions to answer:
- What are the age groups patients who have most turned up?
- People who have some disease/disability usually turned up?
- The Scholarship (Bolsa Família) for each gender contributed to turned up?
- What is the impact of the location for the patients to turned up?

There are a lot of other questions that we can ask, but for this project I limited the escope for them. :)

### Data Understanding

This [dataset](https://www.kaggle.com/joniarroba/noshowappointments) collects information from 100k medical appointments in Brazil and is focused on the question of whether or not patients show up for their appointment. A number of characteristics about the patient are included in each row. 110.527 medical appointments its 14 associated variables (characteristics). The most important one if the patient show-up or no-show to the appointment. Variable names are self-explanatory.

- **PatientId**: Identification of a patient
- **AppointmentID**: Identification of each appointment
- **Gender**: Male or Female.
- **DataMarcacaoConsulta**: The day of the actuall appointment, when they have to visit the doctor.
- **DataAgendamento**: The day someone called or registered the appointment, this is before appointment of course.
- **Age**: How old is the patient.
- **Neighbourhood**: Where the appointment takes place.
- **Scholarship**: True of False . Observation, this is a broad topic, consider reading this article https://en.wikipedia.org/wiki/Bolsa_Fam%C3%ADlia
- **Hipertension**: True or False
- **Diabetes**: True or False
- **Alcoholism**: True or False
- **Handcap**: Number of handicaps this person have [0,1,2,3,4]
- **SMS_received**: True or False.
- **No-show**: True or False.


### Prepare Data

Here I did the Data Wrangling process: Find issues, remove unnecessary data, deal with missing values, feature engineering, etc... All this steps to create a clean dataset. You can see more about the decision that I made on the jupyter code.

### Data Modeling

It is not always about machine learning! In this case, I used descriptive statistics to answer the business questions.

### Evaluate the Results

Results of the questions (Insights!):

- In general, there are more people who turned up than not turned up.
- Female is the greater proportion, woman takes way more care of they health in comparison to man.
- The frequency or proportions results are different from the real relative proportion.
- The age group of 60-70 have more patients that turned up, on the other hand, the age group of 10-20 have more patients that have not turned up.
- Even though the people who have some disease/disability are the minority class, the relative proportion suggests that the people who have some disease/disability, usually turned up more or equal than people who don't have.
- The people who have scolarship (Bolsa Família) tends to not turned up in both genders.
- The relative proportion of all neighbourhoods have around 80% Turned Up Rate. Except the location 'Ilhas Oceânicas de Trindade', that don't have any turned up observation.

## Files

- **data**: This folder was create to save all the dataset downloaded.
- **investigate-a-dataset-template.ipynb**: The jupyter notebook with wrangling process and the exploration of the data.
- **investigate-a-dataset-template.html**: The HTML version of the jupyter above.
- **README<span>.md</span>**: This file.

## Python Libraries Used
- **numpy**
- **pandas**
- **matplotlib**
- **seaborn**
- **kaggle**
- **os**
