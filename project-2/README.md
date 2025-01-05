# Project 2 - RSA Encryption
# Description 
You are to write a program for managing RSA encryption, decryption, and key generation. Your program should be menu or command-line driven, and support the following functionality.
1. Create a private key, and save it to a file.
2. Create a public key from a private key, and save it to a file.
3. Load a key (public or private) from a file specified by the user.
4. Encrypt/decrypt a text file (using RSA) with the currently loaded key.
Note that the algorithms for encryption and decryption are the same; the effect depends only on which key you use (public or private).

# Key Files
You should support two types of key files: private ones containing n, d, p, and q, and public ones, where you only know n and e.\
I would suggest filenames of the form mykey.privk and mykey.pubk or something similar. You may choose your own file layout, but I would suggest including some text in the file so you can tell what is there.  

Let the user decide how many digits to make the primes. Your program should figure out what blocksize to use based on the length of n in the key. Blocks of ciphertext can be separated with spaces, newlines, or a special character (like '#'). You can decide which to use.  

Store all your text/numbers using base 36, which will allow you to convert plaintext directly as an integer (after spaces and punctuation are removed).

# Large Integer Packages
If you are programming in Java, use the java.math.BigInteger class - see http://docs.oracle.com/javase/1.5.0/docs/api/java/math/BigInteger.html.\

If you are programming in C++ or C, you can use the powerful GMP package (https://gmplib.org/manual/Integer-Functions.html#Integer-Functions). GMP is free to download and install, which you can do on your laptop if you don't want to use thomas.\

All of these packages support conversion to/from text strings in base 36, addition, subtraction, multiplication, division, modular exponentiation, and GCDs. The BigInteger package has modular inverses (for computing d) and prime testing, as does GMP.

# Hand In 
Turn in a listing of your source code, and some sample plaintext, ciphertext, and key text files. Be sure to include comments!