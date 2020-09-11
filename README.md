## Javascript



## Javascript ES6 
1. Let and Const
2. Arrow functions
3. Default parameters
4. for of loop
5. Spread attributes
6. Maps
7. Sets
8. Static methods
9. Getters and Setters

#### 1. var
คือคำสั่งสำหรับประกาศตัวแปร
#### var hoisting
การประกาศตัวแปรโดยทั่วไปได้รับการประมวลผลก่อนที่ code คำสั่งจะถูกประมวลผล หมายความว่าตัวแปรสามารถใช้ก่อนที่จะประกาศ ลักษณะการทำงานนี้เรียกว่า "hoisting" เนื่องจากการประกาศตัวแปรจะถูกย้ายไปที่ด้านบนสุดของฟังก์ชัน

        bla = 2; // คำสั่ง
        var bla; // ประกาศตัวแปร

        // เข้าใจได้ดังนี้

        var bla;
        bla = 2;

#### 2. Let
เป็นการประกาศตัวแปรคล้ายๆกับ var แต่มีขอบเขตที่เข้าถึงเข้าถึงได้ในระดับ block { } ที่กำหนดไว้เท่านั้น

        if (true) {
            let a = 40;
            console.log(a); //40
        }
        console.log(a); // undefined
       
ในตัวอย่างต่อไป ตัวแปร "a" ถูกกำหนดไว้ใน block { } ของคำสั่ง If ดังนั้นจึงไม่สามารถเข้าถึงได้จากภายนอก block { } if

        let a = 50;
        let b = 100;
        if (true) {
            let a = 60;
            var c = 10;
            console.log(a/c); // 6
            console.log(b/c); // 10
        }
        console.log(c); // 10
        console.log(a); // 50

#### 3. Const

เป็นการประกาศตัวแปรมีขอบเขตที่เข้าถึงได้ในระดับ block { } คล้ายๆกับ let แต่<b>ไม่สามารถเปลี่ยนแปลงค่าผ่านการประกาศใหม่ได้</b>

#### 4. Arrow function

 ช่วยให้เราสามารถเขียนไวยากรณ์ฟังก์ชั่นที่สั้นลง
 
         // Traditional Function
        function (a, b){
             let chuck = 42;
             return a + b + chuck;
        }

        // Arrow Function
        (a, b) => {
             let chuck = 42;
             return a + b + chuck;
        }
 
 อีกเหตุผลประการหนึ่งที่มีการน Arrow function มาใช้ คือเพื่อหลีกเลี่ยงความซับซ้อนของขอบเขต (this) 
        
        window.age = 10;
        function Person() {
             this.age = 42;
             setTimeout(function () { //  Traditional function is executing on the window scope
                 console.log("this.age", this.age); // "10" because the function executes on the window scope
             }, 100);
        }

        var p = new Person();

Arrow function ไม่ได้ตั้งเริ่มต้น this เป็น window scope แต่จะดำเนินการในขอบเขตที่สร้างขึ้น

        window.age = 10; 
        function Person() {
             this.age = 42; 
             setTimeout(() => { // <-- Arrow function executing in the "p" (an instance of Person) scope
                 console.log("this.age", this.age); // "42" because the function executes on the Person scope
             }, 100);
        }

        var p = new Person();

#### 5. Default parameters

####  Pure function

มีคุณสมบัติดังต่อไปนี้

        function add(x, y) {
          return x + y;
        }


### Higher-order function
        
### Map Function

### Filter Function


### Refference

- https://hackernoon.com/es6-for-beginners-f98120b57414
- http://www.htmldog.com/guides/javascript/advanced/localstorage/
- https://www.earthchie.com/blog/js-bahttext-function/

