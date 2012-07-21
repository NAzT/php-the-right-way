# คู่มือเรื่องรูปแบบของโค้ด

กลุ่มผู้ใช้ PHP เป็นกลุ่มที่มีขนาดใหญ่มากและขยายตัวออกไปเรื่อยๆนอกจากนี้ตัวมันเองยังประกอบไปด้วยไลบรารี่จำนวนมหาศาล
เฟรมเวิร์คต่างๆอีกมากมายและจะเป็นเรื่องปกติที่นักพัฒนา PHP จะเลือกเอาสิ่งต่างๆเหล่านั้นมาผสมรวมกันเพื่อใช้สำหรับโปรเจคของตัวเอง ดังนั้นจึงเกิด
การตกลงร่วมกันว่าจะมีการเขียนโค้ดให้มีมาตรฐานให้ตรงกันมากที่สุดเท่าที่จะทำได้เพื่อให้นักพัฒนาท่านอื่นๆสามารถนำไลบารี่ต่างๆเหล่านั้นมาใช้รวมกันได้สะดวกมากขึ้น

กลุ่มที่ชื่อว่า [Framework Interop Group][fig] (หรือเราอาจรู้จักในชื่อ 'PHP Standards Group') ได้พยายามเสนอมาตรฐานการเขียนโค้ดออกมาสามชุดที่ประกอบไปด้วย  
[PSR-0][psr0], [PSR-1][psr1] และ [PSR-2][psr2] โดยทีข้อตกลงนี้ถูกใช้ในโปรเจคใหญ่ๆหลายตัวไม่ว่าจะเป็น
Drupal, Zend, CakePHP, phpBB, AWS SDK, FuelPHP,
Lithium, และอื่นๆดังนั้นถ้าเราเห็นว่ามันเหมาะสมกับการทำงานก็ควรจะนำมันมาใช้แต่ถ้าคิอว่าไม่เหมาะก็เขียนในแบบเดิมๆก็ไม่มีใครว่าอะไร

ดังนั้นกรณีที่ดีที่สุดคือเราจะเขียนโค้ดตามข้อตกลงอย่างน้อยหนึ่งชุดเพราะจะมำให้นักพัฒนาคนอื่นๆสามารถเข้าใจโค้ดเราได้มากขึ้น
และถ้าเป็นไปได้ก็ขอให้ทำตามข้อตกลง PSR-1 ซึ่งจะทำให้เราต้องใช้ PSR-0 ไปโดยปริยาย และสำหรับ PSR-2 เป็นทางเลือกที่สามารถเลือกได้ว่าจะทำหรือไม่ก็ได้

* [Read about PSR-0][psr0]
* [Read about PSR-1][psr1]
* [Read about PSR-2][psr2]

You can use the [phpcs-psr][phpcs-psr] sniff for [PHP_CodeSniffer][phpcs] to check code against these recommendations.
Use Fabien Potencier's [PHP Coding Standards Fixer][phpcsfixer] to automatically modify your code syntax so that it
conforms with these standards, saving you from fixing each problem by hand.เราสามารถใช้ [phpcs-psr][phpcs-psr] เพื่อตรวจสอบ  [PHP_CodeSniffer][phpcs] ว่าเราได้ทำตามข้อตกลงหรือไม่ และนอกจากนี้เรายัง
สามารถใช้ Fabien Potencier's [PHP Coding Standards Fixer][phpcsfixer] ที่จะช่วยเราแก้ไขรูปแบบการเขียนโค้ดให้เป็นไปตามข้อตกลงที่เราเลือกได้แบบอัตโนมัติ

[fig]: http://www.php-fig.org/
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr1]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md
[psr2]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md
[phpcs]: http://pear.php.net/package/PHP_CodeSniffer/
[phpcs-psr]: https://github.com/klaussilveira/phpcs-psr
[phpcsfixer]: http://cs.sensiolabs.org/
