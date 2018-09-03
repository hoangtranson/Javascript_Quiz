# Quiz 3

1. What is this print?
    ```javascript
    for (var i = 0; i < 5; i++) {
        setTimeout(function() { console.log(i); }, i * 1000 );
    }
    ```

2. What is this print?
    ```javascript
    for (var i = 0; i < 5; i++) {
        (function(x) {
            setTimeout(function() { console.log(x); }, x * 1000 );
        })(i);
    }
    ```

3. What is this print?
    ```javascript
    console.log("0 || 1 = "+(0 || 1));
    console.log("1 || 2 = "+(1 || 2));
    console.log("0 && 1 = "+(0 && 1));
    console.log("1 && 2 = "+(1 && 2));
    ```

4. What is this print?
    ```javascript
    console.log(false == '0')
    console.log(false === '0')
    ```

5. What is the output out of the following code?

    ```javascript
    var a={},
        b={key:'b'},
        c={key:'c'};

    a[b]=123;
    a[c]=456;

    console.log(a[b]);
    ```

6. What is the output out of the following code?
    ```javascript
    console.log((function f(n){return ((n > 1) ? n * f(n-1) : n)})(10));
    ```

7. What is this print?
    ```javascript
    (function(x) {
        return (function(y) {
            console.log(x);
        })(2)
    })(1);
    ```

8. What is this print?
    ```javascript
    var hero = {
        _name: 'John Doe',
        getSecretIdentity: function (){
            return this._name;
        }
    };

    var stoleSecretIdentity = hero.getSecretIdentity;

    console.log(stoleSecretIdentity());
    console.log(hero.getSecretIdentity());
    ```

9. What is this print?
    ```javascript
    var length = 10;
    function fn() {
        console.log(this.length);
    }

    var obj = {
        length: 5,
        method: function(fn) {
            fn();
            arguments[0]();
        }
    };

    obj.method(fn, 1);
    ```

10. What is this print?
    ```javascript
    (function () {
        try {
            throw new Error();
        } catch (x) {
            var x = 1, y = 2;
            console.log(x);
        }
        console.log(x);
        console.log(y);
    })();
    ```

11. What is this print?
    ```javascript
    var x = 21;
    var girl = function () {
        console.log(x);
        var x = 20;
    };
    girl ();
    ```

12. What is this print?
    ```javascript
    for (let i = 0; i < 5; i++) {
        setTimeout(function() { console.log(i); }, i * 1000 );
    }
    ```

13. What is this print?
    ```javascript
    const a = [1, 2, 3];
    a[10] = 99;
    console.log(a[6]);
    ```

14. What is this print?
    ```javascript
    typeof undefined == typeof NULL
    ```

15. What is this print?
    ```javascript
    console.log(typeof typeof 1);
    ```

16. What is this print?
    ```javascript
    var b = 1;
    function outer(){
        var b = 2
        function inner(){
            b++;
            var b = 3;
            console.log(b)
        }
        inner();
    }
    outer();
    ```

17. What is this print?
    ```javascript
    var output = (function(x){
        delete x;
        return x;
    })(0);

    console.log(output);
    ```

18. What is this print?
    ```javascript
    var x = { foo : 1};
    var output = (function(){
        delete x.foo;
        return x.foo;
    })();

    console.log(output);
    ```

19. What is this print?
    ```javascript
    const bar = true;
    console.log(bar + 0);
    console.log(bar + "xyz");  
    console.log(bar + true);  
    console.log(bar + false);
    ```

    Note:
    + Number + Number -> Addition
    + Boolean + Number -> Addition
    + Boolean + Number -> Addition
    + Number + String -> Concatenation
    + String + Boolean -> Concatenation
    + String + String -> Concatenation

20. What is this print?
    ```javascript
    var z = 1, y = z = typeof y;
    console.log(y);
    ```

21. What is this print?
    ```javascript
    const foo = function bar(){ return 12; };
    typeof bar();
    ```

22. What is this print?
    ```javascript
    var salary = "1000$";

    (function () {
        console.log("Original salary was " + salary);

        var salary = "5000$";

        console.log("My New Salary " + salary);
    })();
    ```

23. What is this print?
    ```javascript
    function foo(){
        return foo;
    }
    new foo() instanceof foo;
    ```

24. What is this print?
    ```javascript
    ```

25. What is this print?
    ```javascript
    ```

26. What is this print?
    ```javascript
    ```

27. What is this print?
    ```javascript
    ```

28. What is this print?
    ```javascript
    ```

29. What is this print?
    ```javascript
    ```

30. What is this print?
    ```javascript
    ```

31. What is this print?
    ```javascript
    ```

32. What is this print?
    ```javascript
    ```

33. What is this print?
    ```javascript
    ```

34. What is this print?
    ```javascript
    ```

35. What is this print?
    ```javascript
    ```

36. What is this print?
    ```javascript
    ```

37. What is this print?
    ```javascript
    ```

38. What is this print?
    ```javascript
    ```

39. What is this print?
    ```javascript
    ```

40. What is this print?
    ```javascript
    ```
