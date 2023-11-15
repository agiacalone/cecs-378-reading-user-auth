# CECS 378 Reading Assignment: User Authentication

### Assignment Description
Answer the following questions from the Chapter 3 reading from your text book. Be complete with your answers. You may work on these questions with one or two other partners, but *all* students must submit the document individually in their own repositories along with each student’s name documented with the submission.

1. What are the four means of authenticating a user’s identity?
2. What are two common techniques used to protect a password file? Briefly explain them.
3. List and briefly describe four common techniques for selecting or assigning passwords.
4. List and briefly describe the principal physical characteristics used for biometric identification.
5. Assume that passwords are selected from four-character combinations of 26 alphabetic char- acters. Assume that an adversary is able to attempt passwords at a rate of one per second.
	* Assuming no feedback to the adversary until each attempt has been completed, what is the expected time to discover the correct password
	* Assuming feedback to the adversary flagging an error as each incorrect character is entered, what is the expected time to discover the correct password?
6. Assume that passwords are limited to the use of the 95 printable ASCII characters and that all passwords are 10 characters in length. Assume a password cracker with an encryption rate of 6.4 million encryptions per second. How long will it take to test exhaustively all possible passwords on a UNIX system?
7. It was stated that the inclusion of the salt in the UNIX password scheme increases the difficulty of guessing by a factor of 4096. But the salt is stored in plaintext in the same entry as the corresponding ciphertext password. Therefore, those two characters are known to the attacker and need not be guessed. Why is it asserted that the salt increases security? Explain.
8. Using the previous question as a point of reference, wouldn’t it be possible to completely thwart all password crackers by dramatically increasing the salt size to, say, 24 or 48 bits? Explain.
9. Because of the known risks of the UNIX password system, the SunOS-4.0 documentation recommends that the password file be removed and replaced with a publicly readable file called /etc/publickey. An entry in the file for user A consists of a user’s identifier IDA, the user’s public key, PUa, and the corresponding private key PRa. This private key is encrypted using DES with a key derived from the user’s login password Pa. When A logs in, the system decrypts E(Pa,PRa) to obtain PRa.
(a) The system then verifies that Pa was correctly supplied. How? (b) How can an opponent attack this system?
10. Consider the Bloom filter discussed in Section 3.3 in your textbook (Password-Based Authen- tication). Define k = number of hash functions; N = number of bits in hash table; and D = number of words in dictionary.
(a) Show that the expected number of bits in the hash table that are equal to zero is expressed as φ = (1 − Nk )D
(b) Show that the probability that an input word, not in the dictionary, will be falsely accepted as being in the dictionary is P = (1 − φ)k
(c) Show that the preceding expression can be approximated as P ≈ (1 − e−kD/N )k  