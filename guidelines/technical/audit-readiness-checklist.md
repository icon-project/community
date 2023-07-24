# Audit Readiness Checklist

This checklist provides an overview of the requirements that should be met before commissioning an audit for your project.

- [ ] **Documentation:** Describe the project's architecture, functionalities, technology stack, and design.
  - [ ] Create a state diagram defining every possible system state and state transitions.
  - [ ] Create a logical flowchart depicting how data moves, where it goes, and what happens to it at each step.
- [ ] **Internal Code Review:** Conduct an internal review of the project's codebase.
  - [ ] Conduct internal threat modeling and assess vulnerability to identify potential security risks.
  - [ ] Define the intended behavior of the critical components*, validate that the actual code aligns with the intended behavior, and document any discrepancies and improvements.
- [ ] **Guard Rails:** Implement throttling and temporary halts when predefined metrics exceed their thresholds in accordance with [EIP-7265](https://github.com/ethereum/EIPs/pull/7265). Note that EIP-7265 is subject to change.
- [ ] **Test Coverage:** Implement a minimum of 80% test coverage.
- [ ] **Adherence to [software development guidelines](https://github.com/icon-project/community/blob/main/guidelines/technical/software-development-guidelines.md)**

\* Critical components include but are limited to:
* exchange of value
  * transfer
  * transferFrom
  * send
  * call
  * delegatecall
  * selfdestruct
  * inline assembly code
* access control
  * onlyOwner or similar functions
* fallback
* external contract interactions
* state variable operations
