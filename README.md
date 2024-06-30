# ZK-SNARK
This project involves creating and verifying a zero-knowledge proof using Circom, a specialized language for writing arithmetic circuits, and deploying the verifier contract on the Ethereum Sepolia or Polygon Mumbai Testnet.

## Tools Used

- **Hardhat**: A development environment for Ethereum software.
- **Circom**: A specialized language for creating arithmetic circuits.
- **hardhat-circom**: A Hardhat plugin for integrating Circom with Hardhat projects.

## Project Rubric

To successfully complete the Final Challenge, your project should meet the following criteria:

1. **Write a Correct `circuit.circom` Implementation**: Develop a circuit using Circom that meets the project requirements.

2. **Compile the Circuit to Generate Circuit Intermediaries**: Use the Circom compiler to generate intermediate files necessary for proof generation.

3. **Generate a Proof Using Inputs A=0 and B=1**: Use the compiled circuit to generate a proof with the specified inputs.

4. **Deploy a Solidity Verifier to Sepolia or Mumbai Testnet**: Deploy the verifier contract generated from the Circom compilation process to either the Sepolia or Mumbai Testnet.

5. **Call the `verifyProof()` Method on the Verifier Contract and Assert Output is True**: Invoke the `verifyProof()` method on the deployed contract with the generated proof and ensure the output is `true`.

## Getting Started

### Prerequisites

- Node.js and npm installed
- Hardhat installed
- Circom installed
- Sepolia or Mumbai Testnet faucet for test Ether or MATIC

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/circom-circuit-verification-project.git
   cd circom-circuit-verification-project
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

### Usage

1. **Write the Circuit**: Implement your circuit logic in `circuit.circom`.
   
2. **Compile the Circuit**:
   ```sh
   npx hardhat circom:compile
   ```

3. **Generate Proof**:
   - Navigate to the `input.json` file and set `A=0` and `B=1`.
   - Generate the proof:
     ```sh
     npx hardhat circom:generate-proof
     ```

4. **Deploy Verifier Contract**:
   - Compile and deploy the verifier contract to Sepolia or Mumbai Testnet:
     ```sh
     npx hardhat run scripts/deployVerifier.js --network sepolia
     ```
     or
     ```sh
     npx hardhat run scripts/deployVerifier.js --network mumbai
     ```

5. **Verify Proof**:
   - Call the `verifyProof()` method on the deployed verifier contract using the generated proof and assert the output is `true`:
     ```sh
     npx hardhat run scripts/verifyProof.js --network sepolia
     ```
     or
     ```sh
     npx hardhat run scripts/verifyProof.js --network mumbai
     ```

## Scripts

- `scripts/deployVerifier.js`: Script to deploy the verifier contract.
- `scripts/verifyProof.js`: Script to verify the proof using the deployed verifier contract.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.

---

By following this guide, you will be able to create, deploy, and verify a zero-knowledge proof using Circom and Solidity. Enjoy building your project!
