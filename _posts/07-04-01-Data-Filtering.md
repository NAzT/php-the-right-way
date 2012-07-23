---
isChild: true
title: "การกรองข้อมูล"
anchorid: "data_filtering"
---

<h2 id="data_filtering">การกรองข้อมูล</h2>

อย่าเลยนะที่จะไว้ใจข้อมูลแปลกปลอมที่รับเข้ามา (เช่น ข้อมูลที่มาจาก form, ผู้แปล) จะให้ดีต้องตรวจพวกมันก่อนเอามาใช้ ฟังก์ชัน `filter_var` และ `filter_input` จะช่วยขัดเชื้อโรคร้ายในข้อมูลแปลกปลอมได้ (ยกตัวอย่างเช่น ที่อยู่อีเมล)

ข้อมูลแปลกปลอมสามารถเป็นอะไรก็ได้: ข้อมูลที่รับมาจากฟอร์ม `$_GET` และ `$_POST` หรือค่าที่อยู่ในตัวแปร superglobal `$_SERVER` และอาจเป็นการเรียก `fopen('php://input', 'r')` เพื่อเอาค่า HTTP body ก็ได้ จำไว้ว่าข้อมูลแปลกปลอมไม่ได้จำกัดอยู่เฉพาะข้อมูลจากฟอร์มที่ผู้ใช้ส่งเข้ามา แต่ยังรวมถึงไฟล์ที่อัพโหลดหรือดาวน์โหลดลงมา ค่าเซสชั่น คุกกี้ และค่าที่มาจากเว็บเซอร์วิสอื่นๆ ก็ถือเป็นข้อมูลแปลกปลอมหรือข้อมูลต่างด้าวเช่นกัน

While foreign data can be stored, combined, and accessed later, it is still foreign input. Every
time you process, output, concatenate, or include data in your code, ask yourself if
the data is filtered properly and can it be trusted.

Data may be _filtered_ differently based on its purpose. For example, when unfiltered foreign input is passed
into HTML page output, it can execute HTML and JavaScript on your site! This is known as Cross-Site
Scripting (XSS) and can be a very dangerous attack. One way to avoid XSS is to sanitize all HTML tags
in the input by removing tags or escaping them into HTML entities.

Another example is passing options to be executed on the command line. This can be extremely dangerous
(and is usually a bad idea), but you can use the built-in `escapeshellarg` function to sanitize the executed
command's arguments.

One last example is accepting foreign input to determine a file to load from the filesystem. This can be exploited by
changing the filename to a file path. You need to remove "/", "../", [null bytes][6], or other characters from the file path so it can't
load hidden, non-public, or sensitive files.

* [Learn about data filtering][1]
* [Learn about `filter_var`][4]
* [Learn about `filter_input`][5]
* [Learn about handling null bytes][6]

### Sanitization

Sanitization removes (or escapes) illegal or unsafe characters from foreign input.

For example, you should sanitize foreign input before including the input in HTML or inserting it
into a raw SQL query. When you use bound parameters with [PDO](#databases), it will
sanitize the input for you.

Sometimes it is required to allow some safe HTML tags in the input when including it in the HTML
page. This is very hard to do and many avoid it by using other more restricted formatting like
Markdown or BBCode, although whitelisting libraries like [HTML Purifier][html-purifier] exists for
this reason.

[See Sanitization Filters][2]

### Validation

Validation ensures that foreign input is what you expect. For example, you may want to validate an
email address, a phone number, or age when processing a registration submission.

[See Validation Filters][3]

[1]: http://www.php.net/manual/en/book.filter.php
[2]: http://www.php.net/manual/en/filter.filters.sanitize.php
[3]: http://www.php.net/manual/en/filter.filters.validate.php
[4]: http://php.net/manual/en/function.filter-var.php
[5]: http://www.php.net/manual/en/function.filter-input.php
[6]: http://php.net/manual/en/security.filesystem.nullbytes.php
[html-purifier]: http://htmlpurifier.org/
