# vyper_arb_q3_2024_follow_up_questions
Follow Up Questions for the Vyper Arbitrum Grant



1. How does this compiler verification research differ from or improve upon existing methods in the field?

Compiler validation has been an active area of research in computer science for over half a century and different validation methods are used in practice by major compilers (cf. here for some examples for C++: https://github.com/MattPD/cpplinks/blob/master/compilers.correctness.md). Validation is particularly important for safety-critical applications in industries such as aerospace, automotive and medical software. While blockchain applications are also safety-critical, verification efforts have traditionally been focused on contracts rather than compilers. As a result there have only been limite efforts to ensure the correctness of EVM language compilers. Early formal verification attempts for Solidity have remained dormant (https://github.com/leonardoalt/ethereum_formal_verification_overview?tab=readme-ov-file). SpecTest (https://link.springer.com/chapter/10.1007/978-3-030-71500-7_14), a specification-based testing framework was applied to Solidity in 2020 and discovered several bugs by their authors, but does not seem to have been further integrated to keep up with the language's changes.

Our efforts aim at the implementation of state of the art methods that are already in use with other compilers and to adapt them to Vyper specifically. As Vyper now performs more optimizations than Solidity it also even more crucial to be able to ensure that these optimizations do not unexpectedly alter the compiled program's behavior.


2. What specific challenges do you anticipate in developing the definitional interpreter and program generator?

3. How will you ensure that the generated Vyper programs cover a wide range of possible contract structures and edge cases?

4. Can you provide more details on how the abstract analysis framework will be implemented and integrated into the existing Vyper toolchain?

5. How do you plan to measure and quantify the reduction in development cycle time and audit costs?

6. What is your strategy for disseminating the results of this research to the broader Ethereum development community?

- We are currently working to set up a blog for Vyper where we will report on our security work and research. 
- Academic publications?

7. Can you elaborate on how this research might influence or benefit other EVM-compatible languages and tools?

- Set a higher standard for verification among EVM-language compilers
- Share experience & code via our publications and public repositories to make it easy to reproduce the implemented methods on other codebases
- Raise more awareness about compiler internals and their role in blockchain safety
- Improve the security of all downstreams dAPP relying on Vyper contracts

