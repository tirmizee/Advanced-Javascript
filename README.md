# Advanced-Javascript
http://www.htmldog.com/guides/javascript/advanced/localstorage/
https://www.earthchie.com/blog/js-bahttext-function/


## ทบทวน

### Pure Function

มีคุณสมบัติดังต่อไปนี้

        function add(x, y) {
          return x + y;
        }


### Higher-order Function

### Arrow Function

Arrow Function ช่วยให้เราสามารถเขียนไวยากรณ์ฟังก์ชั่นที่สั้นลงและยังมีความสามารถเข้าถึง this จาก scope ที่ครอบมันอยู่ ซึ่งมีมาให้ใน ES6

-   Before

        hello = function() {
          return "Hello World!";
        }
    
-   Arrow Function

        hello = () => {
          return "Hello World!";
        }
        
### Map Function

### Filter Function



    // Arrays
    var cars = ["Saab", "Volvo", "BMW"];
    console.log('0 in cars : ' +  (0 in cars));
    console.log('1 in cars : ' +  (1 in cars));
    console.log('2 in cars : ' +  (2 in cars));
    console.log('3 in cars : ' +  (3 in cars));
    console.log('"Saab" in person : ' +  ('Saab' in cars));

    // Objects
    var person = {
        firstName:"John", 
        lastName:"Doe", 
        age:50
    };
    console.log('"firstName" in person : ' +  ('firstName' in person));
    console.log('"lastName" in person : '  +  ('lastName' in person));
    console.log('"age" in person : '       +  ('age' in person));
    console.log('0 in person : '           +  (0 in person));
    console.log('50 in person : '          +  (50 in person));
    console.log('"John" in person : '      +  ('John' in person));
    
Selectors

    $('.feature');           // Class selector
    $('li strong');          // Descendant selector
    $('em, i');              // Multiple selector
    $('a[target="_blank"]'); // Attribute selector
    $('p:nth-child(2)');     // Pseudo-class selector
    
    
Prevent click right

    $(document).ready(function() {
        $("body").on("contextmenu",function(){
           return false;
        }); 
    }); 

### Refference

- https://hackernoon.com/es6-for-beginners-f98120b57414
