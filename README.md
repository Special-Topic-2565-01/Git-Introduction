# git-introduction

git เป็น software ควบคุม version ที่มีการเก็บรักษา source code รวมทั้งไฟล์ต่าง ๆ ไว้ในเครื่องคอมพิวเตอร์ของผู้ใช้และบน server ได้พร้อมๆ กัน โดยจะเรียกพื้นที่เก็บไฟล์ว่า  'repository' 

ในขณะที่กำลังพัฒนาโปรแกรมหรือแก้ไขเอกสารต่างๆ เราสามารถใช้ git เป็นตัวช่วยการติดตามการเปลี่ยนแปลงและรวมส่วนต่างๆ ของโปรแกรมหรือเอกสารเข้าด้วยกัน จนกระทั่งได้โปรแกรมหรือเอกสารที่สมบูรณ์ และหากมีข้อผิดพลาด เราสามารถใช้ git เพื่อเปรียบเทียบความแตกต่างระหว่างการแก้ไขในแต่ละรุ่น นอกจากนี้ git ยังมีความสามารถอีกมากมายซึ่งจะได้กล่าวถึงในลำดับถัดไป

ผู้ใช้ที่มีสิทธิ์เข้าถึง repository สามารถช่วยกันพัฒนาโปรแกรมหรือช่วยกันแก้ไขเอกสารได้ โดยสามารถแก้ไขงานได้ที่เครื่องของตนเอง (local) และสามารถ upload การเปลี่ยนแปลงใดๆ ขึ้นไปเก็บบน server ได้ตามต้องการ

ภาพรวมในการทำงานของ git ทั้งฝั่ง local และ server แสดงได้ดังรูปที่ 1

![image](./Pictures/gi-intro/Slide2.PNG)

รูปที่ 1

จากรูปที่ 1 สมมติว่าผู้ใช้ทำการแก้ไข source code ของโปรแกรมบนคอมพิวเตอร์ส่วนบุคคล และใช้ git เป็นตัวช่วยติดตามการเปลี่ยนแปลง

เมื่อผู้ใช้สร้าง local repository ขึ้นใน folder ที่กำลังแก้ไข source code นั้น โปรแกรม  git ก็จะสร้างโฟลเดอร์ที่มี attribute เป็น hidden โดยตั้งชื่อว่า .git หากเราต้องการจะเข้าไปดูในโฟลเดอร์นั้น ต้องกำหนดตัวเลือกให้ file browser มองเห็นโฟลเดอร์ที่ซ่อนอยู่

ภายในโฟลเดอร์ .git จะมีองค์ประกอบสองอย่างคือ 
 1. Local database ทำหน้าที่เก็บเนื้อหาเริ่มต้นและการเปลี่ยนแปลงเนื้อหาของไฟล์ (เช่น source code) ซึ่ง database นี้จะเก็บเฉพาะส่วนที่ถูกเปลี่ยนแปลง ซึ่งอาจจะเป็นการเพิ่มหรือลบเนื้อหาก็ได้ ดังนั้นถ้าจะดูว่าเนื่อหาจริงๆ ของไฟล์นั้นๆ คืออะไร ก็ต้องอาศัยการติดตามการเปลี่ยนแปลงทีละขั้นจนถึงจุดที่เรียกดูข้อมูลในไฟล์นั้นๆ 
 2. Staging area เป็นพื้นที่เก็บเนื้อหาที่จะนำไปเก็บใน database (ซึ่งก็คือความแตกต่างของเนื้อหาที่อยู่ใน database กับเนื้อหาที่อยู่ในไฟล์ที่ถูกบันทึกล่าสุดบน harddisk) 

ในโฟลเดอร์ที่เก็บโฟลเดอร์ .git จะเป็นพื้นที่ทำงาน (Working Area) ซึ่งใช้เป็นที่เก็บ source code หรือเอกสารที่ต้องการให้ git ติดตามการเปลี่ยนแปลง 
ไฟล์ทั้งหมดที่ถูกสั่งให้มีการติดตามโดย git จะถูกนำไปเปรียบเทียบกับไฟล์ที่อยู่ใน database ทุกครั้งที่ได้รับการบันทึกลงใน harddisk (ในส่วน Working Area)
อย่างไรก็ตาม เราสามารถเลือกได้ว่าให้ git ติดตามการเปลี่ยนแปลงของไฟล์ทั้ง folder หรือไม่สนใจไฟล์ใด หรือไฟล์ขนิดใด โดยเราจะเก็บชื่อไฟล์หรือรูปแบบ (spec) ของไฟล์ไว้ในเอกสารที่ชื่อว่า .gitignore หรือ .gitinclude



![image](./Pictures/gi-intro/Slide3.PNG)

รูปที่ 2

![image](./Pictures/gi-intro/Slide4.PNG)

รูปที่ 3

![image](./Pictures/gi-intro/Slide5.PNG)

รูปที่ 4

![image](./Pictures/gi-intro/Slide6.PNG)

รูปที่ 5
 
