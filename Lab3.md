Part 1:
ArrayExamples.java bug
reverseInPlace method:

a)
```
input = [1, 2, 3, 4, 5];
```

b) 
```
input = [1, 2, 3, 2, 1];
```

c)
![image](https://github.com/jgu0453/CSE-15L-lab-reports/assets/119398520/1a07583e-692e-4e1e-bb5b-c0879ba7f653)

![image](https://github.com/jgu0453/CSE-15L-lab-reports/assets/119398520/88887651-671f-443a-8ab1-430bb4222e75)


d)
Before:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < (int)arr.length/2; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
After:
```
static void reverseInPlace(int[] arr) {
    int x;
    for(int i = 0; i < (int)arr.length/2; i += 1) {
      x = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = x;
    }
  }
```
The issue is that the original value in the arr[i] is not being temporarily stored, so the first half of the array is lost. The fix stores arr[i] as a temporary value then reassigns it to the respective spot in the array. 

Part 2:

Chose grep command.
4 options for this command:
1. grep -i : ignore case
2. grep -c : only prints count of lines that match pattern
3. grep -n : display matched lines and their line numbers
4. grep -v : print all lines that do not match the pattern



