# Stand-Alone Projects
## Manual RSA Encyption Decryption 
sp1.  Performing Manual RSA Encryption Decryption using Python and Mathematical Algorithms ( Python )

      Algorithm :
        1) p and q are two supposedly large prime numbers which are strictly private
        2) A value n is calculated. n = p x q. It is better to keep it private but this can be public as it is extremely difficult to find p and q based off of n.
        3) A value of phi(n) is calucluted (Euler's totient function) which equates to (p-1) x (q-1).
        4) The Public Key is then generated which should be a value that is strictly coprime to phi(n).
        5) The Private Key is then generated which should be the modular inverse of the Private Key. This is simply explain using this calculation:
            (publicKey * privateKey) % phi(n) = 1
        6) To Encrypt A Message
            i)  Encode the Message to its Unicode Character-wise (any other Encoding should work as long as its decoded properly)
            ii) for each character, take its power to publicKey and modulo it with n. cipherCharacter = (character ^ publicKey) % n
        7) To Decrypt A Cipher
            i)  for each character, take its power to the privateKey and modulo it with n. decryptedUnicode = (character ^ privateKey) % n
            ii) Decode the character from Unicode to its character equivalent.

## Path Finding using Dijkstra's Algorithm
sp2. Path Finder ( C++ )

      Procedure:
      1) The User is asked to create a mxn matrix of their choice of height and width.
      2) The user then selects a % of impassible objects inside the given map.
      3) This creates a map of paths and random numbers with -1 as an impassible block.
      4) The user is then asked to specify End Point and the Start Point. 
      5) From that the system uses dijkstra algorithm alongside a greedy approach to find the shortest path from the start to end point without crossing the impassible blocks
      
