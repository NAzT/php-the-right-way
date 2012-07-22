---
isChild: true
---

## กรอบของการโปรแกรมมิ่ง

เป็นภาษาที่มีความยืดหยุ่นสูง เป็นภาษาแบบไดนามิกส์ รองรับเทคนิคการเขียนโปรแกรมหลายรูปแบบ
ตั้งแต่การเขียนโปรแกรมเชิงวัตถุ(object oriented programming) ที่ถูกเพิ่มเข้ามาเมื่อปี 2004 การใช้ฟังก์ชั่นแบบ anonymous และ namespaces ที่ถูก
เพิ่มเข้ามาในเวอร์ชั่น 5.3 เมื่อปี  2009 และล่าสุดคือการเพิ่มสิ่งที่เรียกว่า trait เข้ามาในเวอร์ชั่น 5.4 ในปี 2012

### การเขียนโปรแกรมเชิงวัตถุ(object-oriented programming)

PHP เป็นภาษาที่มีความพร้อมเรื่องการเขียนโปรแกรมเชิงวัตถุสูงมาก
ภาษาหนึ่งเลยก็ว่าได้ความสามารถหลักเช่น class, abstract class, interface class, inheritance, constructor, cloning, exception และอื่นๆได้
ถูกสร้างไว้ให้เราใช้งานอย่างเพียบพร้อม

* [Read about Object-oriented PHP][oop]
* [Read about Traits][traits]

### การเขียนโปรแกรมเชิงฟังก์ชั่น(functional programming)

PHP รองรับแนวคิดเรื่อง first-class function ซึ่งเป็นแนวที่ทำให้เราสามารถกำหนดฟังก์ชั่นเข้ากับตัวแปรได้โดยฟังก์ชั่นเหล่านั้นเป็นได้ นอกจากนี้ทั้ง user-defined และ built-in
ฟังก์ชั่นยังสามารถถูกอ้างโดยตัวแปรและถูกเรียกแบบ dynamic ได้ด้วย ยิ่งไปกว่านั้นฟังก์ชั่นยังสามารถถูกส่งเข้าไปเป็นพารามิเตอร์ของฟังก์ชั่นอื่น (ความสามารถนี้เรียกว่า high-order functions) 
และฟังก์ชั่นยังสามารถถูก return กลับออกมาจากฟังก์ชั่นได้อีกด้วย

การทำ recursion ที่ยอมให้ฟังก์ชั่นเรียกตัวเองได้นั้นก็สามารถใช้ได้แต่ส่วนใหญ่แล้วโค้ดของ PHP จะโฟกัสไปที่ iteration

การใช้ anonymous ฟังก์ชั่น (รองรับเรื่องการทำ closures) ถูกใส่เข้ามาตั้งแต่ PHP5.3

PHP5.4 เพิ่มความสามารถเรื่องการ bind closure เข้ากับ object scope ได้และยังปรับปรุงความสามารถเรื่อง
การทำ callable นั่นคือเราสามารถใช้มันสำหรับการแลกเปลี่ยนกับ anonymous ฟังก์ชั่นได้เกือบทุกกรณี

* Continue reading on [Functional Programming in PHP](/pages/Functional-Programming.html)
* [Read about Anonymous Functions][anonymous-functions]
* [Read about the Closure class][closure-class]
* [More details in the Closures RFC][closures-rfc]
* [Read about Callables][callables]
* [Read about dynamically invoking functions with `call_user_func_array`][call-user-func-array]

### การเขียนโปรแกรมเชิงนิยาม(meta programming)

PHP เองรองรับการทำงานของ meta programming หลายรูปแบบโดยสิ่งที่อยู่เบื้องหลังการทำงานคือสิ่งที่เรียกว่า Reflection API และ Magic Method 
เราจะพบ Magic Method ที่เราสามารถใช้งานได้เลยโดยไม่ต้งอเขียนเช่น `__get()`, `__set()`, `__clone()`, `__toString()`, `__invoke()` 
โปรแกรมเมอร์ภาษา Ruby พูดเสมอว่า PHP ไม่มีสิ่งที่เรียกว่า  `method_missing` แต่ตอนนี้เรามีแล้วและอยู่ในรูปแบบของ `__call()` และ `__callStatic()`

* [Read about Magic Methods][magic-methods]
* [Read about Reflection][reflection]

[namespaces]: http://php.net/manual/en/language.namespaces.php
[overloading]: http://uk.php.net/manual/en/language.oop5.overloading.php
[oop]: http://www.php.net/manual/en/language.oop5.php
[anonymous-functions]: http://www.php.net/manual/en/functions.anonymous.php
[closure-class]: http://php.net/manual/en/class.closure.php
[callables]: http://php.net/manual/en/language.types.callable.php
[magic-methods]: http://php.net/manual/en/language.oop5.magic.php
[reflection]: http://www.php.net/manual/en/intro.reflection.php
[traits]: http://www.php.net/traits
[call-user-func-array]: http://php.net/manual/en/function.call-user-func-array.php
[closures-rfc]: https://wiki.php.net/rfc/closures
