# **Factorial QA Testing**

  For testing purposes I have picked a web application developed for helping QA testing which can be accessed through the following link : (https://qainterview.pythonanywhere.com/) . The application has the purpose of calculating the factorial of a number entered by the user.
  
  Due to the fact that there was no documentation provided for this application, the test planning was not based on any therefore I have decided to do exploratory testing instead.
  
  All of the test cases were performed on the three most commonly used browsers: Microsoft Edge, Chrome and Firefox.
  
  ## Summary
  
  The test plan performed on this application is composed of the following suits of test cases :
  - UI/front-end testing : all the elements of the user interface (Page Header, Input Field, Button, "Terms and Conditions" hyperlink, "Privacy" hyperlink, Footer hyperlink) were tested in order for them to be correct, relevant to the theme and interactible
  - functionality testing : the Input Field, Button and hyperlinks were tested to verify that they are functional and they work as they should
  - validation/negative testing : various types of inputs were tested to make sure the correct result/error message is displayed upon calculating

## Factorial Test Cases Suites

### Website link Suite
  
   The first test I performed was making sure that the link is functional. After being able to access the website, I checked if the Website Title is correct and consistent with the purpose of the application.
   
   During this step I have also noticed that the Website does not have a personalized icon and the stardard one is shown instead.
   
   Performing the test run for this suite had the following results: 
   
   - Website link is functional: I was able to access the provided link - passed
   - Website Title is correct and relevant to the theme: while the Title is relevant to the theme, it was spelled incorrectly as "Factoriall" instead of "Factorial" - failed
   - Website has an icon: the Website icon is visible, but the standard one is displayed instead of a personalized one - failed

For both the Website Title and the Website Icon test cases I created a defect detailing why they failed: which were the expected and the actual results.
   
   ### User Interface Suite
   
   After accessing the website, the next step was verifying that the UI elements load up correctly and there is nothing missing or showing inappropriately. The following elements were verified : Page Header, Input Field, Button, "Terms and Conditions" hyperlink, "Privacy" hyperlink, Footer hyperlink. I checked if all are written correctly, the text is relevant to the theme and that they are all interactible.
   
   Performing the test run for this suite had the following results:
   
   - Website elements load up correctly: all the UI elements showed up as expected - passed
   - Page Header is correct and relevant to the theme: the Page Header is "The Greatest Factorial Calculator!" and it is spelled correctly and in accordance with the application theme - passed
   - Input Field shows intuitive placeholder text: the placeholder text is "Please enter an integer" so it is suitable - passed
   - Button text is correct and relevant to the theme: the Button shows the "Calculate!" text so it is correct - passed
   - "Terms and Conditions" hyperlink redirects the user to the "Terms and Conditions" Page: clicking the hyperlink did not redirect to the correct page, it loaded up the "Privacy" Page instead - failed
   - "Privacy" hyperlink redirects the user to the "Privacy" Page: clicking the hyperlink did not redirect to the correct page, it loaded up the "Terms and Conditions" Page instead - failed
   - Footer hyperlink redirects user to the correct page: clicking the hyperlink loaded the following website: (https://qxf2.com/) and it is correct - passed

"Terms and Conditions" and "Privacy" hyperlinks loaded up the incorrect pages. I created defects for both of the test cases mentioning what the expected result was upon accessing the hyperlinks.

### Input Field Suite

Given that the Input Field was interactible, I was able to test various types of inputs in order to determine if the correct result/error message is displayed in accordance with the case.

During this step I verified if entering integer type inputs will display a result and if any other type of inputs (string type, symbol type, float type) will show an error message. I also checked if mistakenly entering blank spaces in front/in the middle/after the number has any effect on the result and if trying to calculate a number starting with "0" or "0" itself will display a result or an error message. 

As a final test, I verified if larger numbers will eventually display a result such as "Infinity" and if four-digits numbers will display an error message.

Performing the test run for this suite had the following results:

- User is able to enter value in the input field: input field was responsive and I was able to enter a number in it - passed
- User can calculate integer type inputs: I was able to calculate the valid type of input and doing so displayed a correct result (eg: calculating "3" displayed "6" as a result) - passed
- User can calculate numbers starting with "0": calculating numbers that start with "0" still displays a correct result (the "0" in front of the number is ignored) (eg: calculating "03" displayed same result as calculating "3") - passed
- User can calculate "0!": calculating "0!" displayed the result "1" which is correct - passed
- Blank spaces before and after the number are ignored: I entered blank space in front/after the number and upon calculating the correct result was shown (eg: calculating " 3" and "3 " showed the same result as calculating "3", which is "6") - passed
- User cannot calculate numbers with blank space in between digits: calculating two or three-digits numbers with a blank space in between digits displayed the "Please enter an integer" error message which is the correct result  (eg: calculating "1 3") - passed
- User cannot calculate string type inputs: calculating a string type input such as "a" displayed the "Please enter an integer" error message which is correct - passed
- User cannot calculate symbol type inputs: calculating numbers with any type of symbols such as "-3" displayed the "Please enter an integer" error message which is correct - passed
- User cannot calculate float type inputs: calculating decimal numbers such as "1.3" or "1,3" displays the "Please enter an integer" error message which is correct - passed
- Numbers greater than "170" display "Infinity" as a result: calculating numbers larger than "170" displayed the "Infinity" result which is correct - `passed`
   





- ui/front-end 
- functionalitate
- edge-case
- negative-testing


- reported issues
- icon missing
