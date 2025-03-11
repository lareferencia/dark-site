---
layout: post
title:  "Architecture and Components"  
date:   2024-02-01 00:00:00 +0200  
description:  "Architecture and Components"  
language: en  
language_reference: architecture
categories: post
published: true
---

The dARK system architecture is designed with a clear separation of components, organized into the Service Layer and the Core Layer.

<img src="{{ site.baseurl }}/assets/img/architecture.png"/>

### Service Layer

The Service Layer provides essential services that interface with the Core Layer components. These services include:

- **dARK Resolver**: Integrated with the global nt2.info resolver system, enabling persistent identifier resolution
- **dARK Minter**: Used to create and register new PIDs in the system
- **dARK Dashboard**: Provides monitoring and administrative capabilities for the platform
- **dARK API**: Facilitates communication between applications and the underlying blockchain
- **dARK Backup**: Ensures data durability and system reliability

These services are supported by load balancing mechanisms to ensure high availability and optimal system performance.

### Core Layer (dARK dApp)

The Core Layer is built on a permissioned blockchain network that forms the backbone of the dARK system. At its heart is a public permissioned network operating on a Proof of Authority (PoA) consensus mechanism, providing both security and efficiency for PID management.

The network leverages <a href="https://besu.hyperledger.org/" target="_blank">Hyperledger Besu</a> technology to provide a secure and efficient blockchain foundation. Hyperledger Besu is an Ethereum client designed for enterprise use that supports both public and private permissioned network deployments. Its implementation of the Ethereum Virtual Machine (EVM) allows for sophisticated smart contracts that manage PID operations with full transparency and auditability.

Designed with resilience and reliability as core principles, the architecture begins with a Minimum Viable dARK Network (MVDN). This network consists of essential blockchain nodes that provide the fundamental functionality required for system operation. These nodes manage RPC/API communications and maintain the distributed ledger of persistent identifiers. Each full node implements API endpoints for external service interaction through load balancing.

To guarantee continuous operation even during node failures, the architecture incorporates fault-tolerant redundancy through backup nodes and data replication systems. This distributed approach ensures that no single point of failure can compromise the integrity or availability of the PID infrastructure.

At the application layer, the dARK dApp delivers the central functionality for managing persistent identifiers through smart contracts. This application logic handles the creation, updating, and resolution of PIDs while enforcing governance rules defined by the network participants.

<div class="architecture-details">
  <div class="detail-box">
    <h4>Federated Infrastructure</h4>
    <p>The architecture supports multiple independent blockchain networks operated by different authorities, creating a truly federated PID infrastructure.</p>
  </div>
  
  <div class="detail-box">
    <h4>Scalable Design</h4>
    <p>The system can scale horizontally by adding more nodes to the network, ensuring high performance even with increasing numbers of PIDs.</p>
  </div>
  
  <div class="detail-box">
    <h4>Future Extensions</h4>
    <p>The modular design enables future incorporation of additional storage solutions like IPFS for larger metadata payloads, while maintaining data integrity through on-chain cryptographic verification.</p>
  </div>
</div>

<style>
  .architecture-details {
    display: flex;
    flex-wrap: wrap;
    gap: 1.5rem;
    margin-top: 2rem;
  }
  
  .detail-box {
    flex: 1;
    min-width: 250px;
    padding: 1.5rem;
    background-color: #f9f9f9;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  }
  
  .detail-box h4 {
    color: #8A3691;
    margin-top: 0;
    margin-bottom: 0.75rem;
  }
  
  @media (max-width: 768px) {
    .architecture-details {
      flex-direction: column;
    }
  }
</style>





