# Basic Crypto Primitives - 1

## Basic cryptographic things behind the BC

- Cryptographically secured hash function
- Digital Signature
- Hash Function - Used to connect blocks.
- Digital Signature - Digitally sign document that no one can deny about own activities.
- Cryptographically Hash Function
  - Takes any string as an input (input M: The message);
  - Fixed size output (256 in Bitcoin).
  - Efficiently computable.

> Thing to note is that the resources used in knowing H(M) will not be great.

## Properties

- Collision free.
  - Two messages are different the digest will also be different.
- Hiding - Hide message (avalanche effect).
- Puzzle friendly - Very hard to crack.

## Collision

- Hash function are one way, that is, it is easy to find H(x) for a given x, but no deterministic algorithm can find x for a given H(x).
- It is difficult to find x and y, x ≠ y however H(x) = H(y).
- Difficult to find, not impossible.
- Try with randomly chosen inputs to find out a collision, but it takes too long.
- **Birthday paradox** -
  - Find a the probability that the n randomly chosen people some will have the same birthday.
  - Pigeonhole principle.
- If hash function produces produces n outputs, the number of hash outputs on a random inputs is 2<sup>n/2</sup> for probability for matching 2 inputs is 0.98.
- For 256 bit, we need 10<sup>28</sup> years.

## Data Hiding Property

The transaction details can be encoded as message then feed in hash function to get digest and saved along details. So if any detail changes the hash will change the hash, thus we can know that the details have been changed.

## Puzzle Friendly

- Z = H( M || K ), M and Z are known, then knowing K(Bitcoin mining) is difficult.
- Randomly searching is the best solution to go.

## Hash Function

- SHA 256 is used in bitcoin mining.
- Secured hash function 256 bits is full form of SHA 256.
- Part of SHA developed by NSA.

## SHA Algorithm Preprocessing

- Pad message such the message size is multiple of 512.
- Append the `1` at the end.
- Append `x` zero `k` is smallest non negative solution equation `1 + 1 + k ===448 mod 512`.
- Append the 64 bit block which is equal to the number 1 written in binary.
- Total length 512.
- Parse the message into N 512 block M', M<sup>2</sup>, MM<sup>2</sup>.
- Every 512 bits block is further divided into 32 bit sub block M<sub>0</sub><sup>'</sup>, M<sub>1</sub><sup>'</sup>.
- Sequential H<sup>i</sup> = H<sup>i-1</sup> + C<sub>M</sub><sup>i</sup>(H<sup>i-1</sup>). C is compression here.
