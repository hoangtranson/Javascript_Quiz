# Quiz 1

1. What is this print?
    ```javascript
    3 + true = ?
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
    x === NaN ???
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

25. What is the result of this script `typeof test()[2]`?

    ```javascript
    const test = () => [
        () => 1,
        () => 2,
        () => 3
    ];
    typeof test()[2]
    ```

26. What is the result of this script `getFirst(test())()`?

    ```javascript
    const test = () => [
        () => 1,
        () => 2,
        () => 3
    ];

    const getFirst = arr => arr[0]
    getFirst(test())()
    ```