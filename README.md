# Python project to manage student performance and track grades with Object Oriented Programming
To make this project, I used the Google Colab as the Integrated Developement Environment with using the Jupyter Notebook , following are the steps , I used to make this Project Successfully

1. First, I created a **Class** of Students and make the **Attributes** of Name, Age, Gender And Roll Name with the use of _init_ constructor with using *self* and then added more attributes like the scores of the students like *score_in_math , score_in_physics , score_in_computer , score_in_english , score_in_chemistry , score_in_science* .
2. Now for string attributes like Name , Gender , Age , Roll Number And Scores, I created a special function name **only_str** with the self and **user_input** attribute and used an **Input()** in it with the Help of the **While Loop**  and to check the validity of the user input as the user only enters the input in strings , I used a Switch/Flag named **Valid Input** in it and also as per the requirement of the Project , I also make use of the Proper Error Handling using **Try/Except**, first I make use of the **if** statement to check if the user enters an empty input and set to raise a **ValueError** to run the **Except** Block printing error message , then used a **for loop** to check all the characters in it by the use of special string functions like **char.isalpha And char.isspace** and at last if the output is valid **return** it to save it in the respective variable.
3. Now for the Integers input , I made a separate function named **only_int** and used the *int()* to check the validity of the input and used the **Try/Except** handling for proper error handling
4. Then for the scores , making a separate function for it named **only_score** and used an **if** condition in it to keep the input between 1 and 100 and the same empoying proper Error Handling in it
5. Created a function for average and checking if the student is passing in each subject or not , used simple math formula in the **calculate_avg** function and for **is_passing** function, first used an empty list and make use of the **if/else** statement in it with the use of the input given by user decided passing or failing criteria and appending the output for each block of code in the empty list and then printing the list.
6. And At the top, I make use of the special method naming **_str_** as I cannot return any value after the **_init** constructor to display all the result of the data entered by the user.
7. Now , I created a Class name Performance Tracker To Track the Info of the student, Performance_tracker Class. This class is designed to handle the core functionalities of adding students, displaying their information, and calculating the class average. It requires a dictionary (student_dict) as an argument, where each student's name is stored as a key and their Student object as the value.
8. Methods in Performance_tracker
 
 * __init__(self, student_dict)
Initializes the Performance_tracker class with student_dict, which stores students' details.
add_student(self)

* Prompts the user to create new Student objects and adds them to student_dict using the student's name as the key.
Repeats this process until the user opts to stop adding students.
Provides feedback on successful additions, confirming each student's addition to the Performance Tracker.
Validates user responses for adding more students, accepting only “yes” or “no” answers.
display_students_info(self)

* Checks if there are any students in student_dict.
If the dictionary is empty, it notifies the user that no students are currently in the tracker.
If there are students, it iterates through student_dict, printing each student’s detailed information (utilizing the __str__ method from the Student class).

* Calculate_class_average(self)
Calculates the class average score based on all students in student_dict.
Iterates through each Student object in the dictionary, summing up their averages (calculated using the calculate_average method from the Student class).
Computes the class average by dividing the total sum of averages by the number of students in student_dict.
If there are no students, it returns a message indicating that the tracker is empty.
Outputs the class average as a formatted string with two decimal places.

9. Now I created a Function name **The input_student** function is designed to create a dictionary of student records, prompting the user to enter each student's details and store them in a structured way. This function also computes the class average score by utilizing the Performance_tracker class once all students have been added.

* Initialize student_info_dict
A dictionary, student_info_dict, is created to store each student's name as the key and the Student object as the value.
Student Input Loop

* The function enters a while loop that allows the user to add multiple students.

* Student Creation
For each iteration, a new Student object is created, prompting the user to input all necessary details such as name, age, gender, and scores in different subjects.
Each Student object is added to student_info_dict with the student's name as the key.
* Adding Confirmation
A message confirms each student's addition to the database, displaying the student's name.
* User Prompt for More Entries
After adding a student, the function prompts the user with "Do you want to add more students Yes/No."
If the user inputs:
"No":
The function exits the loop and proceeds to print all student details from student_info_dict.
It then calculates and displays the class average by creating an instance of the Performance_tracker class and calling its calculate_class_average method.
"Yes": The loop continues, allowing the user to add more students.
Invalid Input: If the input is neither "yes" nor "no," an error message prompts the user to enter a valid response.
Printing Student Details

* Once the user chooses to stop adding students, the function iterates over student_info_dict and prints each student’s details by calling the __str__ method from the Student class.

* Calculating Class Average
After displaying individual student details, the function calculates the class average by:
Creating a Performance_tracker instance with student_info_dict.
Calling the calculate_class_average method, which computes and returns the average score of all students in the dictionary.
Finally, the calculated class average is printed for easy reference.

