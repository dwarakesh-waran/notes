Topic: [[My Learning]]

Analyzing the time complexity of an algorithm will take more time. We have analyze the factors and derive an expression in the end.

An example expression would be T(n) = an^2 + bn + c

That is it takes T(n) time to execute the algorithm with an input of n values.

Usually in interviews, we don't have to explicitly mention this quadratic expression as our time complexity. #qna Why?
Because this quadratic expression contains system-dependent constant like a, b and c. we can ignore these constant and our final value would be T(n) = n^2 + n + 1. We can still ignore the n+1 because when the size of n increases, the n + 1 would be very small. So, the final value would be T(n) = n^2 appx.

**So, this expression is called a asymptotic time complexity expression. We can get the asymptotic time complexity of an algorithm by considering the system-independent factor and by removing the constant and lower order values.**


![[Pasted image 20241127120023.png]]

---

![[Pasted image 20241127120050.png]]

---

![[Pasted image 20241127120146.png]]
#codecheck its should be Big O of n right?

---

![[Pasted image 20241127120649.png]]
![[Pasted image 20241127121020.png]]
![[Pasted image 20241127155449.png]]

![[Pasted image 20241129172917.png]]
#codecheck You can check the possibility of the whether the array is sorted or not and then you can run the any sorting algorithm. But if its not sorted, then the above statement would be false right? Then why the answer is true?

#### The explanation for below Screenshots are given in [[Difference Between Theta, Big O and Omega Notation]]
![[Pasted image 20241129173216.png]]
![[Pasted image 20241129173407.png]]

---

![[Pasted image 20241130205409.png]]
![[Pasted image 20241130205517.png]]****

![[Pasted image 20241130205745.png]]

The strategy behind the quicksort or a merge sort is Divide and Conquer. But if we are dealing with a sorted or reverse sorted array or an array which contains duplicates, then it will divide the values one by one making it a decrease and conquer. 

---

![[Pasted image 20241130210013.png]]
#codecheck I didn't understand this.

----




