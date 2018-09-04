# Quiz 1

1. What is this print?
    ```javascript
    3 + true
    ```

2. What is the result of this script ?
    ```javascript
    "hello"(1)
    ```

3. What is the result of this script ?
    ```javascript
    (2 + 2 === 4) === (2 !== 5)
    ```

4. What is the result of this script ?
    ```javascript
    [2-1, 2, 2+1] === [1,2,3]  
    ```

5. What is this print?

    ```javascript
    1 + 2 + "3"
    ```

6. What is the result of the script `x === NaN` ?

    ```javascript
    let x = NaN
    x === NaN
    ```

7. What is this print?

    ```javascript
    () => "2"
    ```

8. What is this print ?

    ```javascript
    (() => (() => 0)())()
    ```

9. What is this print ?

    ```javascript
    (() =>
        (() => 0
        )()
    )()
    ```

10. What is this print ?

    ```javascript
    (() => (1 + 1, 2 + 2))()
    ```

11. What is this print ?

    ```javascript
    (() => {})()
    ```

12. What is the result of this script ?

    ```javascript
    (() => {})() === (() => {})()
    ```

13. What is the result of this script ?

    ```javascript
    (() => {})() === undefined
    ```

14. What is this print ?

    ```javascript
    void (2 + 2)
    ```

15. What is the result of this script ?

    ```javascript
    (() => 2 + 2)()
    ```

16. What is the result of this script ?

    ```javascript
    (() => {
        1 + 1;
        return 2 + 2
    })()
    ```

17. What is the result of this script `a === b`?

    ```javascript
    let a = (() => () => true)()()
    let b = () => () => { return true; }
    a === b
    ```

18. What is the result of this script ?

    ```javascript
    const calculate = (diameter) => diameter * 3.14159265
    calculate(1) === ((diameter) => diameter * 3.14159265)(2) // result ?
    ```

19. What is the result of this script `typeof test`?

    ```javascript
    const test = () => [
        () => 1,
        () => 2,
        () => 3
    ];
    typeof test
    ```

20. What is this print ?

    ```javascript
    ((x) => (y) => x)(1)(2)
    ```

21. What did this function do ?

    ```javascript
    (x) =>
        (y) =>
            (z) => x + y + z
    ```

22. What is the result ?

    ```javascript
    const PI = 3;
    ((PI) =>
        console.log(PI)
    )(3.14159265)
    ```

23. What is the result of this script `test().length`?

    ```javascript
    const test = () => [
        () => 1,
        () => 2,
        () => 3
    ];
    test().length
    ```

24. What is the result ?

    ```javascript
    const isEven = n => {
        const even = (x) => {
            if (x === 0)
                return true;
            else
                return !even(x - 1);
        }
        return even(n)
    }

    isEven(NaN)
    isEven(0.2)
    isEven(-1)
    isEven(10)
    ```

25. What is different between this two functions ? Which one will work ? Why?

    ```javascript
    (function () {
        return fizzbuzz();
        const fizzbuzz = function fizzbuzz () {
            return "Fizz" + "Buzz";
        }
    })()

    (function () {
        return fizzbuzz();
        function fizzbuzz () {
            return "Fizz" + "Buzz";
        }
    })()

    (function () {
        const fizzbuzz = function fizzbuzz () {
            return "Fizz" + "Buzz";
        }
        return fizzbuzz();
    })()
    ```

26. What is this print ?

    ```javascript
    const repeat = (num, fn) =>
        (num > 0)
        ? (repeat(num - 1, fn), fn(num))
        : undefined

    repeat(3, function (n) {
        console.log(`Hello ${n}`)
    })
    ```

27. What is the result of this script `typeof test()[2]`?

    ```javascript
    const test = () => [
        () => 1,
        () => 2,
        () => 3
    ];
    typeof test()[2]
    ```

28. What do `compose` function do? What is this script `cookAndEat('meat')` result?

    ```javascript
    const compose = (a, b) => (c) => a(b(c));
    const cook = food => {
        console.log('cook ' + food)
        return food;
    }
    const eat = food => {
        console.log('eat ' + food)
        return 'done';
    }
    const cookAndEat = compose(eat, cook);
    cookAndEat('meat')
    ```

    Note: JavaScript functions take values as arguments and return values. JavaScript functions are values, so JavaScript functions can take functions as arguments, return functions, or both. Generally speaking, a function that either takes functions as arguments, or returns a function, or both, is referred to as a `higher-order` function.

    A `combinator` is a higher-order function that uses only function application and earlier defined combinators to define a result from its arguments.

29. What is this print ?

    ```javascript
    const args = function (a, b) {
        return arguments;
    }
    args(2,3)
    ```
30. What are `plus(2)` and `plus(2,3)` print ?

    ```javascript
    const plus = function () {
        return arguments[0] + arguments[1];
    }
    plus(2)
    plus(2,3)
    ```

31. What is this print ?

    ```javascript
    const howMany = function () {
        return arguments['length'];
    }
    howMany('sharks', 'are', 'apex', 'predators')
    ```

32. What is the result of this script `getFirst(test())()`?

    ```javascript
    const test = () => [
        () => 1,
        () => 2,
        () => 3
    ];

    const getFirst = arr => arr[0]
    getFirst(test())()
    ```

33. What is this print ?

    ```javascript
    (function () {
        return (function () { return arguments[0]; })('inner');
    })('outer')
    ```

34. What is this print ?

    ```javascript
    (function () {
        return (() => arguments[0])('inner');
    })('outer')
    ```

35. What is `row1(3)` and `row2(3)` print ?

    ```javascript
    const row1 = function () {
        return [1, 2, 3, 4, 5, 6, 7, 8, 9, 10].map( item => {
            return item * arguments[0]
        })
    }

    const myMap = function (column) { return column * arguments[0] }
    const row2 = function () {
        return [1, 2, 3, 4, 5, 6, 7, 8, 9, 10].map(myMap)
    }

    row1(3)
    row2(3)
    ```

36. What is this print ?

    ```javascript
    ((diameter_fn) => {
        const PI = 3;
        return diameter_fn(2)
    })(
        (() => {
            const PI = 3.14159265;
            return (diameter) => diameter * PI
        })()
    )
    ```

37. What is this print ?

    ```javascript
    0.1 + 0.1 + 0.1 === 0.3
    ```

38. What is this print ?

    ```javascript
    (0.1 + 0.2) + 0.3 === 0.1 + (0.2 + 0.3)
    ```

39. What is this print ?

    ```javascript
    2 * {valueOf: function(){ return 3}}
    ```

40. What is this print ?

    ```javascript
    const a = new String('hello')
    const b = new String('hello')
    const c = 'hello'

    a == b
    a === c
    a == c
    a === c
    ```

## Summary

+ Functions are values that can be part of expressions, returned from other functions,and so forth.

+ Functions are reference values.

+ Functions are applied to arguments.

+ The arguments are passed by sharing, which is also called “pass by value.”

+ Fat arrow functions have expressions or blocks as their bodies.

+ function keyword functions always have blocks as their bodies.

+ Function bodies have zero or more statements.

+ Expression bodies evaluate to the value of the expression.

+ Block bodies evaluate to whatever is returned with the return keyword, or to undefined.

+ JavaScript uses const to bind values to names within block scope.

+ JavaScript uses function declarations to bind functions to names within function scope. Function declarations are “hoisted.”

+ Function application creates a scope.

+ Blocks also create scopes if const statements are within them.

+ Scopes are nested and free variable references closed over.

+ Variables can shadow variables in an enclosing scope.
