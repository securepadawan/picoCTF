# **Problem Statement**

I wonder what this really is... [enc](https://mercury.picoctf.net/static/dd6004f51362ff76f98cb8c699510f23/enc) `''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`

# Information

**Point Value:** 20 points

**Category:** Reverse Engineering

# Hints

1. You may find some decoders online

# Solution

1. Go to [CyberChef](https://gchq.github.io/CyberChef/)
2. Copy the contents from the “enc” file and input them.
3. Under the operations, search for “Text Encoding Bruce Force”
4. Drag and drop it into the “Recipe” section
5. The flag displays under output UTF-16BE (1201)

# Flag

picoCTF{16_bits_inst34d_of_8_0ddcd97a}
