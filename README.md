## Javascript

- #### var
คือคำสั่งสำหรับประกาศตัวแปร

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

#### 1. Let
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

#### 2. Const

เป็นการประกาศตัวแปรมีขอบเขตที่เข้าถึงได้ในระดับ block { } คล้ายๆกับ let แต่<b>ไม่สามารถเปลี่ยนแปลงค่าผ่านการประกาศใหม่ได้</b>

#### 3. Arrow Function

 ช่วยให้เราสามารถเขียนไวยากรณ์ฟังก์ชั่นที่สั้นลงและยังมีความสามารถเข้าถึง this จาก scope ที่ครอบมันอยู่

## ทบทวน

### Pure Function

มีคุณสมบัติดังต่อไปนี้

        function add(x, y) {
          return x + y;
        }


### Higher-order Function
        
### Map Function

### Filter Function


### Refference

- https://hackernoon.com/es6-for-beginners-f98120b57414
- http://www.htmldog.com/guides/javascript/advanced/localstorage/
- https://www.earthchie.com/blog/js-bahttext-function/

