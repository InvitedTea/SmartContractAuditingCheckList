# DEX Oracle Smart Contract Auditing Checklist

This is based on recent report on Code4Rena: https://github.com/code-423n4/2022-09-canto-findings/blob/main/report.md

Based on the specific vulnerabilities and risks identified in the provided report, this checklist is designed for auditing a DEX Oracle smart contract.

## High-Risk Findings

### [H-01] Hardcoded USD Pegs
- [ ] Ensure stablecoin pegs are not hardcoded.
- [ ] Implement dynamic pricing using reliable oracle sources (e.g., Chainlink, Band Protocol).

## Medium-Risk Findings

### [M-01] Unbounded Loop Length DOS
- [ ] Check for loops with variable length and implement gas optimizations.
- [ ] Modify `setPeriodSize` function to handle execution in multiple transactions to avoid gas limit issues.

### [M-02] Calculated `token0TVL` Zero Scenario
- [ ] Review arithmetic operations to prevent zero values in `token0TVL`.
- [ ] Adjust calculation to prevent division before multiplication.

### [M-03] Impersonation Risk with Token Names
- [ ] Use address-based verification for token identification.
- [ ] Implement address whitelisting in the constructor.

### [M-04] Period Size Not Updated on New Pair Creation
- [ ] Ensure period size updates consistently for all pairs, including newly created ones.

### [M-05] Error Handling in `getUnderlyingPrice`
- [ ] Implement error handling that returns 0 on error, aligning with expected behaviors.

### [M-06] Resilience Against Downtime
- [ ] Implement checks for significant downtime or inactivity.
- [ ] Consider tracking average duration of observations and flagging outliers.

## Low Risk and Non-Critical Issues

### General Code Quality and Optimization
- [ ] Address out-of-gas errors in loops, incorrect or misleading comments, and ordering of functions.
- [ ] Ensure adherence to style guides and best practices.
- [ ] Optimize for gas usage and efficiency.

### Error Handling and Edge Cases
- [ ] Check for zero denominators in calculations.
- [ ] Validate input variables to prevent unexpected failures.

### Documentation and Code Clarity
- [ ] Ensure all functions are well-documented.
- [ ] Maintain consistent comment spacing and location for readability.
