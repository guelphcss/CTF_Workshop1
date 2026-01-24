# Demo Quick Writeup

1. Recognize that the ciphertext ends in '=', so it may be base64.

2. Paste the ciphertext into cyberchef and use the from base64 operation.

3. We get something that looks kind of like a flag, with the ctf{...} format, but the letters seem to be rotated.

4. Let's try a simple rotation with the ROT13 operation. 

5. This gives us the flag, with a simple rotation of 13. Note that most challenges will not be this easy and have the rotation as the default value of 13.

### gcss{base64_rotated}

