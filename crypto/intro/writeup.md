# Intro Quick Writeup

1. Given ciphertext already looks to be in a flag format, yukkULX{...}, we can infer that the 2 k's could be s's and ULX could be CTF? so maybe flag format is gcssCTF{...}? We likely need to rotate some letters around to find something.

2. Let's try the ROT13 operation in cyberchef.

3. After brute forcing and trying some different values for the operation, we find that with a value of 8, we get the flag!

(also could use the ROT operation on dcode to test many values at once)

### gcssCTF{rotation_96}
