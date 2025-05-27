Topic: [[My Learning]], [[Design Patterns]]
### Strategy Pattern
#link https://www.youtube.com/watch?v=Nrwj3gZiuJU

***This is a behavioral design pattern***
- Basically this achieves the Single Responsibility Principle and Open-Closed Principle.
- The idea here is, if you have a lot of different algorithms or strategies and if you want to create a new strategy, then this pattern will help us in doing that without disturbing the existing code.
- If a Service class has a lot of responsibility (like lot of logics/algorithm), then we need to create separate classes for separate logic/algorithm/responsibility. And we call each of them (logic/algorithm/responsibility) as Concrete Strategies.
- Then in order to standardize these Concrete Strategies, we need to put the methods in a separate interface.
- Then these Concrete Strategies will be used dynamically in a Context or a Service class. Client has to pass which concreate strategy to use to the Context Class, then the Context Class will decide which Concreate Strategy to use using the Interface.
### Iterator Pattern

***This is a behavioral design pattern***
- If a class tries to accumulate data, then it should have a functionality to iterate that data.
- Instead of client writing the logic to iterate the data, the iterate pattern asks the aggregating class to has the data iteration logic.
- So, the aggregating class should return an object of a Iterator implemented class.
- Iterator implemented class should implement Iterator Interface (hasNext() and next())