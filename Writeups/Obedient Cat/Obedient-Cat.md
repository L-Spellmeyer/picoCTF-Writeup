# PicoCTF 2021 - Obedient Cat

### Information
- Author: SYREAL
- Classificatioin: **General Skills**
- Difficulty: **EASY** - 5 Points
  
<br>

### Description and instructions:
- This file has a flag in plain sight (aka "in-the-clear"). Download flag.

<br>

# Hints:
1. Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal
2. To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag
3. $ man cat

<br>

# Solution:
1. When starting the first thing you want to locate is the Webshell tab on the webpage, typically on the right side as shown in the image below. 

<img src="https://github.com/user-attachments/assets/893168f2-ad62-409a-9a9c-754253a6f004" alt="Alt Text" width="400" height="200">  

2. Next, use the `wget` command followed by the given link `https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag` The `wget` command will download the file specified and should be remembered as you go on to complete other challenges

<img src="https://github.com/user-attachments/assets/796f4a0d-d927-46b4-a104-a2937c76aceb" alt="Alt Text" width="700" height="200">

3. After the file is downloaded run the command `ls` which will display all files from directory that you are in. After running the command and the files in the directory note that one of the files is named "flag". Type `cat flag` in the webshell and hit enter. This will display the contents of the flag file which in this instance is the flag needed to complete the challenge.
 
<img src="https://github.com/user-attachments/assets/a3de9b8c-69bb-49f4-8065-4baec42d5980" alt="Alt Text" width="700" height="275">  


## Thoughts and conclusions:
- Take note that the command `wget _fileName_` as it may be useful in other challenges-

<br>

# Flag: 
- **picoCTF{s4n1ty_v3r1f13d_1a94e0f9}**


