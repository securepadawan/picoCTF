# **Problem Statement**

There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 35652`, but it doesn't speak English...

# Information

**Point Value:** 15 points

**Category:** General Skills

# Hints

1. You can practice using netcat with this picoGym problem: [what's a netcat?](https://play.picoctf.org/practice/challenge/34)
2. You can practice reading and writing ASCII with this picoGym problem: [Let's Warm Up](https://play.picoctf.org/practice/challenge/22)

# Solution

## mac0S Terminal

1. Within terminal type `nc mercury.picoctf.net 35652`
2. It will then output the following numbers:
    - 112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 57 98 51 98 55 51 57 50 125 10
3. Two solution options:
    - Using an [ASCII decoder site](https://www.dcode.fr/ascii-code), you can input the list of numbers above to output the flag.
    - If you want to use a python script for this, use you can use the following:
    
    ```python
    nums = [112, 105, 99, 111, 67, 84, 70, 123, 103, 48, 48, 100, 95, 107, 49, 116, 116, 121, 33, 95, 110, 49, 99, 51, 95, 107, 49, 116, 116, 121, 33, 95, 57, 98, 55, 51, 57, 50, 125, 10]
    flag = ""
    for number in nums:
        flag += chr(number)
    print(flag)
    ```
    

# Flag

picoCTF{g00d_k1tty!_n1c3_k1tty!_9b3b7392}
