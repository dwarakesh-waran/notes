Topic: [[My Learning]]

If a process which has n items takes T(n) time, then these 3 notations are used to address the T(n) based on the actual time.

Lets understand this with an analogy.

If a process takes 1.9 seconds to execute, then the T(n) can be addressed in 3 ways as follows.

1. Theta Notation of T(n) is 1.9 seconds or 2 seconds.
2. Big O Notation of T(n) is 2 seconds but not 1.9 seconds.
3. Omega Notation of T(n) is 0 seconds but not 1.9 seconds.

- So, If the running time of an algorithm is Ө(n), that means it roughly runs in time cn for some constant c.
	- So, from the above example Ө(n) can the exact value or the at most value. Screenshots are given in [[Time Complexity]] 
- If the running time of an algorithm is O(n), that means it runs in time at most c’n for some constant c’