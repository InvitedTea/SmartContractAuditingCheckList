# Smart Contract Auditing CheckList


# Smart Contract Auditing Checklist

This checklist covers common vulnerabilities and issues to watch out for when conducting smart contract security audits. It compiles patterns seen in auditing contests and real-world assessments.

## Documentation

- [ ] Code commented clearly  
- [ ] Comments match implementation
- [ ] Natspec comments exist
- [ ] Design decisions explained

## General Code Quality

- [ ] Current Solidity version used
- [ ] Linter warnings addressed  
- [ ] Formatting consistent
- [ ] Code modularized into readable functions
- [ ] Follows standards like ERC20

## Functional Requirements

- [ ] Behaviors match specifications
- [ ] Inputs/outputs as expected
- [ ] Events emitted properly
- [ ] Tokens minted/burned correctly
- [ ] Arithmetic accurate

## Access Control

- [ ] Roles defined properly
- [ ] Role authorization checked
- [ ] Ownership transfers protected
- [ ] Visibility specifiers used correctly

## Input Validation

- [ ] Input types checked
- [ ] Input bounds checked
- [ ] Input encoding verified
- [ ] Proper handling of errors
- [ ] Front-running protection

## Security Against Attacks

- [ ] Reentrancy issues checked
- [ ] Checks for arithmetic under/overflow   
- [ ] Flash loan protections in place
- [ ] Block values validated
- [ ] Protection against malicious governance

## Smart Contract Integration

- [ ] Expected behavior with inherited contracts
- [ ] Proper handling of native token transfers   
- [ ] Risks from composability with untrusted contracts
- [ ] Checks on integrated contract integrity
