# EXPEPRIMENT-4_MACUNO_2ECE-A
## **I. Intended Learning Outcome:**
1. To identify the codes and functions needed in cleaning and visualizing data
2. To be able to apply and use the different codes and functions in creating a Python program that will
be used in data wrangling and data visualization

## **II. Instructions:**
Download the ECE Board Exam 2 dataset found on this link: bit.ly/ECEBoardExamDataset and write a
Python script/code in the Jupyter Notebook to do the given problems. You may submit your Jupyter
notebook in the dedicated submission bin.

## **III. Solution**

Use panda for data wrangling and manipulation
import panda as pd

Use matplotlib.pyplot for plots and visualization
import matplotlib.pyplot as plt

  ### **_NUMBER 1_**
          To print a dataframe with Name, GEAS, and Electronics who's Grades are more tha 70, and who only lives in Luzon with the track focused on Instrumentations.

          instrumentation = board.loc[(boards['Hometown'] == 'Luzon') & (boards['Track'] == 'Instrumentation') & (boards['Electronics'] > 70), ['Name','GEAS','Electronics']]
          instrumentation

![image](https://github.com/user-attachments/assets/5142f7a3-f8cb-42ac-bb52-9e29915e7fc1)


          To print a dataframe with Name, Track, Electronics, and an Average <= 55, and who only lives at Mindanao & are Female in Gender.

          board['Average'] = round(board[['Math', 'Electronics', 'GEAS', 'Communication']].mean(axis=1),2)
          Mindy = board.loc[(board['Hometown'] == 'Mindanao') & (board['Gender'] == 'Female') & (board['Average'] >= 55), ['Name','Track','Electronics', 'Average']]
          Mindy

  ![image](https://github.com/user-attachments/assets/b7a539fe-44a4-4119-8ae5-7e8e3d8ea6c9)

### **_NUMBER 2_**
matplotlib.pyplot is utilized to display various graphs comparing the average of different categories inside the dataset

1. Figure shows that Microelectronics has the highest average of all the Tracks

          plt.figure(figsize=(5,5))
          plt.bar(board['Track'],board['Average'])
          
![image](https://github.com/user-attachments/assets/e3235437-1ec3-4ffa-ab0b-cdd4fb0850b6)

2. Figure shows that Female has a higher average compared to Male

         plt.figure(figsize=(5,5))
         plt.bar(board['Gender'],board['Average'])

![image](https://github.com/user-attachments/assets/8a161402-3245-42b1-aa61-0a99c7f92d4d)

3. Figure shows that Luzon has the highest average of all the Hometown

         plt.figure(figsize=(5,5))
         plt.bar(board['Hometown'],board['Average'])

![image](https://github.com/user-attachments/assets/797d63ae-3150-4bda-8bd6-7f8dd1404059)


## VERSIONS

**1.2** - Completion of README File

**1.1** -  The initial draft was deleted and replaced with the final .ipynb file

**1.0** - The Repository is created and an initial draft of the code was posted
