# No Show Appointment Data Analysis
### By Anthony Eze

### Introduction
This dataset collects information from 110,527 medical appointments in Brazil and is focused on the question of whether or not patients will show up for their medical appointment. It would be used to answer some questions like what is the most likely factor that makes patient no show up for their appointment.

Some of the questions to answer from the analysis

- Do females value their health more than males do, based on the No-show appointments Dataset?
- Does the hospital's location affect whether patients show up for their appointments?
- Do patients' health conditions affect whether they show up for appointments? What proportion of patients with medical issues keep their appointments or fail to show up?
- What's the correlation between age and showing up for appointments. Do younger population show up for appointment?
- Does sending an SMS reminder help to reduce the no-shows?

### Preliminary Data Wrangling
The following actions have to be performed on the dataset to prepare it for analysis:

- The column names have to be modified so we can utilize and address with ease e.g No-show changed to no_show
- Checked for null and duplicated rows
- dropped the '-1' row on the age column as it is assumed to be an error
- dropped the the columns PatientId and AppointmentID since they appear to be randomly produced integers by a computer.
- converted the ScheduledDay and AppointmentDay to date-time format
- converted the following columns (Scholarship,Hypertension,Diabetes,Alcoholism,SMS_received and No-show) to bool since they represent True or False

### Summary of Findings
From the analysis, below are some of the findings as related to the main features (No-show):

Exploring the data gave us some insight into the data as we compared some of the variables to the No-show variable.

Variables such as Gender, Age, Scholarship, Hypertension, Diabetes, Alcoholism, and Handcap are the independent variables and No-show is the dependent variable.

From the analysis, we can see that variables such as Scholarship, Hypertension, Diabetes, and Alcoholism are not the variables that can be used to predict if a patient scheduled for appointment would show up or not. This is evident from the proportional on the percentage of the variables with no-show. In most of this proportion, patient with scholarship and didn't show up is greater than that of the without scholarship and didn't show up.

Also, Having limitations such as Hypertension, diabetes, alcoholism, and handicap is not a factor that can be used for the prediction

### Limitations on the project
- The Handcap variable that is supposed to be boolean, happen to have multiple input values (0 to 4) and the SMS_received variables that is suppose to have a multiple input has a boolean data. An explanation on this discripancies could help us to have a good insight into the data.
- The proximity of the patient residence to the neighborhood is not given. This can also be a factor to consider, knowing the distance from the patient residence to the neighbourhod can let us know if the patient can easily found her way to the appointment center.
- The Appointment date and Scheduled date is the same, we need some clarifications on this, is the scheduled date same as appointment date? If so, why do we need to send an SMS to them again when the appointment date is the same as the scheduled day.
- The statistics employed here are descriptive rather than inferential, hence no hypotheses, controlled experiments, or inferences were made using the data.
- Additionally, the insights produced are dependent on the questions posed at the start of our analysis, so additional insights may still be discovered.
