Topic: [[My Learning]]

In the event of an array containing duplicates, the sorting technique should previous the order of the duplicates.

Since Selection Sort and Quick Sort are using randomized swapping, the order cannot of the duplicates cannot be preserved and hence are not Stable.

[[Insertion Sort]] can be stable or unstable based on a small catch.
During the shifting phase of Insertion sort, we shift the left values to the right till be find a a value which is lesser than the current value. 

IF THE COMPARISON OF THE CURRENT VALUE IS LESS THAN THE LEFT VALUE, THEN THE INSERTION SORT WOULD BE STABLE.
IF THE COMPARISON OF THE CURRENT VALUE IS LESS THAN **OR EQUAL TO** THE LEFT VALUE, THEN THE INSERTION SORT WOULD BE UNSTABLE BECAUSE THE DUPLICATE VALUE WILL ALSO BE SHIFTED FROM LEFT TO RIGHT AND THE ORDER WOULD BE CHANGED.

![[Pasted image 20241201201223.png]]