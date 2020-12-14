---
id: 838a176c-8ab1-469c-8407-4c68284388e4
title: Ethereum
desc: ''
updated: 1607629803286
created: 1607185174614
---

# Ethereum

```mermaid
flowchart TD
A[white paper 2013] --> B[Smart Contracts]
B --> C[ETH live 2015]
```

*Smart Contracts: code that lve on the Ethereum Blochchain

* Ethereum networks are used to transfer money and store data 
* There are many different Ethereum networks. 
* Networks are formed by one or more nodes. 
* Each node is a machine running an ethereuC2n client. 
* Anyone can run a node. 
* Each node can contain a full copy of the blockchain 
* The 'blockchain' is a database that stores a recl)rd of every transaction that has ever taken place

<details><summary>
How to work with ETHEREUM?
</summary>

![](/assets/images/2020-12-05-17-15-37.png)

---
</details>

<details><summary>
Rapsten, Kavan and Rinkeby are test networks (remote)
localhost 8545 is a local Node
</summary>

![](/assets/images/2020-12-05-17-25-49.png)
![](/assets/images/2020-12-05-17-48-34.png)

---
</details>


<details><summary>
What is a transaction?
</summary>

![](/assets/images/2020-12-06-16-49-27.png)
![](/assets/images/2020-12-06-16-45-52.png)

The transaction is then sent a particular node.
Our and Other people transaction: basically those transactions are assembled into a block. 
![](/assets/images/2020-12-06-16-53-07.png)
```mermaid
flowchart TD
A[transactions into a block] --> B[the Node start running some calculations on the block aka Mining]

```

---
</details>

<details><summary>
What are Smart Contracts and how we build them?
</summary>

![](/assets/images/2020-12-10-19-36-20.png)
---
Notice the difference from External and Contract Account
![](/assets/images/2020-12-10-19-37-11.png)
---
![](/assets/images/2020-12-10-19-38-11.png)
</details>

<details><summary>
What is Solidity?
</summary>

![](/assets/images/2020-12-10-19-44-52.png)
---
Solidity is not execute directly but...
![](/assets/images/2020-12-10-19-46-49.png)
---
Plus our extra JS code (plus html, css) will interact with ABI to understand the Bytecode:
![](/assets/images/2020-12-10-19-50-02.png)
</details>
