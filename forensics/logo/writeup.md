# Logo Quick Writeup

1. We are given an image of the GCSS logo (beautiful) and a text file saying that there's something hidden in the image. We open the image and it's pretty low res, so nothing really to analyse here.

2. Let's try strings on the image. We find a comment, mocking our attempts at using strings. Alright. 

3. Since there is a comment, we know the metadata of the image must have been altered. Let's check if we can find anything else in the metadata using a tool: exiftool gcss.jpg

4. We see a bunch of fields but one stands out immediately, "XP Comment". It's a very long base64 encoded string (ends in '='). Back to cyberchef. We paste this in and use the from base64 operation. Yet again it seems we are mocked, however we are given a password. Where can we use it?

5. The intro.txt file tells us that there is something hidden in the image. This is a technique called steganography, in which data is hidden inside of an image. We can use a tool called steghide to extract this information, and coincidentally, steghide allows us to use a password to embed/extract hidden data. 

6. We use the command steghide --extract -sf gcss.jpg and it prompts us for a password. Let's enter the password we found after decoding the base64 string.

7. A text file called flag.txt was extracted and placed in our current directory! Surely we've found the flag! 

8. Upon using cat on the flag, it seems like we have not found the flag yet. But we are close. The file contains a bunch of 2 character 'groupings'. This looks an awful lot like hexadecimal. Let's go back to cyberchef, paste the contents of flag.txt, and use the from hex operation.

9. This gives us the flag!!

Once again, follow the steps to find the flag ;) You'll know when you see it! 
