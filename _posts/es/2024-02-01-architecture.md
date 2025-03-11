---
layout: post
title:  "Architecture and Components"  
date:   2024-02-01 00:00:00 +0200  
description:  "Architecture and Components"  
language: es
language_reference: architecture
categories: post
published: true
---


The dARK system architecture is designed with a clear separation of components, organized into the Service Layer and the Core Layer.

<img src="{{ site.baseurl }}/assets/img/architecture.png" alt="dARK Architecture Diagram" class="img-fluid mb-4" />

<h2 class="custom-heading">Service Layer</h2>

The Service Layer provides essential services that interface with the Core Layer components. These services include:

| Service | Description |
|---------|-------------|
| **dARK Resolver** | Integrated with the global nt2.info resolver system, enabling persistent identifier resolution |
| **dARK Minter** | Used to create and register new PIDs in the system |
| **dARK Dashboard** | Provides monitoring and administrative capabilities for the platform |
| **dARK API** | Facilitates communication between applications and the underlying blockchain |
| **dARK Backup** | Ensures data durability and system reliability |

These services are supported by load balancing mechanisms to ensure high availability and optimal system performance.

<h2 class="custom-heading">Core Layer (dARK dApp)</h2>

The Core Layer is built on a permissioned blockchain network that forms the backbone of the dARK system. At its heart is a public permissioned network operating on a Proof of Authority (PoA) consensus mechanism, providing both security and efficiency for PID management.

<h3 class="custom-heading-secondary">Blockchain Foundation</h3>

The network leverages <a href="https://besu.hyperledger.org/" target="_blank">Hyperledger Besu</a> technology to provide a secure and efficient blockchain foundation. Hyperledger Besu is an Ethereum client designed for enterprise use that supports both public and private permissioned network deployments. Its implementation of the Ethereum Virtual Machine (EVM) allows for sophisticated smart contracts that manage PID operations with full transparency and auditability.

<h3 class="custom-heading-secondary">Network Architecture</h3>

Designed with resilience and reliability as core principles, the architecture begins with a **Minimum Viable dARK Network (MVDN)**. This network consists of essential blockchain nodes that provide the fundamental functionality required for system operation. These nodes manage RPC/API communications and maintain the distributed ledger of persistent identifiers. Each full node implements API endpoints for external service interaction through load balancing.

To guarantee continuous operation even during node failures, the architecture incorporates fault-tolerant redundancy through backup nodes and data replication systems. This distributed approach ensures that no single point of failure can compromise the integrity or availability of the PID infrastructure.

<h3 class="custom-heading-secondary">Application Layer</h3>

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

<h2 class="custom-heading">Ecosystem Integration</h2>

The dARK system is designed to integrate seamlessly with the existing scholarly ecosystem, particularly with repository networks, diammond journals and metadata aggregators, following this initial workflow:

<div class="workflow-container">
  <div class="workflow-step">
    <div class="step-number">1</div>
    <div class="step-content">
      <h4>Metadata Harvesting</h4>
      <p>Aggregators regularly harvest metadata from institutional repositories, journals, and other content providers through standard protocols like OAI-PMH or custom APIs.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">2</div>
    <div class="step-content">
      <h4>PID Assignment</h4>
      <p>For content without persistent identifiers, the aggregator can request new ARKs through the dARK Minter API. For existing ARKs, they are validated and registered in the dARK system.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">3</div>
    <div class="step-content">
      <h4>Blockchain Registration</h4>
      <p>The dARK system records each ARK on the blockchain, along with its target URL and essential metadata, providing a decentralized, tamper-evident registry of identifiers.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">4</div>
    <div class="step-content">
      <h4>PID Distribution</h4>
      <p>The newly minted or validated ARKs can be sent back to repositories for inclusion in their metadata records, enabling a standardized approach to persistent identification across the network.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">5</div>
    <div class="step-content">
      <h4>Resolution</h4>
      <p>When a user accesses an ARK, the global resolver redirects to the dARK resolver, which uses the blockchain to retrieve the current location information, ensuring persistent access even when resource locations change.</p>
    </div>
  </div>
</div>

This integration approach enables metadata aggregators like LA Referencia to enhance their services with decentralized PID infrastructure while preserving existing workflows and adding value to the repository network as a whole. It also allows for seamless transitions when repositories move content or change platforms, as the PID resolution system can be updated without breaking external links.

<div class="note-container">
  <div class="note-header">
    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#8A3691" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <circle cx="12" cy="12" r="10"></circle>
      <line x1="12" y1="8" x2="12" y2="12"></line>
      <line x1="12" y1="16" x2="12.01" y2="16"></line>
    </svg>
    <h4>Future Development</h4>
  </div>
  <div class="note-content">
    <p>In the next development phases, the dARK project plans to:</p>
    <ul>
      <li>Transform this initial project (currently working in IBICT/Brazil) into a comprehensive regional service designed as a public infrastructure, following the principles established by LA Referencia</li>
      <li>Develop plugins for the most widely used repository and journal systems to facilitate seamless integration with the dARK infrastructure</li>
      <li>Implement decentralized metadata persistence to preserve bibliographic information and serve as a reliable data source for analytical systems like OpenAlex</li>
    </ul>
    <p>These enhancements will further strengthen the dARK ecosystem and expand its utility within the scholarly communication landscape across Latin America and beyond.</p>
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
  
  .custom-heading {
    font-size: 1.4rem;
    color: #8A3691;
    position: relative;
    margin-bottom: 1.5rem;
    padding-bottom: 0.5rem;
    font-weight: 600;
    border-bottom: 2px solid #eaeaea;
  }
  
  .custom-heading::after {
    content: "";
    position: absolute;
    bottom: -2px;
    left: 0;
    width: 60px;
    height: 2px;
    background-color: #8A3691;
  }
  
  .custom-heading-secondary {
    font-size: 1.2rem;
    color: #555;
    margin-top: 1.5rem;
    margin-bottom: 1rem;
    font-weight: 500;
  }
  
  @media (max-width: 768px) {
    .architecture-details {
      flex-direction: column;
    }
  }
  
  .workflow-container {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    margin: 2rem 0;
  }
  
  .workflow-step {
    display: flex;
    gap: 1rem;
    background-color: #f9f9f9;
    border-radius: 8px;
    padding: 1.5rem;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
    border-left: 3px solid #8A3691;
  }
  
  .step-number {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-color: #8A3691;
    color: white;
    font-weight: bold;
    font-size: 1.2rem;
    flex-shrink: 0;
  }
  
  .step-content {
    flex: 1;
  }
  
  .step-content h4 {
    color: #8A3691;
    margin-top: 0;
    margin-bottom: 0.75rem;
  }
  
  .step-content p {
    margin-bottom: 0;
  }
  
  @media (max-width: 768px) {
    .workflow-step {
      flex-direction: column;
    }
    
    .step-number {
      margin-bottom: 1rem;
    }
  }
  
  /* Note container styling */
  .note-container {
    margin: 2.5rem 0;
    background-color: #f8f9fe;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(138, 54, 145, 0.08);
    overflow: hidden;
    width: 100%;
    display: block;
  }
  
  .note-header {
    background-color: rgba(138, 54, 145, 0.07);
    padding: 1rem 1.5rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
    border-bottom: 1px solid rgba(138, 54, 145, 0.1);
    width: 100%;
    box-sizing: border-box;
  }
  
  .note-header h4 {
    color: #8A3691;
    margin: 0;
    font-size: 1.1rem;
    font-weight: 600;
    flex-grow: 1;
  }
  
  .note-content {
    padding: 1.25rem 1.5rem;
    width: 100%;
    display: block;
    box-sizing: border-box;
  }
  
  .note-container ul {
    padding-left: 1.5rem;
    margin-bottom: 1rem;
    width: 100%;
    box-sizing: border-box;
  }
  
  .note-container li {
    margin-bottom: 0.5rem;
    position: relative;
    width: 100%;
    box-sizing: border-box;
  }
  
  .note-container li::before {
    content: "";
    position: absolute;
    left: -1rem;
    top: 0.55rem;
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background-color: #8A3691;
  }
  
  .note-container p:last-child {
    margin-bottom: 0;
  }
  
  .note-container p {
    width: 100%;
    display: block;
    box-sizing: border-box;
  }
</style>





