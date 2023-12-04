Lab Report 4

Steps 4-9:

Step 4:

type 

ssh cs15lfa23hx@ieng6.ucsd.edu <Enter>


Step 5:

clone repository lab7


Step 6:

type

javac -cp ".;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar" *.java <Enter>

java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore ArrayTests <Enter>

bash test.sh <Enter>


Step 7:

type

vim ListExamples.java

j until error line

l until cursor over 2

x

i

2

esc

:wq <Enter>


result:
![image](https://github.com/jgu0453/CSE-15L-lab-reports/assets/119398520/a9353a19-fbd6-46e5-bd04-7ca060d50a60)


Step 8:

type

bash test.sh <Enter>


Step 9:

type

git push origin main


