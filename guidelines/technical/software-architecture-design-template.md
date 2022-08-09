# Software Architecture Design Template

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL
      NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and
      "OPTIONAL" in this document are to be interpreted as described in
      [RFC 2119](https://www.ietf.org/rfc/rfc2119.txt).

## Introduction

The introduction should include the purpose and overview for this technical design. It should detail the problem and the reason for proposing a solution. This problem description should be centered on the user perspective. The problem description should be understandable to the layman.

Introduction should be 1-2 paragraphs, and should contain minimal technical terms.

### Introduction example:

This document describes design options for a protocol that allows for arbitrary cross-chain transactions. Developers looking to build a distributed application increasingly want to integrate their products with other aspects of the blockchain ecosystem. Users benefit from this, as it simplifies their process of interacting with multiple blockchain technologies.

Here, we present two design options for such a protocol. We propose the name to be “Cross-chain Transfer Protocol” (CTP).

## Terminology
All variables and unclear technical terms used should be defined in this section. Please note that you do not need to pre-emptively
list every technical term in this section. However, as you fill out this document, evaluate which terms may be unclear and add them to
this section with a brief definition. Additionally, a collaborator on this document may add terms to this list if they find that it may
benefit viewers of the document. The terminology list should include acronyms, mathematical symbols, and technical words or phrases.

### Terminology example:

| Term      | Definition |
| ----------- | ----------- |
| CTP      | Cross-chain Transfer Protocol       |
| Message center   | Smart contract for aggregating messages and scheduling them for delivery between blockchains        |
| $R_{x \rightarrow y}$   | Unidirectional relay that transfers messages from blockchain X to blockchain Y       |
| $B_k$   | Block header at height $k$       |

## Considerations

The considerations should include the assumptions that are made, and the constraints that are faced. There may be multiple different considerations. Considerations can include technical topics, user-experience topics, or other topics that the collaborators of this document view as pertinent to understanding the design selection process.

### Considerations example:

#### Relay

The relay delivers messages between blockchains. It is essential to the cross-chain transfer process. In this case it is important to consider the balance between responsibilities of the user and the abilities of the user to reliably execute complex actions. The two main considerations here are that the user should be the relay or that there should be a third party that manages a relay service.

#### Fee

In each step of the CTP process there are different services provided, some of which have implicit fees charged by the blockchain, and others that do not have implicit fees but may require explicitly defined fees to incentivize efficient operation.

An example of an implicit fee would be a transaction that occurs on the blockchain. Most blockchains charge some fee to process a transaction.

An example of a fee that may be explicitly defined would be a message delivery fee. Currently, there is no predefined cost for a relay to send a message from one blockchain to another. However, it should be considered whether a fee should be defined to incentivize the user or a third-party relay to operate efficiently with respect to time, robustness, and reliability.

## Designs

This section should contain proposed solutions. Each proposed solution should have its own design, defined in bold font. The steps of the proposed solution should be laid out in full sentences and should cover all major logically likely outcomes, including corner cases. If the proposed solution’s flow branches, all cases should be clearly defined and stepped through. The steps of the proposed solution should also be written as pseudocode when applicable.

### Designs example:

#### Cross-Chain Transfer Protocol Design A

Caller  performs a cross-chain transaction  to transfer amount  from source blockchain  to sink blockchain . Relay  updates the state of blockchain  on blockchain  in smart contract representing a light node...
##### Pseudocode of the cross-chain transfer protocol Design A

```python
def cross_chain_transfer_protocol(routes, from_address, to_address, amount):
	lock(from_address, amount)
	mint(routes, to_address, amount)
	…
```

##### Cross-Chain Transfer Protocol System Context Diagram
<img src="/assets/guidelines/architecture-diagrams/Whiteboard - Example C4 System Context Diagram.svg" width="300">

##### Cross-Chain Transfer Protocol Container Diagram
<img src="/assets/guidelines/architecture-diagrams/Whiteboard-Example-C4-Container-Diagram.svg" width="600">

##### Cross-Chain Transfer Protocol Component Diagram
<img src="/assets/guidelines/architecture-diagrams/Whiteboard - Example C4 Component Diagram.svg" width="600">

## Comparisons

Comparisons should be made between the designs laid out in the “Designs” section. Comparisons should be formatted in a table with the appropriate major design aspects represented by table columns.

### Comparisons example:

| Item      | Design A | Design B |
| ----------- | ----------- | ----------- |
| Scalability      | Medium <br> - Reliance on Relay | Good |
| Flexibility   | Poor <br> - Rigid connections       | Good |

## Discussions

Discussions are artifacts of the clarifying design points that should be left for other contributors, advisors, or general viewers to
gain context into the decision-making process. Discussions should take place on a Github Discussions topic. It is preferable to have one
Github Discussions topic per Technical Design Options document, but there may be additional side-topics if something specific is to be
discussed and it would be simpler to understand in its own topic. It is likely that certain editing or commenting parties will not
fully understand all of the technical designs presented in a Technical Design Options document. Please edit this document to present
a clearer understanding of the technical aspects of the design during the discussion process.
