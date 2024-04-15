# Blockchain-based Cybersecurity Solution

This Solidity smart contract implements a cybersecurity solution for reporting and analyzing security events within a private blockchain network.

## Description

The `Event` contract facilitates the reporting of security events by nodes within the private blockchain network. It allows nodes to create events and alerts, which are then distributed to all nodes for analysis. The contract includes functionality to set a threshold for the maximum number of events per node.

## Contract Details

- **Events**: Logs security events reported by nodes within the network.
- **Alerts**: Stores alerts generated based on the severity of security events.
- **Threshold**: Defines the maximum number of events per node before cycling begins.
- **Owner**: The address of the contract owner, who has permission to modify the threshold.

## Core Features

- **Event Reporting**: Nodes can create security events within the blockchain network.
- **Alert Generation**: Alerts are generated based on the severity of security events and distributed to all nodes.
- **Threshold Management**: The contract owner can set and modify the threshold for event cycling.

## Usage

1. **Event Creation**: Call the `createEvent` function to report security events within the network.
2. **Alert Generation**: Call the `createAlert` function to generate alerts based on security event severity.
3. **Threshold Management**: Call the `setThreshold` function to set or modify the maximum number of events per node.

### Example Usage

```solidity
// Deploy the contract with a threshold of 10 events per node
Event eventContract = new Event(10);

// Report a security event
eventContract.createEvent("Unauthorized access detected in network");

// Generate an alert for a high-risk event
eventContract.createAlert(Risk.HIGH, "Potential security breach detected");

// Modify the threshold for event cycling
eventContract.setThreshold(15);
