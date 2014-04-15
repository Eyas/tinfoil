Project Tinfoil
====

Tinfoil is a simple JS-based tool that encrypts a text string with a random one-time pad. Tinfoil allows a user to store sensitive information on untrusted cloud storage solutions by putting different pieces of information (e.g. the padded xor-ed content and the pad) on separate cloud services. The process can be repeated recursively to use any *n* cloud storage services. This workflow ensures that our sensitive information is not lost, yet minimizes its exposure.

Passwords, persistence, and trust
----

Recent exploits have once again made us worry about protecting our online identity and properties. Vulnerabilities and attacks could expose our e-mail addresses, and, at times, plain-text passwords to attackers. Password reuse exacerbates the problem, as exposed passwords can allow an attacker to unlock multiple accounts, many with potentially valuable information. Most secure and alternate passwords are often simple permutations and modifications of a common *base* password.

The solution to our security problems begins with reducing our password reuse to a minimum, and approaching a state where all of our passwords are unique. Remembering a wide array of unique passwords can be a difficult task for a human, and must require the help of an extra aide. Relying on software for this task works well for many, but others might not want to trust other software makers in producing secure, vulnerability-free code. Locally-stored files are scary, as losing a device leads to losing al of your valuable passwords. Cloud-stored files are also scary, as we are again entrusting one service provider to produce secure, vulnerability-free code.

*Enter "Tinfoil"*.  Tinfoil applies a secure one-time pad to a text file you wish to secure (say, a passwords text file). Producing two encoded strings that are completely useless on their own but, once joined together, gives back the original text file. This allows you to store the two strings on separate cloud storage solution. Therefore, if one of them is compromised, your data would still be safe. You can split each of the two resulting strings into more and more strings, thus potentially storing your passwords text file on many cloud storage services.

