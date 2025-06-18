#       
* * *
## [Contact](./contact.md)
* * *


<img src="https://media.licdn.com/dms/image/v2/C4E03AQEv4RXCekqU_w/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1534002520117?e=1753920000&v=beta&t=2E5gE2OS8GrbyiLFLEeSolaDUhzz438p6U9fTRv-ktI" alt="My Photo" 
     style="width:150px; height:150px; border-radius:50%; border: 3px solid #ccc;">
     
# About Me:

I am a Senior Analyst with over a decade of experience in the AML Compliance/Banking industry, and aspiring Data Scientist. Currently, I'm pursuing a BSc. in Data Science, Innovation Management and Computer Science to formalize and improve upon existing skills.

* * *

# Projects


* * *

## Staff Training Dashboard

### Overview

 This is a relatively simple dashboard that seeks to answer three questions - who needs training? On which employees does the Manager need to focus efforts to bring the company into compliance and reduce risk exposure due to lack of training? When will upcoming training sessions take place? How can the manager quickly act on the information available? This solution provides immediate in-report access to real time information on upcoming training and immediate action to notify relevant persons.

The Staff Training Dashboard was developed to track key performance indicators of the AML/CFT Compliance Training Program for all employees across a financial institution. It provides Compliance Leadership with a bird's eye view of the performance of the training program over time, and a real time snapshot of company progress in ensuring that 100% of the staff meet the AML/CFT training requirements based on established policies and legal/regulatory requirements. 

The Dashboard highlights employees that may not be on track to completing the required amount of Continued Professional Education credits as it relates to AML/CFT Compliance, and also provides an immediate solution, by displaying the dates, times and titles of upcoming training sessions [webinars] so that the Manager can make recommendations to the appropriate Department Head, for the required training to be facilitated, if needed. 

 A report has been created for anyone to use which allows the viewer to see upcoming webinars hosted by ACAMS, and includes a button which leads directly to the website’s webinar catalog in order to register.


### Data Model - Visuals



### Data Model - Description

 The Database Schema consists of 7 tables shown above and a brief summary of the nature of the dataset for each is provided below.

### Employees

This table holds all of the employees of the company. It includes an ID [Integer, Primary key], first name, surname, Job Level, Department, Employment Status, Start Date and Termination Date. 

### Employment Status

This is a fact table that stores possible options for employment status of employees. Current options are *Active* and *Terminated.* It is connected to the Employees table via EmploymentStatusID.

### Departments

This is a fact table that stores the ID and Department name of the company. The ID here is a foreign key in the Employees table as DepartmentID.

### Job Level

This is a fact table that stores the ID and Job Level options of the company. The ID here is a foreign key in the Employees table as JobLevelID.

### Training Sessions

This is a fact table that stores all the unique training sessions undertaken by any employee of the company. It’s primary key, id, is foreign key in the AttendanceLog. Other information stored in the table include the training session title, date, credits earned from attending the session, the facilitator, and the training type [TrainingTypeID], for example, Ethics, Corporate Governance, AML Compliance, BSA.

## Training Type

This is a fact table that stores the ID and description for the subcategories of training sessions related to AML/CFT Compliance. It’s ID [primary key] is a foreign key in the Training Sessions table [TrainingTypeID].

#### Attendance Log

This is a dimensional table that captures each instance of an employee’s attendance at a session. It includes the SessionID, which is the id from the Training Sessions table, Attendee ID, which is the id from the Employees table, and Completion Status.

## Insights

So far only one employee from a low-risk category is not on track to meeting training requirements. Perhaps this means that the company is finally improving on compliance with training requirements. Risk categories need to be assigned to employees for a more targeted report.

Whilst overall the company appears to have struggled and has not been hitting targets as it relates to meeting staff training requirements, specific departments have been meeting training requirements over the past 2 years. When filtered to exclude employees who have been terminated, Investments, Compliance, Private Banking and Legal departments all met training requirements consistently since 2023, and are on track to meeting requirements in 2025.

Further attention needs to be placed on Customer Service.

Training tends to spike annually in February, March and August. There is not enough contextual data to infer the reason for this. However, it provides insight into planning for future training sessions. A manager might want to study the company calendar/agenda closely for additional opportunities to stitch in vital training for employees not in compliance with the training policy.


