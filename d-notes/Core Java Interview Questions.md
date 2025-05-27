Topic: [[My Learning]]

#link Mid Level Java Interview Questions: https://medium.com/@sjvoon97/mid-level-java-developer-interview-guide-java-questions-series-6ab7fc5bc262

>***Static Methods Can Be Overloaded but NOT Overridden***
>***Child is OVERRIDING and the Parent is getting OVERRIDDEN***
### Understanding the Method Hiding in Java is Very Important
![[Pasted image 20250504022129.png]]

One follow up interview question of method hiding is - ways to prevent method overriding in java.
- #link https://www.geeksforgeeks.org/different-ways-to-prevent-method-overriding-in-java/
Other common interview question related to this is - Can we override the static method in Java?

### Is it still method overloading when you just change the return type of 2 methods of the same name?
TL;DR - No its not, it will give you an error.
#link - https://stackoverflow.com/questions/2439782/overload-with-different-return-type-in-java
#link - https://stackoverflow.com/questions/442026/function-overloading-by-return-type
Basically, java (or C++) doesn't know which method to call if we have 2 same methods with a different return type. Some languages which achieves this are perl, haskell etc.,

### Is it possible to have a different return type when doing a Method Overriding?
Actually method overriding has strict restrictions. The method name and signature should be the same for both the method in parent and child classes.
But it is actually possible to have a different return type - this type of overriding is called **Covariant Overriding**.
#### **Note-1:** One more important restriction is **the overloaded method cannot throw a higher exception**

This restriction is only applicable for checked/compile-time exceptions. Not for unchecked/run-time exceptions as mentioned in the below table. So, even if even if the **parent method throws a `NullPointerException`**, a **child (overriding) method** can throw a **`RuntimeException`**. Refer the Note-2 for a follow-up question.

| Rule                                                         | Applies To     | Notes                                 |
| ------------------------------------------------------------ | -------------- | ------------------------------------- |
| Overriding method can't throw **broader checked exceptions** | ✅ Yes          | Ensures safe polymorphism             |
| Can throw **narrower or same** checked exceptions            | ✅ Yes          |                                       |
| Can throw **new unchecked exceptions**                       | ✅ Yes          |                                       |
| Overloading methods                                          | ❌ Not affected | Overloaded methods can throw anything |

#### **Note-2:** One more thing which IS NOT A restriction. 
Java allows you to override methods and add **any unchecked exception**, even if the superclass didn't throw anything at all.
![[Pasted image 20250504034456.png]]

#### Rules of Covariant Overriding

1. The return type must be a **subclass** of the overridden method's return type.
2. This feature only works for **object types** — **not primitives**.
3. It's supported from **Java 5 onwards**.
4. It works with **overriding**, not **overloading**.


### Based on the the above notes (1 and 2), why java cares hierarchy for checked but not for unchecked?
##### Java enforces the exception hierarchy for checked exceptions **to protect the caller**.
- When you override a method, the caller (which may not even know the actual subclass) only knows what **exceptions the superclass promised** to throw. So if a subclass suddenly throws **broader** or **new checked exceptions**, it would break the contract and **force callers to handle exceptions they weren’t expecting**.
- **Preserve safe polymorphism** and **caller expectations** at compile time.
##### Why Java **Does Not** Enforce Hierarchy for **Unchecked Exceptions**
- Give developers flexibility in dealing with **unexpected bugs or logic errors** without bloating code with unnecessary `throws` declarations
### Can you override a non-static method with a static method in Java, or vice versa?
TL;DR - No, in Java you **cannot override** a non-static method with a static one, or a static method with a non-static one. Both will give you compilation error.

> ***Code to an Interface, Not an Implementation***
