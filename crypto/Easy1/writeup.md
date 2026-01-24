# Easy1 Quick Writeup

1. Recognize the first part of the ciphertext (up to the '=') is a base64 string, so throw that into cyberchef to get the plaintext: GUELPHcss is the best club ever ;) polyalphabetic ciphers are also the best. This seems to be a hint.

2. What is a polyalphabetic cipher? A google search reveals that it is a type of cipher which uses multiple alphabets instead of just one. The same google search shows us that some of the most common/widely known polyalphabetic ciphers. We will try the vigenere cipher which seems to be a well known one.

3. Upon placing the second part of the cipher text (after the '='), and adding the vigenere decode operation to the cyberchef recipe, we see that it asks for a key. 

4. Thinking back to the decoded base64 ciphertext, GUELPH was the only part of the ciphertext that was capitalized. Let's try that as the key.

5. Entering GUELPH as the key gives us the flag! 

### gcssCTF{vigenere_is_c00l}
