# **Problem Statement**

Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/a614a27d4cb251d04c7d2f3f3f76a965/cat.jpg)

# Information

**Point Value:** 10 points

**Category:** Forensics

# Hints

1. Look at the details of the file
2. Make sure to submit the flag as picoCTF{XXXXX}

# Solution

1. Upload the photo to a photo forensics site like [this](https://fotoforensics.com/) or [this](https://29a.ch/photo-forensics/)
    1. If using “FotoForensics” check under “XMP” → “License”
    2. If using “Forensically” check under “String Extraction” → “License rdf”
2. You should see the following `cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9`
3. This is Base64 format. Using a [Base64 decoder](https://www.base64decode.org/) you will get the flag.

# Flag

picoCTF{the_m3tadata_1s_modified}
