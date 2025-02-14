Topic: [[My Learning]], [[Sort]]
- Merge Sort is Cache friendly
- Merge Sort is stable
Steps
- Its a divide and conquer algorithm
- Find the middle element of the array and divide the array (use recursion)
- After dividing the array into 2, use left and right pointers on start of each of the arrays.
- Then compare the values of the pointers.
- Create an auxiliary array
- If the value of left pointer is less than or equal to the value of right pointer, add the value of the left pointer to an auxiliary array.
- Else add the value of the right pointer to that auxiliary array.
- At last, fill all the values to the auxiliary array and merge the values in the aux array to the original array.
