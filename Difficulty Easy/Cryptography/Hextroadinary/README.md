1. This one took me a bit longer. I ran some test through CyberChef trying to find the right output for the flag and I could not get anything that looked promising.

2. I looked closer at the question later and realized that the name ROXy is a hint leading to XOR.

3. I had tried XORing the variables in CyberChef and I could not recieve the flag.

4. I finally decided to attempt XORing the variables in python. This gave me a string of numbers, but did not give the flag I was looking for. After some research on Google I discovered that python has the functionality of "hex()" that will convert the output into a string
with a proceeding 0x.

5. This lead me to my final attempt at running print (hex(0xc4115 ^ 0x4cf8)) and recieving my answer.
![image](https://github.com/user-attachments/assets/5ff99b61-6936-43c4-a937-16d48b674c23)
