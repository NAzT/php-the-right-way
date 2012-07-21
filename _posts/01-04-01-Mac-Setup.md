---
isChild: true
---

## การติดตั้งบนเครื่อง Mac

โดยปกติ OSX จะเตรียมแพกเกจ PHP มาให้พร้อมอยู่แล้วอย่างไรก็ตามเวอร์ชั่นที่เราได้มากับ OSX นั้นจะเป็นเวอร์ชั่นที่เก่าไปนิดเช่น
เราจะได้ PHP5.3.6 มาพร้อมกับ Lion และ PHP 5.3.10 มากับ Mountain Lion  

ดังนั้นเราต้อง update ไปสู่เวอร์ชั่นที่ใหม่กว่านี้และการ update PHP บน OSX เองก็
สามารถทำได้หลายวิธีเช่น [package managers][mac-package-managers],กับ [php-osx by Liip][php-osx-downloads]

อีกหนึ่งทางเลือกคือการ [คอมไพล์เอง][mac-compile], แต่นั่นหมายความว่าเราต้องติดตั้ง Xcode หรือ
Apple's substitute ["Command Line Tools for Xcode"][apple-developer] ซึ่งเราสามารถดาว์นโหลดได้ที่ Mac Developer Center.

อีกหนึ่งทางเลือกคือการใช้แพกเกจสำเร็จรูป "all-in-one" ที่มาพร้อมทั้ง PHP, Apache web server และ MySQL พร้อมกันนั้นเรา
จะได้เครื่องมือในการบริหารจัดการที่เป็น GUI มาด้วยตัวอย่างแพกเกจนั้นคือ [MAMP][mamp-downloads]

[mac-package-managers]: http://www.php.net/manual/en/install.macosx.packages.php
[mac-compile]: http://www.php.net/manual/en/install.macosx.compile.php
[xcode-gcc-substitution]: https://github.com/kennethreitz/osx-gcc-installer
[apple-developer]: https://developer.apple.com/downloads
[mamp-downloads]: http://www.mamp.info/en/downloads/index.html
[php-osx-downloads]: http://php-osx.liip.ch/
