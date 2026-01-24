# Checkerboard Quick Writeup

1. Open the ppm file if your computer supports it. There's nothing really to see here though.

2. Try strings on the file, (strings output-00.ppm).

3. We find a comment with a base64 looking cipher, but watch out because this one doesn't end in '=', which is to throw you off. 

4. After pasting the ciphertext into cyberchef, we find yet another flag looking format something{...} but rotated.

5. Let's try trusty ROT13 again. This gives us the flag with the default value of 13! 

### gcss{billions_must_steganography}
