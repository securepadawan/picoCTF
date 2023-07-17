# **Problem Statement**

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/fe16c756149cfa85f23e73cd9dbd6a25/Addadshashanammu.zip)

# Information

**Point Value:** 20 points

**Category:** General Skills

# Hints

1. After ‘unzip’ing, this problem can be solved with 11 button-presses...(mostly Tab)...

# Solution

## picoCTF Webshell

1. Run `wget https://mercury.picoctf.net/static/fe16c756149cfa85f23e73cd9dbd6a25/Addadshashanammu.zip`
2. `unzip Addadshashanammu.zip`
3. You then need to go directory to directory. Quickest way to this is to type `cd` spacebar tab. This will autofill the next directory name. After autofilling, hit enter.
4. Keep doing this until you are in the last directory. To confirm this type `ls` and hit enter
5. Type `./fang-of-haynekhtnamet` and it will display the flag

# Flag

picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}
