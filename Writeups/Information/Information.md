# title

### Information
- Author: SUSIE
- Classificatioin: Forensics, picoCTF-2021
- Difficulty: Easy
  
<br>

### Description and instructions:
* Files can always be changed in a secret way. Can you find the flag? cat.jpg

<br>

# Hints:
1. Look at the details of the file
2. Make sure to submit the flag as picoCTF{XXXXX}


<br>

# Solution:
1. When starting the challenge, the first thing I did was download the cat.jpg file onto the webshell. I did this by using the `wget` command followed by the link I got from right clicking on 'cat.jpg' and clicking copy
2. After downloading the file one thing I instinctively was to run `cat` cat.jpg. Note: The `cat` command is used to output the contents of a file and display them to a user. This however was not very helpful as I was met with the image below.
![image](https://github.com/user-attachments/assets/85365cf8-f36b-420b-b6a2-f03449c45e83)
   
4. If you cant understand what is shown in the image thats fine because it is not anything that made sense to me as it is just a bunch of characters and file data that is unreadable by us humans.
5. At this point I did a little research and came accross the `exiftool "File_Name" ` command which when ran will display the metadata of a file. When `exiftool cat.jpg` is ran this is the output that is returned.

![image](https://github.com/user-attachments/assets/9e905b1a-2dbd-406d-963c-7fc5192f254e)

6. When looking at the displayed metadate the Current IPTC Digest and Liscence rows stood out to me as they seemes like outliers compared to the rest of the displayed data.
7. Going back to do some more reasearch and according to iMDC, "IPTC is a popular photography metadata standard. It specifies the fields, properties, and structure of metadata in order to make it easier to manage and retrieve images."  https://imagemetadatachecker.com/knowledge-base/iptc-digest
8. Basesd on what I had read from iMDC and what I saw displayed by the `exiftool` command I made an educated guess that what I was looking at was somewhat normal for that type of metadata and decided to come back to it later if looking at the liscence did not pan out.
9. Going back to look at the liscence from the metadata I decided to make an assumption that it was some sort of encrypted string and started trying to figure out the best way to decrypt the string. As I was doing the challenge and as I do not have much expierence with these challenges, I reasoned that if trying to decrypt the string did not work I would at least come out with some knowledge of how to approach decrypting strings.
10. One of the methods I tried in the webshell was using the following commant. `echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d`
11. The `echo` command displays any following text out onto the screen, the `|` or pipe sends the output from the left side of the pipe and uses it as input for the command on the right side. `base64 -d` decodes files into standard output.
12. Running this command with the string from the liscense row in turn will display the flag to the screen.
<br>

# Thoughts and conclusions:



<br>

# Flag: 
- picoCTF{the_m3tadata_1s_modified}


