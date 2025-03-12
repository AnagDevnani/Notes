# Introduction
refers to the delivery of computing services from a remote location.

It is Internet based computing, whereby shared resources, software and information are provided to computers and other devices on demand.

Characteristics
1. On demand self-service: users are able to provision, monitor and manage computing resources as needed without the help of human administrators
2. Broad network access: Computing services are delivered over standard networks and heterogenous devices.
3. Rapid elasticity: IT resources are able to scale out and in quickly and on as needed basis.
4. Resource pooling; IT resources are shared accross multiple applications and tenants in a non-dedicated manner.
5. Measured service: IT resource utilization is tracked for each application and tenant, typically for public cloud billing or private cloud chargeback.

The client consist of hardware and software that access the cloud services.
The client can be a Thick or Thin client.

Thick client refers to a fully functional computer on each desk whereas a Thin client refers to a machine which provides just the functionality needed to accomplish the necessary tasks.


## Cloud Services
1. Software as a Service (SaaS):
	- Complete application is offered to the customer, as a service or on demand.
	- No need to worry about installation, setup and running of application, service provider will do that for you. You just have to pay and use it through some client.
2. Platform as a Services (PaaS):
	- Development environement is offered as a service upon which other higher levels of service can be built.
	- Provides the computing platforms which typically include the operating system, programming language execution environment, database, web server and so forth.
3. Infrastructure as a Service (IaaS):
	- Provides basic storage and computing capabilities as standardized services over the network.
	- IaaS provides the computing infrastructure, physical or virtual machines like servers, and other resources like virtual-machine disk image library, block and file based storage, firewalls, load balancers, IP addresses, virtual local area networks and so on.
	- The customer would typically deploy his own software on the infrastructure.

|Type|Description|Examples|
|:---:|---|---|
|**Saas**| Highly scalable internet based applications are hosted on the cloud and offered as services to the end user|Google Docs, acrobat.com|
|**PaaS**|Here, the platforms used to design, develop, build and test applications are provided by the cloud infrastructure.|Azure Service Platform, Google App Engine|
|**IaaS**|In this pay per use model, services like storage, database management and compute capabilities are offered on demand.|Amazon Web Services, 3 Tera, GoGrid|

# Blockchain Technology
- Blockchain technology is a decentralized, digitized, distributed public ledger of each of the online transactions (mostly financial, but not always) across a peer-to-peer (P2P) network.
- Block refers to a secured data chunk that stores encrypted details of a valid transaction that has occurred online. A block consists of 2 parts:
	- Header: which is public to all
	- Private details of the transaction, accesible only to the owner of the block.
- Blockchain is the group of linked blocks which are related to each other and are in a proper, linear chronological order. It stores the complete trail of transactions.
- Public Ledger: all confirmed transactions' linked blocks since the first transaction are available in the form of a blockchain called public ledger.
- Mining: it is the process of confirming a transaction after validation, and adding it to the public ledger.

## How it works
A block is a secure data chunk storing encrypted details (using cryptography) of a valid transaction. A block is created when a user initiates a transaction. It stores the encrypted details of the transaction taking place.

A block gets connected with blockchain as a permanent database only after validation. A blockchain contains numerous linked blocks which are related to each other in a proper, linear, chronological order.

Each block contains a hash of the previous block. Hashing is a strong encrypting mechanism. Hashing not only encrypts, it makes forgery impossible becuase hashing cannot be reversed. Thus, a blockchain has complete information about different user addresses as well as their right from the origins set to the very recent completed block. Every node of the P2P network has access to the blockchain.

The blockchain technology ensures that all the transactions are always available since its creation and no transaction can be deleted.

Blockchain is the underlying technology of cryptocurrency.

Benefits of Blockchain Technology:
- Increased time effectiveness due to real time transactions
- Direct transactions eliminate the overheads and intermediary costs.
- Reduced risks related to cybercrimes, frauds and tampering.
- More transparent processes with a proper record creation and tracking.
- Highly secure due to cryptographic and decentralized blockchain protocols.

Blockchains can be of these types:
- Consortium Blockchains - Consensus process is controlled by a pre-selected group.
- Semi-private Blockchains - Semi-private blockchains are run by a single company that grants access to any user who satisfies a pre-established criteria.
- Private blockchains - Controlled by a single organization that determines who can read it, submit transactions to it, and participate in the consensus process.
- Public blockchains - Anyone can read a public blockchain, send transactions to it, or participate in the consensus process. They are considred to be "permissionless". Every transaction is public, and users can remain anonymous.