# Information

Files can always be changed in a secret way. Can you find the flag? `cat.jpg`

My initial thought was to perform the following steps:

1. Download the file and conduct some basic checks:
   - Use the `file` command to determine the file format.
   - Open the JPG file using the `eog` command to view it.

2. View the metadata using `exiftool`.
   - I discovered a suspicious license text.

3. Identify the cipher by using the [dcode.fr cipher analysis](https://www.dcode.fr/cipher-identifier) tool.
   - The analysis suggested a high probability that it may be a base64 encoded text.

4. Decrypt the suspected base64 encoded text and found the flag.

Answer: **picoCTF{the_m3tadata_1s_modified}**
