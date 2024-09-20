# Programming Assignment 4
## ECE Board Exam Problem: 
Using data wrangling and data visualization technique with storytelling, analyze the data and present different (i) data frames; and (ii) visuals using the dataset given.

### INTRODUCTION
Data analyzation can be overwhelming if it is not well-presented in an organized manner. As discussed, data wrangling (or also known as data munching) is a process of cleaning, organizing, and transforming raw data into a more organized in order for it be easily navigated. For this programming assignment, there was a given csv file that contains the data to be extracted as the main data frame. In the board2.csv file, there are 8 columns namely as 'Name', 'Gender', 'Track', 'Hometown', 'Math', 'Electronics', 'GEAS', and 'Communication'. Furthermore, there are a total of 30 rows of students data. Now, how do we comply to the set of instructions given?

#### A. Students (Hometown is Luzon; Track is Instrumentation)
For the first instructions, we have to filter the main dataframe by only listing those students whose hometown is 'Luzon' and their track must be 'Instrumentation'. Additionally, the program must only output the following information: 'Name', 'GEAS', 'Electronics > 70'. However, there is an additional condition that their score in the 'Electronics' subject must be more than 70. How do we do that?

##### STEP 1: Import the Pandas Library
Before we proceed with the actual coding, never forget to import the Pandas library first in order to gain access to its functions.
![image](https://github.com/user-attachments/assets/360d4459-806f-4539-adfc-1c4196602df8)

##### STEP 2: Load the .csv File into the Data Frame
In order to load the .csv file into the Data Frame, the syntax "pd.read_csv('board2.csv')" has been utilized. After loading the data frame, it was assigned to variable named "ece".
![image](https://github.com/user-attachments/assets/30ae7d52-4de2-4e38-bf69-06164c95365c)

##### STEP 3: Set the Conditions
As shown in the image below, locate function was used. Firstly, the program checks each row in line with the 'Track' column if the student choose 'Instrumentation'. After satisfying the condition, using the notation & (and), the program will then check if the 'Hometown' is 'Luzon'. Lastly, the program will also check if the student's score in Electronics is greater than the assigned value of 70. After setting up the conditions, the next line of code allows you to type in the names of the columns that you only wish to print.
![image](https://github.com/user-attachments/assets/302204ce-1396-4aeb-9d08-a5dec1e594d0)
##### STEP 4: Print the Output
For printing the output, simply type the assigned variable name "Instru".
![image](https://github.com/user-attachments/assets/8778d049-e032-4b7f-9254-66a2bf97bc21)

#### B. Students (Hometown is Mindanao; Gender is Female)
For the next instructions, we have to filter the main dataframe by only listing those students whose hometown is 'Mindanao' and their gender must be 'Female'. It almost have the same steps as the first instructions, however, it has an additional instruction of: the average of the four scores in Math, Electronics, GEAS, and Communication must be greater than or equal to 55. How do we do that?

##### STEP 1: Solve for the Average Score of Each Student (EACH ROW)
Let's focus on calculating the average first by using the syntax presented below. The following syntax allows the program to add another column in the data frame and named is as 'Average'.
![image](https://github.com/user-attachments/assets/2588a05d-a295-4f5f-90e8-1bdac8bd8d69)

##### STEP 2: Set the Conditions
Just as the same as we did in the first part of this experiment, write a code that includes all the conditions stated. Then, only print the columns 'Name', 'Track', 'Electronics', and 'Average'. Additionally, for this one, in order to have an organized indexing at the left side of the output, add a syntax ".reset_index(drop=1)".
![image](https://github.com/user-attachments/assets/1680a9d1-4a4f-4c9e-b7b0-c3aeb2fa25f3)

##### STEP 3: Print the Results
For printing the results, simply type the assigned variable name "Mindy".
![image](https://github.com/user-attachments/assets/102076ba-e528-415b-97a8-68174178072b)

### VISUALIZATION
**Task:** Create a visualization that shows how the different features contributes to average grade. Does chosen track in college, gender, or hometown contributes to a higher average score?

There are a lot of ways in order to present data, some of them are through tables, charts, infographics and many more. My personal favorite of presenting data is through graphs! For the next part of the experiment, I used bar graphs in order to visualize whether chosen track in college, gender, or hometown is an aspect that affects the average score of the student. How do we do that?

##### STEP 1: Import the Matplot Library
In order to output graphs, we firstly have to import the matplot library as plt. The image below shows the actual syntax in importing the aforementioned library.
![image](https://github.com/user-attachments/assets/860c2c97-b26e-4470-8eed-56bc3cf31054)

##### STEP 2: Creation of the Graph
Since I choose to create a bar graph, I have to used the syntax plt.bar and then, assign the x and y variables. In this case, I have created three different bar graphs and I just simply change the x variables to 'Hometown', 'Track', and 'Gender'. While the y variable remains to be the 'Average'. It would then automatically output the results.
![image](https://github.com/user-attachments/assets/250f1bfa-e337-4500-98fc-e89062799318)
![image](https://github.com/user-attachments/assets/f6315375-6b7a-46b8-a94a-8b94fbed4851)
![image](https://github.com/user-attachments/assets/419c0397-b02d-46d7-bb24-43a5cf220aa6)

### INSIGHTS
_Does chosen track in college, gender, or hometown contributes to a higher average score?_

Based on my observation in the graphs, the chosen track in college, gender, and hometown does not siginify relevant correlation with the average score accumulated by the students. There is no significant difference between the bar graphs of each variable. Hence, all of the aformentioned variable does not contribute to getting a higher average score.
