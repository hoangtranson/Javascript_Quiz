# Quiz 2

1. What is this print?
    ```javascript
    console.log(x);
    var x = 100;
    ```

2. What is this print?
    ```javascript
    console.log(x);
    let x = 100;
    ```

3. What is this print?
    ```javascript
    var x = 100;

    function hoist() {
        if (false) {
            var x = 200;
        }
        console.log(x);
    }

    hoist();
    ```

4. What is this print?
    ```javascript
    var x = 100;

    function hoist() {
        if (false) {
            let x = 200;
        }
        console.log(x);
    }

    hoist();
    ```

5. What is this print?
    ```javascript
    var x = 1;
    var x = 2;

    console.log(x);
    ```

6. What is this print?
    ```javascript
    let x = 1;
    let x = 2;

    console.log(x);
    ```

7. What is this print?
    ```javascript
    const SPECIES = "human"
    SPECIES = "werewolf"

    console.log(SPECIES)
    ```

8. What is this print?
    ```javascript
    const TODO;
    console.log(TODO);
    ```

9. What is this print?
    ```javascript
    const CAR = {
        color: "blue",
        price: 15000
    }
    CAR.price = 20000;
    console.log(CAR);
    ```

10. What is this print?
    ```javascript
    var a = 1;
    function b() {
        a = 10;
        return;
        function a() {}
    }
    b();
    console.log(a);
    ```

11. What is this print?
    ```javascript
    var a = 1;
    function b() {
        a = 10;
        return;
    }
    b();
    console.log(a);
    ```

12. What is this print?
    ```javascript
    function foo(){
        function bar() {
            return 3;
        }
        return bar();
        function bar() {
            return 8;
        }
    }
    alert(foo());
    ```

13. What is this print?
    ```javascript
    function parent() {
        var hoisted = "I'm a variable";
        function hoisted() {
            return "I'm a function";
        }
        return hoisted();
    }
    console.log(parent());
    ```

14. What is this print?
    ```javascript
    alert(foo());
    function foo() {
        var bar = function() {
            return 3;
        };
        return bar();
        var bar = function() {
            return 8;
        };
    }
    ```

15. What is this print?
    ```javascript
    alert(foo());
    function foo() {
        function bar() {
            return 3;
        };
        return bar();
        function bar() {
            return 8;
        };
    }
    ```

16. What is this print?
    ```javascript
    var myVar = 'foo';
    (function() {
        console.log('Original value was: ' + myVar);
        var myVar = 'bar';
        console.log('New value is: ' + myVar);
    })();
    ```

17. What is this print?
    ```javascript
    function getShape(condition) {
        console.log(shape);
        if (condition) {
            var shape = "square";
            return shape;
        } else {
            return false;
        }
    }
    getShape(false)
    getShape(true)
    ```

18. What is this print?
    ```javascript
    function getShape(condition) {
        console.log(shape);
        if (condition) {
            let shape = "square";
            return shape;
        } else {
            return false;
        }
    }
    getShape(false)
    getShape(true)
    ```

19. What is this print?
    ```javascript
    var shape = "square";
    let shape = "rectangle";
    ```

20. What is this print?
    ```javascript
    var shape = "square";
    if (true) {
        let shape = "rectangle";
    }
    ```

21. What is this print?
    ```javascript
    const color;
    ```
    Note: As a general rule, use `let` only for loop counters or only if you really need reassignment. Everywhere else, use `const`. Personally I’ve ditched loops for filter(), map() & reduce().

22. What is this print?
    ```javascript
    var outerFunction  = function(){
        if(true){
            var x = 5;
        }
        var nestedFunction = function() {
            if(true){
                var y = 7;
                console.log(x);
            }

            if(true){
                console.log(y);
            }
        }
        return nestedFunction;
    }

    var myFunction = outerFunction();
    myFunction();
    ```

23. What is this print?
    ```javascript
    var cat = {
        name: "Gus",
        color: "gray",
        age: 15,
        printInfo: function() {
            console.log("Name:", this.name, "Color:", this.color, "Age:", this.age);
            nestedFunction = function() {
                console.log("Name:", this.name, "Color:", this.color, "Age:", this.age);
            }
        nestedFunction();
        }
    }
    cat.printInfo();
    ```

    Note: A `closure` is a special kind of object that combines two things: a function, and the environment in which that function was created. The environment consists of any local variables that were in-scope at the time that the closure was created.

24. What is this print?
    ```javascript
    var cat = {
        name: "Gus",
        color: "gray",
        age: 15,
        printInfo: function() {
            console.log("Name:", this.name, "Color:", this.color, "Age:", this.age);
            nestedFunction = () => {
                console.log("Name:", this.name, "Color:", this.color, "Age:", this.age);
            }
        nestedFunction();
        }
    }
    cat.printInfo();
    ```

25. What is this print?
    ```javascript
    var cat = {
        name: "Gus",
        color: "gray",
        age: 15,
        printInfo: function() {
            console.log("Name:", this.name, "Color:", this.color, "Age:", this.age);
            nestedFunction = function() {
                console.log("Name:", this.name, "Color:", this.color, "Age:", this.age);
            }
            nestedFunction.call(this);
            nestedFunction.apply(this);
            var storeFunction = nestedFunction.bind(this);
                storeFunction();
            }
        }
    cat.printInfo();
    ```

    Note:
    `Closures` are best used when you have nested functions similar to the first cat example above, which used var that = this. This method is also nice because you don’t have to worry about cross-platform issues. For instance, bind() is a recent addition to ECMAScript5 and isn’t always supported.
    `Call() and apply()` are useful for when you want to borrow a method from one object and use it in a completely separate object. For example, using our cat example above, we could reuse its  printInfo() function to print information about a dog.
    `Bind()` is useful for maintaining context in asynchronous callbacks and events.

26. What is this print?
    ```javascript
    function init() {
        var name = 'Mozilla'; // name is a local variable created by init

        function displayName() { 
            // displayName() is the inner function, a closure

            alert(name);
        }
        displayName();
    }
    init();
    ```

27. What is this print?
    ```javascript
    function makeFunc() {
        var name = 'Mozilla';
        function displayName() {
            alert(name);
        }
        return displayName;
    }

    var myFunc = makeFunc();
    myFunc();
    ```

28. What is this print?
    ```javascript
    function makeAdder(x) {
        return function(y) {
            return x + y;
        };
    }

    var add5 = makeAdder(5);
    var add10 = makeAdder(10);

    console.log(add5(2));
    console.log(add10(2));
    ```
29. What is this print?
    ```javascript
    var counter = (function() {
        var privateCounter = 0;
        function changeBy(val) {
            privateCounter += val;
        }
        return {
            increment: function() {
            changeBy(1);
            },
            decrement: function() {
            changeBy(-1);
            },
            value: function() {
            return privateCounter;
            }
        };
    })();

    console.log(counter.value());
    counter.increment();
    counter.increment();
    console.log(counter.value());
    counter.decrement();
    console.log(counter.value());
    ```

30. What is the difference between `undefined` and `not defined` in JavaScript?

    Consider this follow code?

    ```javascript
    let x;
    console.log(x)
    console.log(y)
    ```

31. What is this print?

    ```javascript
    var y = 1;
    if (function f(){}) {
        y += typeof f;
    }
    console.log(y);
    ```

32. What is this print?
    ```javascript
    var k = 1;
    if (1) {
        eval(function foo(){});
        k += typeof foo;
    }
    console.log(k);
    ```

33. What is this print?
    ```javascript
    var k = 1;
    if (1) {
        function foo(){};
        k += typeof foo;
    }
    console.log(k);
    ```

34. What is this print?
    ```javascript
    (function(){
        var a = b = 3;
    })();

    console.log("a defined? " + (typeof a !== 'undefined'));
    console.log("b defined? " + (typeof b !== 'undefined'));
    ```
35. What is this print?
    ```javascript
    var myObject = {
        foo: "bar",
        func: function() {
            var self = this;
            console.log("outer func:  this.foo = " + this.foo);
            console.log("outer func:  self.foo = " + self.foo);
            (function() {
                console.log("inner func:  this.foo = " + this.foo);
                console.log("inner func:  self.foo = " + self.foo);
            }());
        }
    };
    myObject.func();
    ```

36. Consider the two functions below. Will they both return the same thing? Why or why not?
    ```javascript
    function foo1(){
        return {
            bar: "hello"
        };
    }

    function foo2(){
        return
        {
            bar: "hello"
        };
    }
    ```

37. What is this print?
    ```javascript
    console.log(typeof NaN === "number");
    console.log(NaN === NaN);
    ```

38. What will the code below output?
    ```javascript
    console.log(0.1 + 0.2);
    console.log(0.1 + 0.2 == 0.3);
    ```

    Note: A typical solution is to compare the absolute difference between two numbers with the special constant `Number.EPSILON`

    ```javascript
    function areTheNumbersAlmostEqual(num1, num2) {
        return Math.abs( num1 - num2 ) < Number.EPSILON;
    }
    console.log(areTheNumbersAlmostEqual(0.1 + 0.2, 0.3));
    ```
39. In what order will the numbers 1-4 be logged to the console when the code below is executed?
    ```javascript
    (function() {
        console.log(1);
        setTimeout(function(){console.log(2)}, 1000);
        setTimeout(function(){console.log(3)}, 0);
        console.log(4);
    })();
    ```

    Ref: http://javascript.info/settimeout-setinterval

40. What will the code below output to the console?
    ```javascript
    console.log(1 +  "2" + "2");
    console.log(1 +  +"2" + "2");
    console.log(1 +  -"1" + "2");
    console.log(+"1" +  "1" + "2");
    console.log( "A" - "B" + "2");
    console.log( "A" - "B" + 2);
    ```