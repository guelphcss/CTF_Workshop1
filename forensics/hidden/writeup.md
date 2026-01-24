# Hidden Quick Writeup

1. First, let's try opening the docx file, which is a Microsoft Word file. Upon opening it we dont really see anything apart from some text telling us the flag is not here. Not much else to see. Let's move on.

2. Next let's try using strings. Nothing really stands out except this string: "word/media/image1.png". There's an image in here somewhere...hmm.

3. Sometimes files can be embedded inside other files, so let's try to figure out how to extract it. We will use a tool called binwalk to find embedded files. 

4. We run the command 'binwalk -e definitely-doesnt-contain-the-flag.docx' (the -e option tells binwalk to extract any embedded files that it finds.

5. After extracting, a new directory with the extractions is created. Let's cd into it. Another directory '0', cd into it.

6. There are 4 items in the '0' directory. One is a directory called 'word', which matches the string we found in step 2. Let's cd into there. Now, we find another directory 'media', just like the string in step 2. Enter the media directory. We have found an image!

7. We open the image and find the flag!

I won't put the flag here, try to follow the steps and find it yourself ;)
