# Red

# Approach

The image looked  completely red so there was not much useful information from just looking at it.

I first checked the file and its metadata. The metadata contained a poem. After analysing i understood that we had to take  the first letter of each line.


CHECKLSB

This suggested that the flag was hidden using the least significant bits of the image pixels.(took help from ai)

# Solution

I checked the image as an RGBA image and extracted the least significant bit from each channel.

The basic idea was to get the data by putting the image on online tools to get lsb info about it
I used APERI'SOLVE.com to get 

This produced a Base64 string:
cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==

I decoded it by just putting it in a decoder and out then was the flag itself
# Flag


picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}

# Takeaway

If an image looks empty or uniform, check its metadata first and look for LSB steganography when the file gives a clue like CHECKLSB.

# AI Help

I used AI to understand how LSB steganography works and how to extract the least significant bits from the RGBA channels. I also used it to understand how the metadata clue pointed towards LSB extraction. After checking the steps myself, I understood that the hidden bits form bytes, which in this challenge produce a Base64 string that has to be decoded to get the flag.