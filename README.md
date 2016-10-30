#LAB01

##ผลการทดลอง

![](https://scontent.fbkk2-1.fna.fbcdn.net/v/t34.0-12/14877289_1118469081606675_1815150258_n.png?oh=b8ba0d69b1ac860f010c2c67e0cf381e&oe=5818047F)

###สรุปผลการทดลอง
         เมื่อทำตามขั้นตอนจากใบงานLAB-01แล้วนั้น ทำให้ผลที่ได้ออกมาคือ Massageboxที่แสดงผล 
	 Hello World! This is my first win32 program! และมีปุ่มให้กดโต้ตอบคือ ปุ่ม OK 
	 โดยเราสามารถเลือกเปลี่ยนปุ่มได้ ตามฟังห์ชันที่เราต้องการ เช่น หากใส่ปุ่ม MB_ICONERROR 
	 ก็จะแสดงผลเป็นเครื่องหมายวงกลมสีแดง มีกากบาทตรงกลาง นั่นหมายความถึง Error นั่นเอง
	 ทั้งนี้ผู้เขียนโปรแกรมสามารถที่จะเลือกฟังก์ชันดังกล่าวได้ตามความเหมาะสมกับการออกแบบโปรแกรมนั้นๆนั่นเอง

###ตอบคำถาม

1.นักศึกษาพบปัญหาในการคอมไพล์โปรแกรมหรือไม่ ถ้าเจอให้บอกที่ผิดและแนวทางการแก้ไข

ตอบ ไม่พบปัญหาในการคอมไพล์โปรแกรมค่ะ

2.ให้ทดลองแก้ไข  MessageBox(...)  โดยการเปลี่ยน  MB_OK  เป็นค่าอื่นๆ 

ตอบ 

>> MB_ICONWARNING <<


![](https://scontent.fbkk2-1.fna.fbcdn.net/v/t34.0-12/14826259_1118511578269092_210004818_n.png?oh=c9dab6f6f2a04ff73777db588521979c&oe=58184EC4)

ผลที่ได้ ^

--------------------------------------------------------------------------------------------------------------------

>> MB_YESNOCANCEL <<

![](https://scontent.fbkk2-1.fna.fbcdn.net/v/t34.0-12/14877080_1118523604934556_1524426563_n.png?oh=feb002486f387040f17fe643e22e9647&oe=58187711)

ผลที่ได้ ^

-----------------------------------------------------------------------------------------------------------------------

>> MB_RETRYCANCLE <<

![](https://scontent.fbkk2-1.fna.fbcdn.net/v/t34.0-12/14914571_1118518241601759_221078509_n.png?oh=23ec6e335295d472a96fe692e01954cf&oe=581805E4)

ผลที่ได้^
---------------------------------------------------------------------------------------------------------------------------
>> MB_YESNO <<

![](https://scontent.fbkk2-1.fna.fbcdn.net/v/t34.0-12/14826350_1118540541599529_419772629_n.png?oh=6db598f92b36e4f1560e792cbbda7958&oe=581859AB)

ผลที่ได้ ^

# ใบงานที่ 1 เรื่อง การเขียนโปรแกรม Win32 ด้วยภาษา C
##วัตถุประสงค์

1. เพื่อให้นักศึกษาสามารถบอกวิธีการเขียนโปรแกรมบน Windows ด้วยฟังก์ชัน Win32 API ได้
2. เพื่อให้นักศึกษาสามารถใช้เครื่องมือต่างๆ ในการสร้าง Application บน IDE ได้

##ลำดับการทดลอง

1. เรียกโปรแกรม Microsoft Visual Studio 
2. สร้าง Project ใหม่  โดยเลือกเมนู File >> New >> Project… (Ctrl+Shift+N) จะปรากฏหน้าต่าง New Project ดังรูปที่ 1 ให้ทำตามขั้นตอน 2.1 – 2.4
![](https://github.com/Desktop-Programming-Lab-2559/LAB-01/blob/master/imgs/pic1.png)
    2.1 ช่อง Templates: ให้เลือก Visual C++ และเลือกชนิด project เป็น Empty Project

    2.2 ช่อง Name: ให้ใส่ชื่อของ Project เป็น EasyWin32

    2.3 ช่อง Location: ให้เลือกตำแหน่งที่จะสร้าง Project

    2.4 ส่วนที่เหลือ ให้คงไว้ตามที่ปรากฏ กด OK 

3 เพิ่ม source code ให้กับ project โดยการเลือกเมนู PROJECT >> Add New Item…
   
    3.1 ตั้งชื่อไฟล์เป็น EasyMain.cpp
    3.2 กด Add เพื่อเพิ่มไฟล์


4 พิมพ์โปรแกรมดังต่อไปนี้ลงในไฟล์ EasyMain.cpp
 
```c 
#include <windows.h>

int WINAPI
WinMain(HINSTANCE hInst, HINSTANCE hPrev, LPSTR  lpCmdLine, int nCmdshow)
{
    MessageBox(NULL, "Hello World! This is my first win32 program!",
	"Lesson1", MB_OK);
    return 0;
}
```

**หมายเหตุ**
ใน Windows นั้น ฟังก์ชันแรกในโปรแกรมของเราที่จะถูกเรียกใช้คือ WinMain ต่างจากในภาษา C ที่ใช้ main()<br>
อ่านเพิ่มเติม 
* [WinMain entry point](https://msdn.microsoft.com/en-us/library/windows/desktop/ms633559(v=vs.85).aspx)
* [MessageBox](https://msdn.microsoft.com/en-us/library/windows/desktop/ms645505(v=vs.85).aspx)
* [HINSTANCE](https://msdn.microsoft.com/en-us/library/windows/desktop/aa383751(v=vs.85).aspx)

5 กดปุ่ม Ctrl+F5 เพื่อดูผลการทำงานของโปรแกรม

## บันทึกผลการทดลอง

 [ให้สรุปผลการทดลอง แล้ว commit changes จากนั้นให้ส่งไปที่ edmodo]
 เหตุผลที่ต้องแจ้ง เพราะส่วนใหญ่ไม่ได้ใช้ชื่อจริง + รหัสนักศึกษา ในการสมัคร github

## คำถาม 
1. นักศึกษาพบปัญหาในการคอมไพล์โปรแกรมหรือไม่ ถ้าเจอให้บอกที่ผิดและแนวทางการแก้ไข
2. ให้ทดลองแก้ไข <code> MessageBox(...) </code> โดยการเปลี่ยน <code> MB_OK </code> เป็นค่าอื่นๆ [ดูได้จากอ้างอิงตามลิงค์นี้](https://github.com/Desktop-Programming-Lab-2559/LAB-01/blob/master/message-box.md)

```c 
 	MessageBox(NULL, "Hello World! This is my first win32 program!", "Lesson1", MB_OK);
```
				


##[อ้างอิง](https://github.com/Desktop-Programming-Lab-2559/LAB-01/wiki/References)
WinMain (..), MessageBox(..) 
 
* [theForger's Win32 API Programming Tutorial](http://www.winprog.org/tutorial/start.html)
* [Win32 programming tutorials](http://www.win32developer.com/tutorial.shtm)

* [Building a Win32 App, Part 2: Windows and Messages](https://www.codementor.io/c_plus_plus/tutorial/build-win32-api-app-windows-messages-c-cpp-visual-studio)
