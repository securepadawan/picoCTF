# **Problem Statement**

Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py) using [this password](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt) to get [the flag](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en)?

# Information

**Point Value:** 10 points

**Category:** General Skills

# Hints

1. Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py`
2. `$ man python`

# Solution

## picoCTF Webshell

1. Run `$ wget` for all three files
    - `$ wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py`
    - `$ wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt`
    - `$ wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en`
2. When checking the permissions (`ls -lath`) you can see you don’t have authorization to execute. So you need to change the permissions by running `chmod +x ende.py`
3. Since it is a python file, you need to run `vi [endo.py](http://endo.py)` and then add `#!/usr/bin/python`  to the file. Then exit vi by hitting ESC `:wq`
4. Execute file `./ende.py`
5. It prompts to use (-e/-d). This means to encrypt or decrypt. We want to decrypt, so type `./ende.py -d flag.txt.en` 
6. It will then prompt for the password (from the pw.txt file): `67c6cc9667c6cc9667c6cc9667c6cc96`
    - Just download the file and open using notepad / notepad++ / Visual Studio Code / etc.
7. Then it will output the flag.

## mac0S Terminal

1. Download all three files to the same location. I just left the files in the downloads directory.
2. Open terminal
3. Go to the downloads directory `cd downloads`
4. Run `python3 [ende.py](http://ende.py) -d flag.txt.en`
5. It will then prompt for the password. Open the `pw.txt` file and copy the password `67c6cc9667c6cc9667c6cc9667c6cc96` and execute.
6. Then it will output the flag.

# Flag

picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}
