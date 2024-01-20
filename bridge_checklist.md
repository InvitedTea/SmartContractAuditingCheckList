# Detailed Bridge Protocol Attack Checklist

- This list comes from [code4rena-2023-07-axelar](https://github.com/code-423n4/2023-07-axelar-findings/blob/main/report.md)


## High Severity Vulnerabilities

### Smart Contract Flaws
- **Automated Analysis**: Utilize automated tools to scan for common vulnerabilities like overflow/underflow, unchecked return values, and reentrancy.
- **Independent Audits**: Engage third-party security firms to perform independent audits of the smart contracts.

### External Contract Dependencies
- **Verification of Sources**: Ensure all external contracts or libraries are sourced from reputable and secure repositories.

## Medium Severity Vulnerabilities

### Transaction Limits
- **Limit Setting**: Implement configurable limits on transaction values and frequencies.
- **Monitoring and Alerts**: Set up monitoring for transactions that approach or exceed set limits.

### Input Validation
- **Sanitization**: Sanitize all user inputs to prevent injection attacks.
- **Type Checks**: Implement strict type checks to ensure only the intended data types are processed.

### Reentrancy Guards
- **Modifiers**: Use modifiers in smart contracts to prevent reentrant calls.
- **Checks-Effects-Interactions Pattern**: Follow the checks-effects-interactions pattern to avoid reentrancy vulnerabilities.

### Access Control
- **Role-Based Access**: Implement role-based access control to govern who can execute critical functions.
- **Multi-Signature Requirements**: Require multiple signatures for critical operations, especially fund transfers.

### Gas Limitations
- **Function Optimization**: Optimize contract functions for gas efficiency to prevent out-of-gas errors.
- **Gas Usage Monitoring**: Monitor gas usage of functions to identify potential denial-of-service vectors.

### Error Handling
- **Revert with Reasons**: Ensure functions revert transactions with clear error messages.
- **Fail-Safe Mechanisms**: Implement fail-safe mechanisms to handle unexpected states or errors gracefully.

### Upgradability Checks
- **Governance Control**: Establish a clear governance model for upgrades, with community involvement where applicable.
- **Upgrade Testing**: Thoroughly test all upgrades in a staged environment before deploying to the main network.

### Cross-Chain Communication
- **Validation of Data**: Implement robust validation mechanisms for all incoming cross-chain data.
- **Secured Communication Channels**: Use secure and authenticated channels for cross-chain communications.

### Oracles Reliability
- **Multiple Data Sources**: Use multiple independent oracles to mitigate the risk of relying on a single data source.
- **Oracle Monitoring**: Continuously monitor oracle performance and data accuracy.
