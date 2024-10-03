# PicoCTF 2021 - Obedient Cat

### Information
- Author: SYREAL
- Classificatioin: **General Skills**
- Difficulty: **EASY** - 5 Points
  
### Description and instructions:
- This file has a flag in plain sight (aka "in-the-clear"). Download flag.

<br>

# Hints:
1. Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal
2. To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag
3. $ man cat

<br>

# Walkthrough:
1. **First** locate the Webshell tab displayed on the side of your screen, typically on the right side as shown in the image below. 

<img src="https://github.com/user-attachments/assets/893168f2-ad62-409a-9a9c-754253a6f004" alt="Alt Text" width="400" height="200">  

2. **Next**, use the `wget` command followed by the given link `https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag` to download the file provided for the challenge. The `wget` command will any specified file onto the webshell and should be remembered as you go on to complete other challenges

<img src="https://github.com/user-attachments/assets/796f4a0d-d927-46b4-a104-a2937c76aceb" alt="Alt Text" width="700" height="200">

3. After the file is downloaded type `ls` and hit enter. This will display all files from the directory that you are currently in. After running the command and the files in the directory are displayed, note that one of the files is named "flag". Type `cat flag` in the webshell and hit enter. This command outputs the contents of the flag file which in turn leads to the flag you are looking for being displayed in the terminal
 
<img src="https://github.com/user-attachments/assets/a3de9b8c-69bb-49f4-8065-4baec42d5980" alt="Alt Text" width="700" height="275">  


## Thoughts and conclusions:
- `wget` is the command used to download files onto the webshell when completing challenges. Remember this as it may come in handy when completing other challenges in which you are provided file/s to start with.
- `ls` displays all contents of the current directory you are in
- `cat` followed by a file name will display the contents of that file

<br>

# Flag: 
- **picoCTF{s4n1ty_v3r1f13d_1a94e0f9}**


