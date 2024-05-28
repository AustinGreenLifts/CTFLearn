1) The first thing I did for this CTF was open the bof2 file in Visual Studio to take a look at what we are trying to accomplish. From here I saw we were going to need to call the win function so I wanted to try and get some more information on what the function was.
![image](https://github.com/AustinGreenLifts/CTFLearn/assets/155912182/534be0aa-7c3b-4368-a355-f79242de4885)

2) Next I dropped the server file into a HEX editor to look for anymore clues or information and I noticed the file started with ELF so I began to research what this meant.
![image](https://github.com/AustinGreenLifts/CTFLearn/assets/155912182/fa9b5d1d-adf8-44b8-b6da-bb0bbe96b327)

3) After learning what a .ELF file is and what they do I was lead to an online ELF file viewer and dropped the file into it.
![image](https://github.com/AustinGreenLifts/CTFLearn/assets/155912182/d10ebfd3-208b-4860-89bc-d3d212a053e9)

4) Following this, I now had the address I needed to redirect to. I created a short python script using some inspiration from other CTFs that would occupy the 60 previous bytes with my initials and then fill my address in for the last 4.
$ echo -e "$(python3 -c 'print("AG" * 30)')\x86\x85\x04\x08" | nc thekidofarcrania.com 4902
![image](https://github.com/AustinGreenLifts/CTFLearn/assets/155912182/4d5aeabb-5178-421c-ba22-ed24b247b794)
