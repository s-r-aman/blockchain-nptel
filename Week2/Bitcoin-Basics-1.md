# Bitcoin Basics - 1

A **decentralized** digital currency enables instant payments to anyone, anywhere in the world.

## Main Features

- Completely independent i.e. no single authority has control over it.
- Money transfer can be done at anytime to anywhere in the world, without any restrictions.
- Bitcoins regulates its money by technical concepts as we will see later.

## Creation of the Coin

- There must a limited amount of bitcoin at a time, as unlimited supply of them will decrease it's value. And any hacked or malicious coin needs to be rejected by the system.
- Bitcoins are generated during mining time i.e. a user discovers a new block.
- The rate of creation of the block is adjusted every 2016 blocks to aim for a constant week adjustment period of time.
- The bitcoins generated for every block creation reduces by 50% for every 210, 000 blocks or approximately 4 years i.e. the reward get lowered by 50% every 4 years.
- The theoretical limit of bitcoin is minutely less than **21 million.**
- So now the question arises that why will miners mine when they get reward less than the investment cost. Solution is **charge the transaction fee from the transaction maker**.

## Sending Payments

- Bitcoin uses **Public Key Cryptography** to make and verify digital signatures.
- Each persona have one or more addresses each with an associated pair of public and private key.
- If Alice wants to transfer some bitcoins to bob then
  - Alice can sign the transaction with her private key.
  - Anyone can verify the transaction with Alice's public key.
  - Alice gets bobs address  and adds it and amount on the transaction message.
  - Alice signs the transaction w/ her private key.
  - Alice then broadcasts that message on the bitcoin network.

## Double Spending

When same bitcoins are used for more than one transactions.

- In a centralized system, the banks prevents double spending.
- We use blockchain main features to prevent double spending.
- When the first transaction is made, the whole block is aware of the transaction.
- When someone tries to make the second transaction it fails, because everyone knows about the previous transaction and will be able to see malicious activity with the help of a concept called **Proof Of Work**.

## Bitcoin Anonymity

- Bitcoin is permission-less, you do not need to setup any “account”, or required any e-mail address, user name or password to login to the wallet.
- The public and the private keys do not need to be registered, the wallet can generate them for the users.
- The bitcoin address is used for transaction, not the user name or identity.
- A bitcoin address mathematically corresponds to a public key based on ECDSA – the digital signature algorithm used in bitcoin.
- Each person can have many such addresses, each with its own balance.

## Bitcoin Script

- A transaction has two things -
  - Sending: Out
  - Receiving: In
- We need to check if the in correctly claims the out.
- To do this a programming language is made called bitcoin scripts.
  - A list of instructions.
  - Describes the next person can gain access to the bitcoin, if that person wants to spend them.
- A Forth like language.
  - Designed by Charles Moore.
  - A procedural language with type checking.
  - Stack used for recursion subroutine.
  - Uses polish notation.