# **Problem Statement**

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/3cfeb09681369c26e3f19d886bc1e5d9/values)

# Information

**Point Value:** 20 points

**Category:** Cryptography

# Hints

1. Bits are expensive, I used only a little bit over 100 to save money

# Solution

1. Use the following python script
    
    ```python
    from Crypto.Util.number import inverse, long_to_bytes
    
    c = 8533139361076999596208540806559574687666062896040360148742851107661304651861689
    n = 769457290801263793712740792519696786147248001937382943813345728685422050738403253
    e = 65537
    p = x
    q = x
    
    phi = (p-1)*(q-1)
    
    d = inverse(e, phi)
    
    m = pow(c,d,n)
    
    print(long_to_bytes(m))
    ```
    
2. For `p` and `q` , go to [factordb](http://factordb.com/)
3. Copy and paste the `n` value and then hit “Factorize”
4. The first value after the `=` is for `p` and the second value is for `q` . It will then look like this
    
    ```python
    from Crypto.Util.number import inverse, long_to_bytes
    
    c = 8533139361076999596208540806559574687666062896040360148742851107661304651861689
    n = 769457290801263793712740792519696786147248001937382943813345728685422050738403253
    e = 65537
    p = 1617549722683965197900599011412144490161
    q = 475693130177488446807040098678772442581573
    
    phi = (p-1)*(q-1)
    
    d = inverse(e, phi)
    
    m = pow(c,d,n)
    
    print(long_to_bytes(m))
    ```
    
5. Once you execute, you will get your flag

# Flag

picoCTF{sma11_N_n0_g0od_45369387}
