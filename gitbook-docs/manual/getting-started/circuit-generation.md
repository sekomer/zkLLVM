---
description: Generating circuit using zkLLVM
---

# Circuit Developer

Before progressing further, please ensure you have set up the [environment](../../guides/environment-setup.md) and followed the [installation](../../guides/installation.md) guide.



## Flow

### 1. Compile Circuit

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption><p>Compile Circuit</p></figcaption></figure>

A circuit developer writes his circuit in a high-level language of his choice (C++/Rust). This circuit is next compiled using the `clang` compiler generated by zkLLVM. This step outputs a `*ll` file, an intermediate representation of the circuit.

### 2. Publish Circuit (Proof Market)

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption><p>Publish Circuit</p></figcaption></figure>

The generated IR can be pushed to the proof market. This enables Proof requesters & generators to serve each other. The proof market project handles the process of publishing circuits.



### 3. Publish On chain verifiers (ex: EVM)

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>Publish Verifiers</p></figcaption></figure>

The circuit developer will also be generating smart contracts for the circuits they have created. This will enable on-chain verification of the proof. The smart contracts consist of gate representations of the circuit. These contracts work in conjunction with the `placeholder` proof validation smart contracts. The lorem-ipsum project handles the process to transpile the circuit into smart contracts.&#x20;

{% hint style="info" %}
EVM is one of the first supported protocols. The transpiler will be extended to generate verification in other VMs.
{% endhint %}














