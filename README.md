
# Analysis of DID Use Case

Let's look closely at one of the DID Use Cases.  Specifically, the second one,
[7.2 Life-long, recipient-managed Credentials (education)](https://w3c-ccg.github.io/did-use-cases/#life-long-recipient-managed-credentials-education).

We can simplify it to this simple scenario, consisting of two steps:

1. At time T1, Alice (A) graduates from University of Barcelona (B) 
2. At time T2, Alice attempts to convince Victor (V) of that fact.

The challenge is to develop technology which makes this cheap and
easy, secure against attack, and robust against possible types of
failure.  Ideally, the solution should handle problems that might
occur like:

* Decades go by and all the cryptosystems that were known at T1 have become easy to break
* At some point between T1 and T2, one of computing platforms used by A or B turns out to have an unpatched security hole, allowing private keys to be compromised, possibly without detection
* B ceases operation
* A wants to keep the identity of V secret from B
* A forgets her password
* A loses lose her possessions, such as secret codes or keystore device
* A moves to another country obtains entirely different legal identity documents
* A changes her name
* B discovers A cheated on exams and recinds A's diploma
* Mallory, a close associates of A, with technical sophistication and co-conspirators, wants to impersonate A to V.

### Conventional Solution

Here's how one might do this without DID technology, for contrast.

1. Victor requires from Alice proof of name (and birthdate, for disambiguation, for more secure applications).  This would typically be provided via government-issued identification, such as a passport.

2. Victor contacts B to confirm A's graduation status.  This might just mean looking for her name on a published list on B's website.  Or, if B does not want to make the list public, V could use a web form or API, or even making a telephone call.  In any case, he provides Alice name (and maybe birthdate), and is told whether she is a graduate.  V might do this anonymously or might need to authenticate himself in some way. He might need to agree to some terms-of-service.

Downsides:
* Fails if B shuts down without there being some alternative provider for this service (such as partner schools or the local government).
* Can be difficult to handle name change from A, or lack of government-issued ID for A
* Currently most people have no way to prove their name online, only in person

### High Tech Solutions

...
