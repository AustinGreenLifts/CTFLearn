1) The first thing I did upon acquiring the files for this CTF was look at the source code.
![image](https://github.com/AustinGreenLifts/CTFLearn/assets/155912182/d586fa79-3741-4274-946c-2021fef31197)

2) After looking at the code I tried a few things that proved to be rather futile attempts at a workaround. This included but was not limited to: utilizing exponents, trying operands, & attempting to utilize filler characters to cause an error.

3) Following my failed attempts at drawing an error message. I took another look at the code and noticed that n was defined as an int variable in C. I took to google to see if int variables in C have any thresholds and what the upper end of those parameters look like. That is where I was reminded of the obvious that "The value of INT_MAX is: INT_MAX = 2147483647 (for 32-bit Integers) INT_MAX = 9,223,372,036,854,775,807 (for 64-bit Integers)"

4) This lead me to my final step and the answer by inputting 2 values whose sum is greater than the 32 bit threshold can handle causing a buffer overflow.
![image](https://github.com/AustinGreenLifts/CTFLearn/assets/155912182/2f46770f-6f63-4b55-a446-b4b11b3c496c)
