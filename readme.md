<div align="center">
  <img src="assetes/img/htmlCssJavaScript.png">
  <h1>Workshop Create form sign in and sign up</h1>
</div>

### สิ่งที่ได้เรียนรู้

1. [การออกแบบ Form ด้วย Figma](https://www.figma.com/file/0CAGx5FQRWAcgpTzrCmkKb/Login-Form)
2. [html](#html)
3. [css](#css)
4. [javaScript](#javaSCript)

### ภาพของโปรเจคนี้

![Form](assetes/img/Form.png)

### html

1. การสร้างฟอร์ม
   - placeholder คือ ให้ข้อความที่เราต้องการไปอยู่ในช่อง Form
   - type of input
     - text //สิ่งที่เราต้องการให้รับค่าเข้ามา
     - password //สิ่งที่เราต้องการให้รับค่าเข้ามา
     - email //สิ่งที่เราต้องการให้รับค่าเข้ามา

ซึ่งจากการลงมือทำในครั้งนี้จะเห็นว่า การวางโครงสร้างของ html เป็นเรื่องที่สำคัญเป็นอย่างมาก ถ้าหากเราวางโครงสร้างไม่ถูกต้อง เวลาที่เรา แสดงผลจะทำให้ โปรแกรมแสดงผลผิดพลาด และทำให้เกิด Error ได้นั้นเอง

### Example code 1

```html
<div class="container">
  <!-- เราจะเริ่มเขียนโปรแกรมที่ตรงนี้ -->
</div>
```

### Example code 2

```html
<div class="container">
  <div class="form-container">
    <!-- Form signin -->
    <div class="signin">
      <form action="#" class="form-sign-in">
        <h1>Sign In</h1>
        <input type="text" placeholder="Username" />
        <input type="password" placeholder="Password" />
        <a href="#">Forgot your password?</a>
        <button class="btn btn-form">SIGN IN</button>
      </form>
    </div>

    <!-- Form signup -->
    <div class="signup">
      <form action="#" class="form-sign-up">
        <h1>SIGN UP</h1>
        <input type="text" placeholder="Username" />
        <input type="email" placeholder="email" />
        <input type="password" placeholder="password" />
        <button class="btn btn-form">SIGN UP</button>
      </form>
    </div>
  </div>
</div>
```

Tip : ค่อยๆ เรียนรู้ อย่ารีบร้อน จงจำคำนี้ไว้ อย่าไปสนใจว่าเราทำได้เยอะขนาดไหน แต่จงใส่ใจว่า เราได้เรียนรู้จากสิ่งนั้นมากขนาดไหน และสามารถนำไปประยุกต์ใช้ได้ต่อไป

### css

ได้เรียนรู้การจัดตำแหน่งของ CSS ด้วย Flexbox ซึ่ง Flexbox จะเปรียบเหมือนกล่องๆ หนึ่งนั้นเอง จะทำให้การจัดตำแหน่งมีความง่ายมากขึ้นกว่าเดิมนั้นเอง

#### ยกตัวอย่างคำสั่งของ flexbox

ก่อนอื่นเราจะต้องตั้งค่า css ให้เป็น flexbox ก่อนด้วยคำสั่ง `display: flex;` เสียก่อน จากนั้นเราก็สามารถคำสั่งเหล่านี้ในการจัดตำแหน่งได้เลย  
`justify-content` แล้วตามด้วยคำสั่งต่อไปนี้ (ซึ่งจะเป็นการจัดตำแหน่งแกลน X เท่านั้น )

- flext-start //วัตถุจะอยู่ที่ตำแหน่งซ้ายสุดของหน้าจอ
- flext-end //วัตถุจะอยู่ที่ตำแหน่งขวาสุดของหน้าจอ
- center //วัตถุจะอยู่ตรงกลางหน้าจอ
- space-between //สมมุติถ้ามีวัตถุจำนวน 3 ชิ้น จะถูกจัดตำแหน่งดังนี้ ชิ้นที่ 1 อยู่ทางซ้ายสุด ชิ้นที่ 2 อยู่ตรงกลาง ชิ้นที่ 3 อยู่ขวาสุด
- space-around //สมมุติถ้ามีวัตถุจำนวน 3 ชิ้น จะถูกจัดตำแหน่งดังนี้ ชิ้นที่ 1 อยู่ทางซ้ายสุด ชิ้นที่ 2 อยู่ตรงกลาง ชิ้นที่ 3 อยู่ขวาสุด แต่จะเว้นระยะห่างเท่ากัน
- initial //วัตถุจะอยู่ที่ตำแหน่งซ้ายสุดของหน้าจอ

[สำหรับการอ่านเรื่อง Flexbox เพิ่มเติม](https://www.w3schools.com/cssref/playit.asp?filename=playcss_justify-content&preval=initial])

[อ่านเพิ่มเติมเรื่อง Box-sizing](https://medium.com/hbot/box-sizing-%E0%B8%AA%E0%B8%B4%E0%B9%88%E0%B8%87%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%AB%E0%B8%A5%E0%B8%B2%E0%B8%A2%E0%B8%84%E0%B8%99%E0%B8%AD%E0%B8%B2%E0%B8%88%E0%B9%84%E0%B8%A1%E0%B9%88%E0%B8%A3%E0%B8%B9%E0%B9%89-f13e1cad6e06)

```css
/* Link font form google fonts */
@import url("https://fonts.googleapis.com/css?family=Kanit&display=swap");

/* ทำการกำหนดค่าของหน้า html */
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  font-family: "Kanit", sans-serif; /* กำหนด Font ให้ตรงตามที่เราเลือกมาจาก google font */
  display: flex; /* กำหนดตำแหน่งของวัตถุุให้เป็นแนวนอนด้วยคำสั่ง Flex (แต่ก่อนตำแหน่งของวัตถุ จะเป็น Block) */
  align-items: center; /* ใช้คำสั่ง align-items : center; เพื่อให้วัตถุอยู่ตรงกลาง */
  justify-content: center; /* จัดตำแหน่งให้มาอยู่ตรงกลางแบบ Auto  */
  min-height: 100vh;
  background: #f6f5f7;
}

/* container */
.container {
  position: relative;
  padding: 40px 20px; /* first are top and bottom second are right and left */
  background: white;
  border-radius: 10px;
  width: 700px;
  min-height: 400px;
  box-shadow: 5px 5px 20px 5px rgba(214, 214, 214, 1);
  overflow: hidden; /* อะไรก็ตามที่เกินขอบวัตถุนี้ ให้ซ้อนไว้ */
}

/* form-container */
.form-container {
  height: 100%;
  width: 50%;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  right: 0;
}

.form-container input {
  display: block;
  padding: 12px 20px;
  margin: 7px 13px;
  background: #f6f5f7;
  border: none;
  outline: none;
}

.form-sign-in,
.form-sign-up {
  position: absolute;
  height: 100%;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.signin {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  transition: 0.8s;
}

.signup {
  position: absolute;
  width: 100%;
  height: 100%;
  bottom: -100%;
  transition: 0.8s;
}

.signup.show {
  bottom: 0;
}
.signin.hide {
  top: -100%;
}

.form-container h1 {
  text-align: center;
  font-size: 25px;
  text-transform: uppercase;
  margin: 10px;
}

.form-container a {
  margin: 10px;
  text-align: center;
  font-size: 10px;
  text-transform: uppercase;
  color: gray;
  text-decoration: none;
}

/* Button */
.btn {
  padding: 10px;
  min-width: 100px;
  border-radius: 20px;
  color: white;
  margin: 20px;
  outline: none;
  cursor: pointer;
  background: linear-gradient(
    rgb(255, 151, 207),
    rgb(255, 68, 146)
  ); /* linear-gradient จะมีการไล่เฉดสี */
}

.btn-form {
  border: none;
}

/* overlay */
.overlay {
  position: absolute;
  height: 100%;
  width: 50%;
  background: linear-gradient(rgb(255, 151, 207), rgb(255, 68, 146));
  top: 50%;
  transform: translateY(-50%);
  left: 0;
}

.overlay h1 {
  text-align: center;
  font-size: 25px;
  text-transform: uppercase;
  color: white;
}

.overlay span {
  color: white;
  text-align: center;
  font-size: 12px;
  padding: 10px;
}

.overlay-panel {
  position: absolute;
  height: 100%;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  padding: 30px;
}

.btn-overlay {
  border: 1px solid white;
}

/* เป็นการจัดตำแหน่งของวัตถุที่ทับซ้อนกัน */
.overlay-signup {
  top: 0;
  transition: 0.8s;
}
.overlay-signin {
  bottom: -100%;
  transition: 0.8s;
}

.overlay-signin.show {
  bottom: 0;
}
.overlay-signup.hide {
  top: -100%;
}
```

### javaScript

```js
function togglePage() {
  document.querySelector(".overlay-signin").classList.toggle("show");
  document.querySelector(".overlay-signup").classList.toggle("hide");
  document.querySelector(".signup").classList.toggle("show");
  document.querySelector(".signin").classList.toggle("hide");
}
```

สำหรับภาษา javaScript นั้นก็เหมือนการที่เรามีเว็บไซต์ปกติอยู่แล้ว เพียงแต่ว่าตอนนี้เราต้องการให้เว็บไซต์ของเรานั้น สามารถที่จะมีการตอบโต้ได้ เช่น ถ้าหากกดปุ่มนี้เราต้องการให้เกิดอะไรขึ้น หรือว่าถ้าหากกดอีกครั้งเราต้องการให้เกิดอะไรข้น ด้วยการเขียน javaScript นั้นเอง

```js
document.querySelector("class or id of css "); //เป็นการบอกว่า เราต้องการเข้าถึง selector ตัวไหนภายใน css
.classList.toggle("show"); //เราต้องการให้มันเกิดอะไรขึ้นนั้นเอง
```
