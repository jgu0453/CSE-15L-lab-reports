Lab 9

Student Question:

Hi, I was trying out the bash script for list examples and list test examples and I changed the code index1 to index2 but the code still does not run. I am unsure why because everything looks correct.

Here are screenshots of my code and terminal:

![image](https://github.com/jgu0453/CSE-15L-lab-reports/assets/119398520/b8586a00-2b9f-4fd9-9a34-fba342199a95)

![image](https://github.com/jgu0453/CSE-15L-lab-reports/assets/119398520/4c3e3cf8-c962-4a08-b10c-ed764918aca6)




TA Response:

After looking through your code, there is nothing wrong with the bash script.

The problem is in your code.

For the merge method, the conditions for the while loop are causing the error because it should be an && instead of ||, otherwise it is possible for one of the indices to increment outside of the bounds of their list size.

Try that to see if it works.





Student trial:

That worked, Thank you very much.

![image](https://github.com/jgu0453/CSE-15L-lab-reports/assets/119398520/635202ae-1618-40bc-938e-82365a01f51f)

![image](https://github.com/jgu0453/CSE-15L-lab-reports/assets/119398520/9c7de6f9-705e-4194-b44f-31499b63584a)







