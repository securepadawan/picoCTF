# **Problem Statement**

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm) has extraordinarily helpful information...

# Information

**Point Value:** 10 points

**Category:** General Skills

# Hints

1. This program will only work in the webshell or another Linux computer.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm`
3. Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
4. h and --help are the most common arguments to give to programs to get more information from them!
5. Not every program implements help features like -h and --help.

# Solution

## picoCTF Webshell

1. Run `$ wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm`
2. Need to change permissions to be able to execute “program”. `$ chmod +x warm`
3.  Execute “program”. `./warm` It will then display the following: `Hello user! Pass me a -h to learn what I can do!`
4. Run `/.warm -h`
5. It will then output the flag

## mac0S

1. When opening the “program” it opens in TextEdit
2. Do a find and search for `pico`
3. Once found, this is the flag

# Flag

picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
