---
theme: apple-basic
background: https://go.dev/images/gophers/motorcycle.svg
title: เริ่มต้นเขียนโปรแกรมด้วย Go
info: |
  พร้อมยังกับการมาเรียนปูพื้นฐาน Golang จ้ะ
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
---

# พร้อมยังกับการมาเรียนปูพื้นฐาน Golang จ้ะ!

<div class="flex justify-center">
  <img class="w-20" src="https://go.dev/images/gophers/ladder.svg" />
</div>

<h1 class="text-xl mt-10 text-blue">"Hello World"</h1>

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  กดปุ่ม Space เพื่อไปหน้าถัดไป <carbon:arrow-right />
</div>

---

## layout: two-cols

<template v-slot:default>

<div class="content-section">
  <h2>สารบัญเนื้อหา 📚</h2>

  <h4>ส่วนที่ 1: พื้นฐานการเขียนโปรแกรม 💻</h4>
  <ul>
    <li><h3>1. ทำความรู้จักกับการเขียนโปรแกรมและภาษา Go 🚀</h3></li>
    <li><h3>2. การติดตั้งและเตรียมสภาพแวดล้อมการทำงาน 🛠️</h3></li>
    <li><h3>3. ตัวแปรและชนิดข้อมูลพื้นฐาน 🔄</h3></li>
    <li><h3>4. การคำนวณและตัวดำเนินการ 🧮</h3></li>
    <li><h3>5. การแสดงผลข้อความ (Output) 🖥️</h3></li>
    <li><h3>6. การรับข้อมูลจากผู้ใช้ (Input) 🖥️</h3></li>
    <li><h3>7. การตัดสินใจด้วย if-else 🤔</h3></li>
    <li><h3>8. การทำซ้ำด้วย for loop 🔁</h3></li>
    <li><h3>9. ฟังก์ชันพื้นฐาน 🚀</h3></li>
    <li><h3>10. การจัดการข้อผิดพลาด 🚨</h3></li>
    <li><h3>11. โครงสร้างข้อมูลพื้นฐาน 🚧</h3></li>
  </ul>
</div>

</template>
<template v-slot:right>

<div class="project-section">
  <h2>Mini Projects 🚀</h2>

  <h4>ส่วนที่ 2: โปรเจคตัวอย่าง 🎉</h4>
  <ul>
    <li>
      เกมทายตัวเลข 🎮
      <ul>
        <li><h3>การสุ่มตัวเลข 🔄</h3></li>
        <li><h3>การรับค่าจากผู้ใช้ 🖥️</h3></li>
        <li><h3>การใช้ loop และ if 🔁</h3></li>
        <li><h3>การแสดงผลลัพธ์ 🖥️</h3></li>
      </ul>
    </li>
    <li>
      โปรแกรมคำนวณเกรด 📚
      <ul>
        <li><h3>การรับคะแนนหลายวิชา 🖥️</h3></li>
        <li><h3>การคำนวณเกรดเฉลี่ย 🧮</h3></li>
        <li><h3>การแสดงผลในรูปแบบตาราง 🚧</h3></li>
      </ul>
    </li>
    <li>
      โปรแกรมบันทึกรายรับ-รายจ่าย 📈
      <ul>
        <li><h3>การใช้ struct และ slice 🚧</h3></li>
        <li><h3>การบันทึกและแสดงข้อมูล 🚧</h3></li>
        <li><h3>การคำนวณยอดคงเหลือ 🧮</h3></li>
      </ul>
    </li>
  </ul>
</div>

</template>

---

# 1. ทำความรู้จักกับการเขียนโปรแกรมและภาษา Go 🚀

<v-clicks>

<h2>การเขียนโปรแกรมคืออะไร? 🤔</h2>
<ul>
  <li><h3>การเขียนโปรแกรมคือการสร้างชุดคำสั่งที่บอกให้คอมพิวเตอร์ทำงานตามที่เราต้องการ 💻</h3></li>
  <li><h3>ต้องใช้ภาษาที่คอมพิวเตอร์เข้าใจ เรียกว่า "ภาษาโปรแกรมมิ่ง" (Programming Language) 📚</h3></li>
  <li><h3>การเขียนโปรแกรมเหมือนการสื่อสารกับเครื่องคอมพิวเตอร์ด้วยภาษาที่มีรูปแบบเฉพาะ 💬</h3></li>
</ul>

<h2>ทำไมต้องเป็นภาษา Go? 🤔</h2>

<ul>
  <li><h3>Go (หรือ Golang) เป็นภาษาที่พัฒนาโดย Google ในปี 2009 🚀</h3></li>
  <li><h3>จุดเด่นของภาษา Go:</h3>
    <ul>
      <li><h3>ไวยากรณ์เรียบง่าย เหมาะกับผู้เริ่มต้น 🌱</h3></li>
      <li><h3>มีความเร็วในการทำงานสูง ⚡️</h3></li>
      <li><h3>รองรับการทำงานแบบขนาน (Concurrency) ได้ดี 🔄</h3></li>
      <li><h3>มีไลบรารีมาตรฐานที่ครบครัน 🛠️</h3></li>
      <li><h3>คอมไพล์เป็นไฟล์ที่ทำงานได้เลย (ไม่ต้องติดตั้งโปรแกรมเพิ่ม) 💻</h3></li>
      <li><h3>ใช้ได้กับหลายระบบปฏิบัติการ (Windows, macOS, Linux) 🌐</h3></li>
    </ul>
  </li>
</ul>

</v-clicks>

---

<h2>2. การติดตั้งและเตรียมสภาพแวดล้อม</h2>
<v-clicks>
  <h4>2.1 การติดตั้ง Go</h4>
  <ol>
    <li><h3>ไปที่เว็บไซต์ <a href="https://golang.org/dl">golang.org/dl</a></h3></li>
    <li><h3>ดาวน์โหลดตัวติดตั้งตามระบบปฏิบัติการที่ใช้ (Windows, macOS, Linux)</h3></li>
    <li><h3>ติดตั้งตามขั้นตอนที่แนะนำ</h3></li>
  </ol>
  <h4>2.2 ตรวจสอบการติดตั้ง</h4>
  <p>เปิดโปรแกรม Command Prompt หรือ Terminal แล้วพิมพ์:</p>
```bash
go version
```

ควรจะแสดงเวอร์ชันของ Go ที่คุณติดตั้ง เช่น `go version go1.18.1 windows/amd64`

<h4>2.3 โปรแกรมแก้ไขโค้ด (Code Editor)</h4>
<ol>
    <li><h3>- Visual Studio Code + ส่วนขยาย Go</h3></li>
    <li><h3>- GoLand (IDE เฉพาะสำหรับ Go)</h3></li>
    <li><h3>- Sublime Text หรือ Atom + ส่วนขยาย Go</h3></li>
</ol>

<h4>2.4 การสร้างโปรเจคแรก</h4>
<h3>- สร้างโฟลเดอร์ใหม่ และสร้างไฟล์ `hello.go` ข้างใน</h3>
</v-clicks>

---

<h2>3. ตัวแปรและชนิดข้อมูลพื้นฐาน</h2>

<v-clicks>

<h4>3.1 ชนิดข้อมูลพื้นฐานใน Go</h4>

<h3>
    <li><strong>string</strong> - ข้อความ เช่น "สวัสดี", "ภาษา Go สนุกมาก"</li>
    <li><strong>int</strong> - จำนวนเต็ม เช่น 1, 42, -10, 0</li>
    <li><strong>float64</strong> - จำนวนทศนิยม เช่น 3.14, 0.5, -1.23</li>
    <li><strong>bool</strong> - ค่าความจริง true (จริง) หรือ false (เท็จ)</li>
</h3>

## 3.2 การประกาศตัวแปรแบบต่างๆ

```go {all|1|2|3|all}
// แบบที่ 1: ประกาศและกำหนดค่าแยกกัน
var name string
name = "โกโก้"

// แบบที่ 2: ประกาศและกำหนดค่าในบรรทัดเดียว
var age int = 25

// แบบที่ 3: ให้ Go เดาชนิดข้อมูลจากค่าที่กำหนด
var height = 175.5  // Go จะเดาว่าเป็น float64

// แบบที่ 4: แบบย่อด้วยเครื่องหมาย := (ใช้ได้เฉพาะในฟังก์ชัน)
score := 100        // เทียบเท่า var score = 100
message := "Hello"  // เทียบเท่า var message = "Hello"
```

</v-clicks>

---

## 3.3 การแสดงผลตัวแปร

<v-clicks>
<h3 class="text-green">Code : </h3>

```go {1|2|3|4|all}
name := "โกโก้"
age := 25
fmt.Println("ชื่อ:", name)
fmt.Println("อายุ:", age)

// หรือใช้ Printf เพื่อจัดรูปแบบ
fmt.Printf("คุณ%s อายุ %d ปี\n", name, age)
```

<h3 class="text-red">OutPut : </h3>

```text{1|2|3|4|all}
C:/Users/hello.go/go run hello.go
ชื่อ : สมชาย
อายุ : 99
คุณ สมชาย อายุ 99
```

## 3.4 ค่าเริ่มต้นของตัวแปร

<h3>
    <li>- string: "" (ข้อความว่าง)
</li>
    <li>- int: 0
</li>
    <li>- float64: 0.0
</li>
    <li>- bool: false
</li>
</h3>

</v-clicks>

---

## layout: two-cols

<template v-slot:default>

<v-clicks>

# 4. การคำนวณและตัวดำเนินการ (Operators)

#### 4.1 ตัวดำเนินการทางคณิตศาสตร์

<h4>
    <li><strong class="text-red">` + `</strong> บวก</li>
    <li><strong class="text-red">` - `</strong> ลบ</li>
    <li><strong class="text-red">` * `</strong> คูณ</li>
    <li><strong class="text-red">` / `</strong> หาร</li>
    <li><strong class="text-red">` %`</strong> หารเอาเศษ(modulo)</li>
</h4>

#### 4.2 ตัวอย่างการคำนวณ

```go {all|1-3|5-9|all}
a := 10
b := 3
result := 0

result = a + b  // result = 13
result = a - b  // result = 7
result = a * b  // result = 30
result = a / b  // result = 3 (เพราะเป็นการหารระหว่างจำนวนเต็ม ผลลัพธ์จึงเป็นจำนวนเต็ม)
result = a % b  // result = 1 (เศษจากการหาร 10 ÷ 3 = 3 เหลือเศษ 1)
```

</v-clicks>

</template>

<template v-slot:right>

<v-clicks>

<h3 class="text-red">Output:</h3>

```text
C:/Users/hello.go/go run hello.go
13
7
30
3
1
```

</v-clicks>
</template>

---

## 4.3 การคำนวณทศนิยม

<v-clicks>

```go {all|1-3|5|all}
x := 10.0  // ต้องเป็น float64
y := 3.0   // ต้องเป็น float64
result := 0.0

result = x / y  // result = 3.3333333333333335
```

<h3 class="text-red">Output:</h3>
```text
C:/Users/hello.go/go run hello.go
3.3333333333333335
```

## 4.4 ตัวดำเนินการเพิ่ม/ลดค่า

```go {all|1-2|4-5|7-8|all}
count := 5
count++      // เพิ่มค่า 1 (count = 6)

value := 10
value--      // ลดค่า 1 (value = 9)

number := 7
number += 3  // เพิ่มค่าด้วยจำนวนที่กำหนด (number = 10)
```

<h3 class="text-red">Output:</h3>
```text
C:/Users/hello.go/go run hello.go
count: 6
value: 9
number: 10
```

</v-clicks>

---

## 4.5 ตัวดำเนินการเปรียบเทียบ

<v-clicks>

| ตัวดำเนินการ | ความหมาย            |
| ------------ | ------------------- |
| `==`         | เท่ากับ             |
| `!=`         | ไม่เท่ากับ          |
| `<`          | น้อยกว่า            |
| `>`          | มากกว่า             |
| `<=`         | น้อยกว่าหรือเท่ากับ |
| `>=`         | มากกว่าหรือเท่ากับ  |

</v-clicks>

---

## 4.6 ตัวดำเนินการทางตรรกะ

<v-clicks>

<table>
  <thead>
    <tr>
      <th>ตัวดำเนินการ</th>
      <th>ความหมาย</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>&&</td>
      <td>และ (and)</td>
    </tr>
    <tr>
      <td>||</td>
      <td>หรือ (or)</td>
    </tr>
    <tr>
      <td>!</td>
      <td>ไม่ (not)</td>
    </tr>
  </tbody>
</table>

<div class="flex justify-center">
    <img class="object-fill h-65 w-[1000px]" src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExbHBrYXc0a3l6bmVvcXZ0ZmRuNGx2ZGZja2N4M2lrZDRsbWx2MnBlciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/4qx6IRdg26uZ3MTtRn/giphy.gif">
</div>

</v-clicks>

---

# Mini Project โปรแกรมคำนวณพื้นที่รูปทรงต่างๆ

<v-clicks>

### โปรแกรมคำนวณพื้นที่สี่เหลี่ยม

<h3 class="text-green">Code : </h3>

```go {all|1-3|5|7-10|12-15|17|19-20|all}
package main

import "fmt"

func main() {
    // ประกาศตัวแปรสำหรับเก็บความกว้างและความยาว
    var width, height float64

    fmt.Print("ป้อนความกว้าง: ")
    fmt.Scanln(&width)

    fmt.Print("ป้อนความยาว: ")
    fmt.Scanln(&height)

    // คำนวณพื้นที่
    area := width * height

    // แสดงผลลัพธ์
    fmt.Printf("พื้นที่สี่เหลี่ยม = %.2f หน่วย\n", area)
}
```

</v-clicks>

---

# Mini Project โปรแกรมคำนวณพื้นที่รูปทรงต่างๆ

### โปรแกรมคำนวณพื้นที่วงกลม

<v-clicks>
<h3 class="text-green">Code : </h3>

```go {1-6|9|11-12|14-15|17|all}
package main

import (
    "fmt"
    "math" // ใช้สำหรับค่า Pi
)

func main() {
    var radius float64

    fmt.Print("ป้อนรัศมีวงกลม: ")
    fmt.Scanln(&radius)

    // คำนวณพื้นที่วงกลม (π × r²)
    area := math.Pi * math.Pow(radius, 2)

    fmt.Printf("พื้นที่วงกลม = %.2f หน่วย\n", area)
}
```

</v-clicks>

---

# 5. การแสดงผลข้อความ (Output) 🖥️

<v-clicks>

<h4>5.1 โครงสร้างพื้นฐานของโปรแกรม Go</h4>

```go {all|1|3|5|6|7|all}
package main // ประกาศว่านี่คือโปรแกรมหลัก

import "fmt" // นำเข้าไลบรารีสำหรับแสดงผล

func main() {
    // โค้ดที่จะทำงานเมื่อรันโปรแกรม
}
```

<h4>5.2 คำสั่งแสดงผลพื้นฐาน</h4>

```go {all|1|2|3|4-5|all}
fmt.Println("สวัสดี! นี่คือโปรแกรมแรกของฉัน") // แสดงข้อความแล้วขึ้นบรรทัดใหม่
fmt.Print("ข้อความนี้") // แสดงข้อความโดยไม่ขึ้นบรรทัดใหม่
fmt.Print(" ต่อกัน\n") // \n คือการขึ้นบรรทัดใหม่ด้วยตัวเอง
fmt.Printf("ชื่อ: %s, อายุ: %d\n", "โกโก้", 25) // แสดงผลแบบกำหนดรูปแบบ
// %s = ข้อความ (string), %d = ตัวเลขจำนวนเต็ม (int)
```

<h4>5.3 การรันโปรแกรม</h4>

<p>บันทึกไฟล์ `.go` แล้วเปิด Terminal หรือ Command Prompt:</p>

```bash
go run hello.go
```

</v-clicks>

---

<h1>5.4 ตัวอย่างโปรแกรมแสดงผลพื้นฐาน (แบบเต็ม)</h1>
<h4>Code : </h4>
<v-clicks>

```go
package main

import "fmt"

func main() {
    fmt.Println("สวัสดี! นี่คือโปรแกรมแรกของฉัน")
    fmt.Println("===== โปรแกรม Go =====")
    fmt.Println("บรรทัดที่ 1")
    fmt.Println("บรรทัดที่ 2")
    fmt.Println("บรรทัดที่ 3")
    fmt.Println("=====================")
}
```

</v-clicks>

<v-clicks>
<h4>Output : </h4>
```text {1|2|3-9|all}
C:/Users/hello.go/go run hello.go
C:/Users/hello.go/
สวัสดี! นี่คือโปรแกรมแรกของฉัน
===== โปรแกรม Go =====
บรรทัดที่ 1
บรรทัดที่ 2
บรรทัดที่ 3
=====================
```
</v-clicks>

---

# 6. การรับข้อมูลจากผู้ใช้ (Input) 🖥️

<h4>6.1 การประกาศตัวแปรเพื่อเก็บข้อมูล</h4>

<v-clicks>

```go {all|1|2|3|all}
var name string     // ประกาศตัวแปรชื่อ name เป็นชนิดข้อความ
var age int         // ประกาศตัวแปรชื่อ age เป็นชนิดตัวเลขจำนวนเต็ม
var height float64  // ประกาศตัวแปรชื่อ height เป็นชนิดทศนิยม
```

<h4>6.2 การรับข้อมูลด้วย Scanln</h4>

```go {all|1|2|3-4|all}
var name string
fmt.Print("กรุณาป้อนชื่อของคุณ: ") // แสดงข้อความเพื่อขอข้อมูล
fmt.Scanln(&name)
fmt.Println(name) // แสดงข้อความเพื่อขอข้อมูล // รับข้อมูลและเก็บในตัวแปร name
// & คือการอ้างอิงถึงตำแหน่งของตัวแปรในหน่วยความจำ
```

<h3 class="text-red">output : </h3>

```text
C:/Users/hello.go/go run hello.go
C:/Users/hello.go/ กรุณาป้อนชื่อของคุณ: [ใส่ชื่อ]
[ชื่อที่ออกมา]
```

</v-clicks>

---

## 6.3 การรับข้อมูลตัวเลข

<v-clicks>

```go {all|1-2|3-4|5-6|all}
var age int
fmt.Print("กรุณาป้อนอายุของคุณ: ")
fmt.Scanln(&age)
fmt.Println("คุณอายุ", age, "ปี")
// สามารถผสมตัวแปรกับข้อความใน Println ได้
// ตัวแปรและข้อความจะถูกคั่นด้วยช่องว่างโดยอัตโนมัติ
```

<h3 class="text-red">Output :</h3>
```text
C:/Users/hello.go/_
C:/Users/hello.go/99
คุณอายุ 99 ปี
```

<div class="absolute left-320px bottom-25px">
  <img class="w-70" src="https://i.imgflip.com/9le287.jpg" />
</div>
 </v-clicks>

---

## layout: two-cols

<template v-slot:default >

<h1>6.4 โปรแกรมทักทาย (ตัวอย่างแบบเต็ม)</h1>
<h3 class="text-green">Code : </h3>

<v-clicks>

```go
package main

import "fmt"

func main() {
    var name string
    var age int

    fmt.Print("คุณชื่ออะไร? ")
    fmt.Scanln(&name)

    fmt.Print("คุณอายุเท่าไร? ")
    fmt.Scanln(&age)

    fmt.Printf("สวัสดี คุณ%s อายุ %d ปี ยินดีที่ได้รู้จัก!\n", name, age)
}
```

</v-clicks>

</template>

<template v-slot:right >
<v-clicks>

<div class="absolute left-500px bottom-238px w-96 text-red">

### Output :

```text
C:/Users/hello.go/go run hello.go
C:/Users/hello.go/
คุณชื่ออะไร? สมชาย
C:/Users/hello.go/
คุณอายุเท่าไร? 25
C:/Users/hello.go/
สวัสดี คุณสมชาย อายุ 25 ปี ยินดีที่ได้รู้จัก!
```

</div>

</v-clicks>

<v-clicks>
<div class="absolute left-600px bottom-70px">
    <img class="w-45" src="https://i.imgflip.com/9le0v0.jpg">
</div>
</v-clicks>

</template>

---

# 7. การตัดสินใจด้วย if-else 🤔

<v-clicks>

## 7.1 รูปแบบพื้นฐานของ if-else

```go {all|1-3|4-6|all}
if เงื่อนไข {
    // ทำเมื่อเงื่อนไขเป็นจริง
} else {
    // ทำเมื่อเงื่อนไขเป็นเท็จ
}
```

<h4>ตัวอย่าง</h4>

```go
var num int
fmt.Print("คะแนน ")
fmt.Scanln(&num)

// ตรวจสอบอายุ
if num >= 80 {
    fmt.Println("A")
} else {
    fmt.Println("F")
}
```

</v-clicks>

---

## 7.2 ตัวอย่าง - ตรวจสอบอายุ

<v-clicks>

```go {all|1-4|6-10|12-14|all}
// รับข้อมูลอายุจากผู้ใช้
var age int
fmt.Print("คุณอายุเท่าไร? ")
fmt.Scanln(&age)

// ตรวจสอบอายุ
if age >= 18 {
    fmt.Println("คุณเป็นผู้ใหญ่แล้ว สามารถเข้าชมได้")
} else {
    fmt.Println("คุณยังเป็นเด็ก ไม่สามารถเข้าชมได้")
}

// เพิ่มเติม: สามารถใช้ if โดยไม่มี else ได้
if age == 0 {
    fmt.Println("ข้อมูลอายุไม่ถูกต้อง")
}
```

<h3 class="text-red">output : </h3>
```text
C:/Users/hello.go/go run hello.go
คุณอายุเท่าไร? 99
คุณเป็นผู้ใหญ่แล้ว สามารถเข้าชมได้
```

</v-clicks>

---

## 7.3 if-else if-else (หลายเงื่อนไข)

<v-clicks>

```go {all|1|3-5|6-8|9-11|all}
score := 75

if score >= 80 {
    fmt.Println("เกรด A")
} else if score >= 70 {
    fmt.Println("เกรด B")
} else if score >= 60 {
    fmt.Println("เกรด C")
} else {
    fmt.Println("เกรด F")
}
```

## 7.4 การใช้ตัวดำเนินการทางตรรกะ

```go
age := 25
hasID := true

if age >= 18 && hasID {
    fmt.Println("สามารถซื้อเครื่องดื่มแอลกอฮอล์ได้")
} else {
    fmt.Println("ไม่สามารถซื้อเครื่องดื่มแอลกอฮอล์ได้")
}
```

</v-clicks>

---

# 8. การทำซ้ำด้วย for loop 🔁

<v-clicks>

#### 8.1 for loop แบบมาตรฐาน

```go {all|1|2|3|1-3|all}
for ค่าเริ่มต้น; เงื่อนไข; การเปลี่ยนแปลง {
    // คำสั่งที่จะทำซ้ำ
}
```

#### 8.2 ตัวอย่าง - การนับเลข 1 ถึง 5

```go {all|1-3|all}
for i := 1; i <= 5; i++ {
    fmt.Println(i)
}
```

<h3 class="text-red">output : </h3>
```text{1|2-6|all}
C:/Users/hello.go/go run hello.go
1
2
3
4
5
```

</v-clicks>

---

#### 8.3 ตัวอย่าง - การแสดงสูตรคูณ

<v-clicks>

```go {all|1-2|4|6-8|all}
number := 2
fmt.Println("สูตรคูณแม่", number)

fmt.Println("===============")

for i := 1; i <= 12; i++ {
    fmt.Printf("%d x %d = %d\n", number, i, number*i)
}
```

```text{1|2|3|4|all}
C:/Users/hello.go/go run hello.go
สูตรคูณแม่ 2
===============
2 x 1 = 2
2 x 2 = 4
2 x 3 = 6
2 x 4 = 8
2 x 5 = 10
2 x 6 = 12
2 x 7 = 14
2 x 8 = 16
2 x 9 = 18
2 x 10 = 20
2 x 11 = 22
2 x 12 = 24
```

</v-clicks>

---

#### 8.4 for loop แบบ while (ไม่มี while ใน Go)

```go {all|1|2-4|all}
for เงื่อนไข {
    // คำสั่งที่จะทำซ้ำตราบใดที่เงื่อนไขเป็นจริง
}
```

#### 8.5 ตัวอย่าง - การรับข้อมูลจนกว่าจะถูกต้อง

<v-clicks>

```go
var password string

for {
    fmt.Print("ป้อนรหัสผ่าน: ")
    fmt.Scanln(&password)

    if password == "abc123" {
        fmt.Println("รหัสผ่านถูกต้อง")
        break  // ออกจาก loop
    }

    fmt.Println("รหัสผ่านไม่ถูกต้อง ลองใหม่อีกครั้ง")
}
```

```text
มันจะรันจนกว่าจะใส่รหัส abc123 ถูกแต่ถ้าใส่ไม่ถูกก็จะกลับมาใส่เรื่อยๆ
```

</v-clicks>

---

# 9. ฟังก์ชันพื้นฐาน 🚀

<v-clicks>

#### 9.1 การสร้างฟังก์ชันพื้นฐาน

```go {all|1|2-4|all}
func ชื่อฟังก์ชัน() {
    // คำสั่งต่างๆ ภายในฟังก์ชัน
}
```

#### 9.2 ตัวอย่าง - ฟังก์ชันแสดงข้อความทักทาย

```go {all|1-3|6|all}
func sayHello() {
    fmt.Println("สวัสดี! ยินดีต้อนรับสู่โปรแกรม Go")
}

func main() {
    sayHello()  // เรียกใช้ฟังก์ชัน
}
```

<h3 class="text-red"> output :   </h3>
```text
C:/Users/hello.go/go run hello.go
สวัสดี! ยินดีต้อนรับสู่โปรแกรม Go
```

</v-clicks>

---

#### 9.3 ฟังก์ชันที่รับพารามิเตอร์

<v-clicks>

```go {all|1|2-4|7-8|all}
func greet(name string) {
    fmt.Printf("สวัสดี คุณ%s!\n", name)
}

func main() {
    // เรียกใช้ฟังก์ชันพร้อมส่งค่า
    greet("ธนา")
    greet("นภา")
}
```

<h3 class="text-red">Output:</h3>
```text
C:/Users/hello.go/go run hello.go
สวัสดี คุณธนา!
สวัสดี คุณนภา!
```

</v-clicks>

---

## layout: two-cols

<v-clicks>

<template v-slot:default>

## 10. การจัดการข้อผิดพลาด 🚨

<h4>10.1 การจัดการข้อผิดพลาดพื้นฐาน</h4>

```go {all|1-3|5-13|all}
import (
    "fmt"
    "strconv"  // ใช้สำหรับแปลงข้อความเป็นตัวเลข
)

func main() {
    var input string
    fmt.Print("ป้อนตัวเลข: ")
    fmt.Scanln(&input)

    number, err := strconv.Atoi(input)  // แปลงข้อความเป็นตัวเลข

    if err != nil {  // ถ้ามีข้อผิดพลาด
        fmt.Println("เกิดข้อผิดพลาด:", err)
    } else {
        fmt.Println("ตัวเลขที่ป้อน คือ", number)
    }
}
```

</template>
</v-clicks>

<div class="absolute left-500px bottom-238px w-100">
<v-clicks>

<h3>กรณีที่ 1: ผู้ใช้ป้อนตัวเลขที่ถูกต้อง (เช่น "123")</h3>

```
C:/Users/hello.go/go run hello.go
ป้อนตัวเลข: 123
ตัวเลขที่ป้อน คือ 123
```

<h3>กรณีที่ 2: ผู้ใช้ป้อนข้อมูลที่ไม่ใช่ตัวเลข (เช่น "abc")</h3>

```
C:/Users/hello.go/go run hello.go
ป้อนตัวเลข: abc
เกิดข้อผิดพลาด: strconv.Atoi: parsing "abc": invalid syntax
```

</v-clicks>
</div>

<v-clicks>
<div class="absolute left-600px bottom-70px rounded-xl">
  <img class="w-100 w-50 " src="https://i.imgflip.com/9le287.jpg" />
</div>
</v-clicks>

---

#### 10.2 การใช้ panic และ recover

<v-clicks>

```go
import "fmt"

func riskyFunction() {
    defer func() {
        if r := recover(); r != nil {
            fmt.Println("ฟื้นฟูจากข้อผิดพลาด:", r)
        }
    }()

    // สร้างข้อผิดพลาดด้วย panic
    panic("เกิดข้อผิดพลาดร้ายแรง!")
}

func main() {
    fmt.Println("เริ่มต้นโปรแกรม")
    riskyFunction()
    fmt.Println("โปรแกรมทำงานต่อไปได้")
}
```

<h3 class="text-red">Output:</h3>
```text
C:/Users/hello.go/go run hello.go
เริ่มต้นโปรแกรม
ฟื้นฟูจากข้อผิดพลาด: เกิดข้อผิดพลาดร้ายแรง!
โปรแกรมทำงานต่อไปได้
```

</v-clicks>

---

# 11. โครงสร้างข้อมูลพื้นฐาน (Slices & Maps) 🚧

<v-clicks>

## 11.1 Slice - อาร์เรย์ที่ปรับขนาดได้

```go {all|1-2|4-5|7-9|11-12|all}
// การประกาศ slice
var scores []int  // ประกาศ slice ว่างๆ

// การกำหนดค่าเริ่มต้น
scores = []int{95, 88, 76, 100, 67}  // กำหนดค่าเริ่มต้น

// การวนลูปแสดงผลข้อมูลใน slice
for i, score := range scores {
    fmt.Printf("คะแนนที่ %d: %d\n", i+1, score)
}

// การเพิ่มข้อมูลใน slice
scores = append(scores, 82)  // เพิ่ม 82 ต่อท้าย slice
```

<h3 class="text-red">Output:</h3>

```text
C:/Users/hello.go/go run hello.go
คะแนนที่ 1: 95
คะแนนที่ 2: 88
คะแนนที่ 3: 76
คะแนนที่ 4: 100
คะแนนที่ 5: 67
```

</v-clicks>

---

## 11.2 Map - ข้อมูลแบบคู่ key-value

<v-clicks>

```go {all|1-6|8-10|12-13|all}
// การประกาศและกำหนดค่า map
scores := map[string]int{
    "วิชาคณิตศาสตร์": 85,
    "วิชาภาษาไทย":   92,
    "วิชาอังกฤษ":    78,
}

// การวนลูปแสดงผลข้อมูลใน map
for subject, score := range scores {
    fmt.Printf("%s: %d คะแนน\n", subject, score)
}

// การเพิ่มข้อมูลใน map
scores["วิชาวิทยาศาสตร์"] = 88
```

<h3 class="text-red">Output:</h3>

```text
C:/Users/hello.go/go run hello.go
วิชาคณิตศาสตร์: 85 คะแนน
วิชาภาษาไทย: 92 คะแนน
วิชาอังกฤษ: 78 คะแนน
วิชาวิทยาศาสตร์: 88 คะแนน
```

</v-clicks>

---

## layout: two-cols

<template v-slot:default>

## 11.3 การใช้งาน Slice และ Map ร่วมกัน

```go {all|1-3|5-11|13-15|all}
// สร้าง map เก็บ slice ของคะแนนแต่ละวิชา
studentScores := make(map[string][]int)

// เพิ่มคะแนนสอบแต่ละครั้งของแต่ละวิชา
studentScores["คณิตศาสตร์"] = []int{85, 90, 88}
studentScores["ภาษาไทย"] = []int{92, 87, 95}

// แสดงผลคะแนนทั้งหมด
for subject, scores := range studentScores {
    fmt.Printf("%s: %v\n", subject, scores)
}

// คำนวณคะแนนเฉลี่ยของแต่ละวิชา
for subject, scores := range studentScores {
    sum := 0
    for _, score := range scores {
        sum += score
    }
    average := float64(sum) / float64(len(scores))
    fmt.Printf("คะแนนเฉลี่ย%s: %.2f\n", subject, average)
}
```

</template>

<template v-slot:right >

<div class="ml-10 mt-1">
<h3 class="text-red">Output:</h3>

<v-clicks>

```text
C:/Users/hello.go/go run hello.go
คณิตศาสตร์: [85 90 88]
ภาษาไทย: [92 87 95]
คะแนนเฉลี่ยคณิตศาสตร์: 87.67
คะแนนเฉลี่ยภาษาไทย: 91.33
```

</v-clicks>

</div>

<v-clicks>
<div class="ml-10">
  <img class="w-100 h-70" src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExcmR2cGU2bXZtZ2l2dmdiNTBpNDZ1NzM0Zjk0OWd4YnlxMWFla3FmOSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/st8Wfzji7jm146Ru7p/giphy.gif" />
</div>
</v-clicks>

</template>

---

<div class="flex justify-center mt-10">
  <img class="w-100" src="https://go.dev/images/gophers/newscaster.svg" />
</div>

<h1 class="text-xl mt-10 text-blue text-center">"Hello World"</h1>
<p  class="text-xl mt-10 text-center">เลือกสาขามาถูกแล้วสินะ ยินดีต้อนรับสู่นรก</p>
<p  class="text-xl mt-10 text-center">ขอให้เรียนสนุกและโชคดี By <a href="https://github.com/TitleKung-01">TitleKung</a></p>

---

<div class="flex justify-center mt-10">
  <img class="w-100" src="https://go.dev/images/gophers/biplane.svg" />
</div>
<p class="flex justify-center text-center text-4xl">"Wait a minute!  ถ้าอยากได้ A ต้องลองทำโจทย์นี้"</p>
<div class="flex justify-center text-center" >
  ไปดูโจทย์เลย Broo!!  <carbon:arrow-right />
</div>

---

## layout: two-cols

<template v-slot:default>

<v-clicks>

# 1. เกมทายตัวเลข 🎮

### :::: ความต้องการของโปรแกรม ::::

<ul>
  <li>ให้ผู้เล่นเลือกระดับความยาก</li>
  <li>แสดงจำนวนครั้งที่เหลือในการทาย</li>
  <li>มีระบบคะแนน (คะแนนเริ่มต้น 100)</li>
  <li>แสดงผลว่า "มากไป" หรือ "น้อยไป"</li>
  <li>เมื่อเล่นจบให้แสดงคะแนนที่ได้</li>
</ul>

### ::: ระดับความยาก :::

<ul>
  <li>ระดับง่าย: ทายตัวเลข 1-50 (10 ครั้ง)</li>
  <li>ระดับกลาง: ทายตัวเลข 1-100 (7 ครั้ง)</li>
  <li>ระดับยาก: ทายตัวเลข 1-200 (5 ครั้ง)</li>
</ul>

</v-clicks>

</template>

<template v-slot:right>

<v-clicks>

<div class="mt-10">
  <img class="w-80" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExcmR2cGU2bXZtZ2l2dmdiNTBpNDZ1NzM0Zjk0OWd4YnlxMWFla3FmOSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/st8Wfzji7jm146Ru7p/giphy.gif" />
</div>

### Bonus Features 🌟 (ถ้าทำได้ลองทำ)

<ul>
  <li>เพิ่มระบบ High Score</li>
  <li>เพิ่มระบบจับเวลา</li>
  <li>เพิ่มโหมดเล่นหลายรอบ</li>
</ul>

</v-clicks>

</template>

---

## layout: two-cols

<template v-slot:default>

<v-clicks>

## 2. โปรแกรมคำนวณเกรด 📚

### :::: ความต้องการของโปรแกรม ::::

<ul>
  <li>รับข้อมูลคะแนนแต่ละส่วนของแต่ละวิชา</li>
  <li>คำนวณเกรดตามเกณฑ์มาตรฐาน</li>
  <li>แสดงผลในรูปแบบตารางที่สวยงาม</li>
  <li>คำนวณและแสดง GPA</li>
</ul>

### ::: สัดส่วนคะแนน :::

<ul>
  <li>คะแนนเก็บ 30%</li>
  <li>คะแนนสอบกลางภาค 30%</li>
  <li>คะแนนสอบปลายภาค 40%</li>
</ul>

</v-clicks>

</template>

<template v-slot:right>

<v-clicks>

<div class="mt-10">
  <img class="w-80" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZHozbHlleXRvOTEyenQ4NDIyejQ1MGJ5N2RiNWdsaGhqY2xneXN0cyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/K4WqOlAGTIyopmlL4o/giphy.gif" />
</div>

### Bonus Features 🌟 (ถ้าทำได้ลองทำ)

<ul>
  <li>เพิ่มระบบบันทึกประวัติผลการเรียน</li>
  <li>แสดงกราฟพัฒนาการของแต่ละวิชา</li>
  <li>เพิ่มระบบแนะนำวิชาที่ควรปรับปรุง</li>
</ul>

</v-clicks>

</template>

---

## layout: two-cols

<template v-slot:default>

<v-clicks>

## 3. โปรแกรมบันทึกรายรับ-รายจ่าย 📈

### :::: ความต้องการของโปรแกรม ::::

<ul>
  <li>บันทึกรายการโดยระบุวันที่ ประเภท หมวดหมู่ จำนวนเงิน</li>
  <li>แสดงรายงานประจำวันและสรุปรายเดือน</li>
  <li>ค้นหารายการตามช่วงเวลา</li>
  <li>แสดงสถิติการใช้จ่ายแต่ละหมวดหมู่</li>
</ul>

</v-clicks>

</template>

<template v-slot:right>

<v-clicks>

<div class="mt-10">
  <img class="w-80" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbHBrYXc0a3l6bmVvcXZ0ZmRuNGx2ZGZja2N4M2lrZDRsbWx2MnBlciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/4qx6IRdg26uZ3MTtRn/giphy.gif" />
</div>

### Bonus Features 🌟 (ถ้าทำได้ลองทำ)

<ul>
  <li>เพิ่มระบบตั้งเป้าหมายการออม</li>
  <li>แสดงกราฟวิเคราะห์การใช้จ่าย</li>
  <li>ส่งออกรายงานเป็นไฟล์ CSV</li>
  <li>แจ้งเตือนเมื่อใช้จ่ายเกินงบ</li>
</ul>

</v-clicks>

</template>

---

<div class="flex justify-center mt-10">
  <img class="w-70" src="https://go.dev/images/gophers/biplane.svg" />
</div>

<h1 class="text-xl mt-10 text-blue text-center">ขอให้สนุกกับการทำโปรเจค!</h1>
<p class="text-xl mt-5 text-center">ไม่ไหวก็ลองๆก็ทำได้ที่เข้าใจ ถ้าเข้าใจสนทำตามนนี้ได้ทั้งคือ เก่งกว่าพี่ละ 😇 </p>
<p class="text-xl mt-5 text-center">By <a href="https://github.com/TitleKung-01">TitleKung</a></p>
