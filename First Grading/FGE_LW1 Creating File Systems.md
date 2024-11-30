![image](https://github.com/user-attachments/assets/28a70ff1-0510-4705-b688-4b9f1779148b)


# SYSADM1 -- Introduction to File Systems in Windows and Linux

# Requirement: 

-   A virtual machine running Linux and Windows OS

# Instructions: 

**Part A: Windows File System**

1.  **Open File Explorer:** Click the File Explorer icon on your desktop
    or press the Windows key + E.

![image](https://github.com/user-attachments/assets/bc3b4da5-0c9d-401b-bb9f-f2508aa4c5ed)


2.  **Navigate to your Documents folder:** This is usually the default
    location for user files.

![image](https://github.com/user-attachments/assets/221e9bf6-21dc-4234-ab4e-8bbb3a08c3f6)


3.  **Create a new folder:** Right-click in an empty space, select
    \"New,\" then \"Folder.\" Name it \"Lab1_Windows.\"

![image](https://github.com/user-attachments/assets/5bccb8bf-c949-44f0-b7b7-37d115ac5856)


4.  **Create a text file:** Right-click in the \"Lab1_Windows\" folder,
    select \"New,\" then \"Text Document.\" Rename it to \"info.txt.\"

![image](https://github.com/user-attachments/assets/4aa02e8a-d6d0-4dfb-956a-d88e7f1b2c8b)


5.  **Open the text file:** Double-click the \"info.txt\" file to open
    it in Notepad.

![image](https://github.com/user-attachments/assets/af607ffa-5ba4-444b-88db-5407d03f3e4d)


6.  **Type some text:** Write a short paragraph about yourself or the
    purpose of the file.

![image](https://github.com/user-attachments/assets/c3742a8e-706e-4ee4-99ab-fd6fb3f3bd32)


7.  **Save the file:** Close the Notepad window and save the changes.
   ![image](https://github.com/user-attachments/assets/2e009f40-0bde-4a3b-9d0c-e1bd4cf18134)


8.  **Create a subfolder:** Create a new folder inside \"Lab1_Windows\"
    called \"Data.\"

![image](https://github.com/user-attachments/assets/fc4e8f34-8612-4474-9291-79183321a3dd)


9.  **Copy the text file:** Copy the \"info.txt\" file to the \"Data\"
    subfolder.

![image](https://github.com/user-attachments/assets/38abbd74-ad0e-4d2c-a026-f7f95d33f5bd)


10. **Rename the copied file:** Rename the copied file to \"data.txt.

![image](https://github.com/user-attachments/assets/a6c1e1df-739c-49c4-9e0c-74c31bdd793f)


11. Create a folder named \"LabFiles\" with subfolders for each file
    type. Use the internet for the resources of the files listed below.

![image](https://github.com/user-attachments/assets/8d45eb44-5ed2-4634-85ee-b4b6f86ac5e2)

> **LabFiles**

1.  **Text**

    1.  large_text.txt

    2.  small_text.txt

    3.  code.cpp

![image](https://github.com/user-attachments/assets/efeec972-ea04-47f5-8c31-05de0ab894ee)


2.  **Images**

    1.  image1.jpg

    2.  image2.png

    3.  image3.bmp

![image](https://github.com/user-attachments/assets/169f9815-1743-4951-805b-3df04acd67ec)


3.  **Audio**

    1.  song.mp3

    2.  speech.wav

![image](https://github.com/user-attachments/assets/0c97970a-8081-40b1-8ebd-1a49c247ae86)


4.  **Video**

    1.  clip.mp4

![image](https://github.com/user-attachments/assets/e8027056-b160-4132-a8ca-bb3c8baa82b3)


12. **Check file properties:** Right-click on the \"info.txt\" file and
    select \"Properties.\" Explore the General, Details, and Security
    tabs to understand file attributes like creation date, size, and
    read-only status.

![image](https://github.com/user-attachments/assets/0d5d874b-3e02-461f-b880-1a2bc1d270dc)

> **The creation date of the file depends on the time that it was
> created. Also, the size of the file depends on how many characters are
> inside the file. A read-only status on a.txt file means you can open
> and view the file but cannot make any changes to it. The difference
> between the General and Details tabs is that the detail tab has more
> specific data about the file, like the owner and the name of the
> computer.**

13. **Change file attributes:** Try changing the file attributes (e.g.,
    read-only, hidden) using the Properties dialog. Observe the changes
    in File Explorer.

![image](https://github.com/user-attachments/assets/2fa93977-7ef5-4a68-b159-bfc853f1127e)

> **When I click the hidden attribute, the file will vanish and if I
> click the read-only attribute, the file will restore.**

14. **Share the folder:** Right-click on the \"Lab1_Windows\" folder,
    select \"Properties,\" and then the \"Sharing\" tab. Share the
    folder with a specific user or group, setting appropriate
    permissions (e.g., Read, Write, Full control)

15. **Create an archive:** Use WinRAR or 7-Zip to create a compressed
    archive of the \"Lab1_Windows\" folder.

![image](https://github.com/user-attachments/assets/4c965a64-e6c2-4689-8a3a-100f261c84d4)



16. **Extract an archive:** Create a new folder, then extract the
    created archive into it.

Part B. Create a log report structure
![image](https://github.com/user-attachments/assets/ec65c86d-59a3-41cc-ace9-c5472595e882)


**LOG REPORT**
**PART B.1**


![image](https://github.com/user-attachments/assets/d20e4075-7acd-417a-bcba-814cf4c47435)![image](https://github.com/user-attachments/assets/2e9f44da-0723-4896-9515-9ca77e9c1118)



**PART B.2**

+-------+-------+-------+----------------+-------------+-------------+
| File  | File  | File  | Creation Date  | Modified    | Accessed    |
| Name  | Type  | Size  |                | Date        |             |
+=======+=======+=======+================+=============+=============+
| inf   | Text  | 323   | Thursday, ‎22   | Thursday,   | ‎Today, ‎22   |
| o.txt | Doc   | bytes | ‎August ‎2024,   | ‎22 ‎August   | ‎August      |
|       | ument | (323  |                | ‎2024,       | ‎2024, ‏‎41    |
|       |       | b     | ‏‎9:14:06 am     |             | minutes ago |
|       |       | ytes) |                | ‏‎9:14:06 am  |             |
+-------+-------+-------+----------------+-------------+-------------+
| dat   | Text  | 323   | ‎Thursday, ‎22   | Thursday,   | ‎Today, ‎22   |
| a.txt | Doc   | bytes | ‎August ‎2024,   | ‎22 ‎August   | ‎August      |
|       | ument | (323  | ‏‎9:16:56 am     | ‎2024,       | ‎2024, ‏‎44    |
|       |       | b     |                | ‏‎9:16:56 am  | minutes ago |
|       |       | ytes) |                |             |             |
+-------+-------+-------+----------------+-------------+-------------+
| larg  | Text  | 200   | Thursday, ‎22   | ‎Thursday,   | Today, ‎22   |
| e_tex | Doc   | MB    | ‎August ‎2024,   | ‎22 ‎August   | ‎August      |
| t.txt | ument | (2    | ‏‎8:36:38 am     | ‎2024,       | ‎2024, ‏‎2     |
|       |       | 09,71 |                | ‏‎8:36:38 am  | hours ago   |
|       |       | 5,205 |                |             |             |
|       |       | b     |                |             |             |
|       |       | ytes) |                |             |             |
+-------+-------+-------+----------------+-------------+-------------+
| smal  | Text  | 20.0  | Thursday, ‎22   | Thursday,   | Today, ‎22   |
| l_tex | Doc   | MB    | ‎August ‎2024,   | ‎22 ‎August   | ‎August      |
| t.txt | ument | (     | ‏‎8:37:32 am     | ‎2024,       | ‎2024, ‏‎2     |
|       |       | 20,97 |                | ‏‎8:37:32 am  | hours ago   |
|       |       | 1,548 |                |             |             |
|       |       | b     |                |             |             |
|       |       | ytes) |                |             |             |
+-------+-------+-------+----------------+-------------+-------------+
| cod   | C++   | 94    | ‎Thursday, ‎22   | ‎Thursday,   | ‎Today, ‎22   |
| e.cpp | S     | bytes | ‎August ‎2024,   | ‎22 ‎August   | ‎August      |
|       | ource | (94   | ‏‎8:38:54 am     | ‎2024,       | ‎2024, ‏‎2     |
|       | File  | b     |                | ‏‎8:38:54 am  | hours ago   |
|       |       | ytes) |                |             |             |
+-------+-------+-------+----------------+-------------+-------------+
| image | Imag  | 46.8  | Thursday, ‎22   | Thursday,   | Today, ‎22   |
| 1.jpg | e.jpg | KB    | ‎August ‎2024,   | ‎22 ‎August   | ‎August      |
|       | File  | (4    | ‏‎8:40:52 am     | ‎2024,       | ‎2024, ‏‎2     |
|       |       | 7,995 |                | ‏‎8:40:52 am  | hours ago   |
|       |       | b     |                |             |             |
|       |       | ytes) |                |             |             |
+-------+-------+-------+----------------+-------------+-------------+
| image | Imag  | 183   | ‎Thursday, ‎22   | ‎Thursday,   | ‎Today, ‎22   |
| 2.png | e.png | KB    | ‎August ‎2024,   | ‎22 ‎August   | ‎August      |
|       | file  | (18   | ‏‎8:46:16 am     | ‎2024,       | ‎2024, ‏‎2     |
|       |       | 7,935 |                | ‏‎8:46:16 am  | hours ago   |
|       |       | b     |                |             |             |
|       |       | ytes) |                |             |             |
+-------+-------+-------+----------------+-------------+-------------+
| image | Imag  | 1.56  | Thursday, ‎22   | ‎Thursday,   | ‎Today, ‎22   |
| 3.bmp | e.bmp | MB    | ‎August ‎2024,   | ‎22 ‎August   | ‎August      |
|       | file  | (1,63 | ‏‎8:49:12 am     | ‎2024,       | ‎2024, ‏‎2     |
|       |       | 8,538 |                | ‏‎8:49:12 am  | hours ago   |
|       |       | b     |                |             |             |
|       |       | ytes) |                |             |             |
+-------+-------+-------+----------------+-------------+-------------+
| son   | Audi  | 7.11  | ‎Thursday, ‎22   | Thursday,   | ‎Today, ‎22   |
| g.mp3 | o.mp3 | MB    | ‎August ‎2024,   | ‎22 ‎August   | ‎August      |
|       | file  | (7,46 | ‏‎8:52:20 am     | ‎2024,       | ‎2024, ‏‎2     |
|       |       | 0,397 |                | ‏‎8:52:20 am  | hours ago   |
|       |       | b     |                |             |             |
|       |       | ytes) |                |             |             |
+-------+-------+-------+----------------+-------------+-------------+
| speec | Audi  | 926   | ‎Thursday, ‎22   | ‎Thursday,   | Today, ‎22   |
| h.wav | o.wav | KB    | ‎August ‎2024,   | ‎22 ‎August   | ‎August      |
|       | file  | (94   | ‏‎8:55:24 am     | ‎2024,       | ‎2024, ‏‎2     |
|       |       | 8,290 |                | ‏‎8:55:24 am  | hours ago   |
|       |       | b     |                |             |             |
|       |       | ytes) |                |             |             |
+-------+-------+-------+----------------+-------------+-------------+
| cli   | Vide  | 3.87  | ‎Thursday, ‎22   | ‎Thursday,   | Today, ‎22   |
| p.mp4 | o.mp4 | MB    | ‎August ‎2024,   | ‎22 ‎August   | ‎August      |
|       | file  | (4,06 | ‏‎8:57:26 am     | ‎2024,       | ‎2024, ‏‎2     |
|       |       | 6,020 |                | ‏‎8:57:26 am  | hours ago   |
|       |       | b     |                |             |             |
|       |       | ytes) |                |             |             |
+-------+-------+-------+----------------+-------------+-------------+
