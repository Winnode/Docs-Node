<p align="center">
  <img height="350" height="350" src="https://private-user-images.githubusercontent.com/85368621/330419211-92fccc7f-d19c-43a1-b513-4118d4d79c53.jpg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTU2OTAxMzIsIm5iZiI6MTcxNTY4OTgzMiwicGF0aCI6Ii84NTM2ODYyMS8zMzA0MTkyMTEtOTJmY2NjN2YtZDE5Yy00M2ExLWI1MTMtNDExOGQ0ZDc5YzUzLmpwZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDA1MTQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwNTE0VDEyMzAzMlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWU5YTQ3NzViMDBhM2FhYWJkZGE0NjQ0Y2MyYjI1YmU1ODRlOWUwN2ExMjEzZTE0YjgxOWExMGJhNWMwNzRlZmQmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.U2MNgsK40X4JXwnm5EjEY3-vIDeryXgf45B3g8Nub4A">
</p>
<h1>
<p align="center"> 0G </p>
</h1>
0G System
Data availability problem stems from the demand for off-chain verification of executed states, which in turn arises from the trade-off between scalability and security of blockchain systems. The increasing prominence of Layer 2 networks and decentralized AI platforms has made the data availability even more crucial and also made its scalability the primary challenge at present.

ZeroGravity (0G in short) is the first data availability system with a built-in general purpose storage layer that is super scalable and decentralized. The scalability of 0G hinges on the idea of separating the workflow of data availability into data publishing lane and data storage lane. Large volume of data transfers happen on the data storage lane that is supported by the storage layer which achieves the horizontal scalability through well designed partitioning, while the data publishing lane guarantees the data availability property through consensus of data availability sampling which only requires tiny data flowing through the consensus protocol to avoid the broadcasting bottleneck. Data storage is an integral part of data availability because it must answer the question of where the data is published.

The ZeroGravity Data Availability (0G DA) system is a scalable Data Availability (DA) service layer which is directly built on top of a decentralized storage system and addresses the scalability issue by minimizing the data transfer volume required for broadcast. Its general decentralized storage design further enables it to support a variety of availability data types from diversified scenarios not limited to Layer 2 networks but also inclusion of decentralized AI infrastructures.

In informal terms, DA is a guarantee that a given piece of data is available to anyone who wishes to retrieve it. 0G DA is focused on providing DA with both high security and throughput.

At a high level, a DA system is one which accepts blobs of data via some interface and then makes them available to retrievers through another interface.

The storage layer of 0G consists of a storage network connecting with a separate consensus network. Each storage node actively participates a mining process by submitting the proof of accessibility for specific piece of data to the smart contract deployed on the consensus network. Once the proof is validated by the smart contract, the storage node gets rewarded accordingly. The partitioning is enabled through rewarding more to the node for storing the specific data that belong to the same partition with the node. This incentive-based mechanism rewards the nodes for contributions rather than punishing them for misbehaviors, so it can better encourage nodes to participate in the maintenance of the network, and hence can promote the network to achieve better scalability in practice. 0G storage is also designed as a general storage system with multiple stacks of abstractions and structures including an append-only log layer for archiving unstructured data and also a key-value layer for managing mutable and structured data. This allows 0G to support reliable data indexing and a greater variety of availability data types from Layer 2 and AI scenarios.
### Documentation
> - [Site](https://0g.ai/)
> - [X](https://twitter.com/0G_labs)
> - [Discord](https://discord.com/invite/0glabs)
> - [Github](https://github.com/0glabs)

### Minimum Hardware :
OS  | CPU     | RAM      | SSD     | 
| ------------- | ------------- | ------------- | -------- |
| Ubuntu 22.04 | 8          | 64         | 1 TB  | 

