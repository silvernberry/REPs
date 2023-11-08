---
layout: default
---

# Runtime Enhancement Proposals (REPs)

The [Runtime Enhancement Proposals (REPs)](https://reps.w3society.org) for Intra-Chain Network encompass critical aspects, including core functionalities, networking, consensus mechanisms, and all enhancements related to ICN node and global state. As the ICN operates on the Substrate Framework, it employs a forkless upgrade approach, where the runtime is directly updated through a specialized extrinsic transaction. Governance participants have the authority to accept or reject proposed runtime upgrades, which are detailed here as formal proposals.

## REP Status Terms

[![](https://mermaid.ink/img/pako:eNptUstOwzAQ_JVoz0mVV52SSEhAgVOhagviYQ4m2TaREjtynJZS9d_Z9CFKxc2zMzuzXnsDqcoQYpiXapXmQhuLy6b9XGhR59bkduw8LlEvC1ydlMU7EdbUCNM2HwmXQy3mhssbUZZcPiuDXN4VUpQdo-ojgTI7SC3H6Zyv0hRr4ziXVidI9q0dvFeUKYVMyej3TF2vHbuzTs6Yh47p0pJ9HMExonYmuJ_9BBA1xCWWqq5QGudak0XujNsmp_H-JzrzSStnRYVPNe0gw9kLl-cVUp1cntBfwXkDCUaiMTTXIWmEeoG7PYENFepKFBm9zIZLy-JgcqyQQ0zHDOeiLQ0HLrckFa1R07VMITa6RRvaOhMGh4WgmAriuSgbqtZCvilVHUUEId7AF8SsxxhzvYt-EHqB5_qRDWuIo0GPuZHXd0OXuf2LkG1t-N71ez03jCI_YJHPPL8_CEIbMCuM0qP9V9r9qO0P0dfL8A?type=png)](https://mermaid.live/edit#pako:eNptUstOwzAQ_JVoz0mVV52SSEhAgVOhagviYQ4m2TaREjtynJZS9d_Z9CFKxc2zMzuzXnsDqcoQYpiXapXmQhuLy6b9XGhR59bkduw8LlEvC1ydlMU7EdbUCNM2HwmXQy3mhssbUZZcPiuDXN4VUpQdo-ojgTI7SC3H6Zyv0hRr4ziXVidI9q0dvFeUKYVMyej3TF2vHbuzTs6Yh47p0pJ9HMExonYmuJ_9BBA1xCWWqq5QGudak0XujNsmp_H-JzrzSStnRYVPNe0gw9kLl-cVUp1cntBfwXkDCUaiMTTXIWmEeoG7PYENFepKFBm9zIZLy-JgcqyQQ0zHDOeiLQ0HLrckFa1R07VMITa6RRvaOhMGh4WgmAriuSgbqtZCvilVHUUEId7AF8SsxxhzvYt-EHqB5_qRDWuIo0GPuZHXd0OXuf2LkG1t-N71ez03jCI_YJHPPL8_CEIbMCuM0qP9V9r9qO0P0dfL8A)

### Draft

The "Draft" status is assigned by the REP author when merging their `rep-n.md` into the REPs repository. Following this, the repository maintainers will conduct a review to assess its formatting suitability. Once the submission meets the required criteria, it will be accepted, and its status will transition to "Call," initiating further peer-review and awaiting a vote.

### Call

Upon approval by the maintainers, the status of the new `rep-n.md` will be updated to "Call." This phase involves a peer-review process conducted by various voters and the general public. It precedes the REP becoming available for voting on potential amendments. The status will transition to "Vote" only when the author updates the runtime upgrade transaction hash, updates a development branch of the native source code, and confirms these changes with the maintainers.

### Vote

During the voting process, only one runtime upgrade transaction can be posted at a time, and it must adhere to the sequential order of REPs awaiting the "Call" status. Any parallel transactions will not be synchronized with the REPs flow, leading to automatic rejection by the voters. It is strongly discouraged to attempt such transactions, as they may result in unnecessary runtime upgrade transaction fees.

### Final

Upon the conclusion of the voting period with a decision to accept the runtime upgrade, nodes will execute a forkless upgrade. Subsequently, the maintainers will have the authority to change the REP's status to "Final."

### Drop

In the event of a vote against the runtime upgrade, the REP will be updated to "Drop," indicating that the upgrade will not proceed. In such cases, the author has the option to submit a new REP with an updated proposal, which may be more likely to be accepted by the voters.

## Guidelines for Preparing a Runtime Enhancement Proposal (REP) Submission

To facilitate a smooth and effective Runtime Enhancement Proposal (REP) submission process, please adhere to the following steps:

1. **Conceptualize and Engage in Discussion:** Initiate a discussion on the REPs repository's GitHub Discussions to introduce your proposal. Seek feedback and reviews, particularly if you have already laid out your research.

2. **Refine Your Proposal:** Incorporate feedback from the community to enhance your proposal. Make necessary adjustments to improve your ideas, findings, or algorithms.

3. **Implement Changes:** Create a fork of the ICN Node Repository and begin implementing your proposed enhancements.

4. **Stay Updated:** Regularly synchronize your fork with the main repository to keep your changes current. Note that intermediate upgrades may occur during your development process.

5. **Thorough Documentation:** Clearly document each modification with comprehensive comments. Ensure clarity to assist future contributors. Unclear submissions will be directed by the maintainers to require revisions for forward compatibility.

6. **Draft Your REP:** Fork the REPs Repository and commence drafting your proposal by copying the `rep-template.md` template.

7. **REP ID and Formatting Review:** After opening the Pull Request, the maintainers will review the formatting and provide a REP-ID while updating the file name, e.g., `rep-1.md`.

8. **REP Acceptance:** Upon REP acceptance, the REP will become visible as an accepted REP undergoing a call for public peer-review for further enhancements. At this stage, the author is required to update a development branch of the native substrate source code with their REP. The public can review and provide their opinions for the voting phase if the author decides to proceed with a runtime upgrade transaction.

9. **Voting Stage:** The voting process will commence as per the governance rules specified for a runtime upgrade. The REP can either be selected as "Yes" to proceed with the upgrade or "No" to reject the proposed changes. With a positive acceptance from voters, all nodes will undergo a runtime upgrade, and the author must merge the development branch into the master branch to release the native runtime code.

10. **REP Status and Process:** Familiarize yourself with the different statuses and processes associated with a REP before its implementation can be merged into the main ICN repository.

## Exclusions from REP

It is important to note that REP is not intended for proposals pertaining to the application layer, specifically involving smart contracts. For matters related to application-layer enhancements, ICN offers a distinct proposal format known as [Contract Interface Pronouncements (CIPs)](https://cips.w3society.org). This separate format is designed to facilitate the announcement of interface standards developed by individuals and for-profit organizations, proceeding to public-peer-review for their adoption. 

## Core Principles

Every REP should encompass and affirm these core principles: neutral stance, non-profit ethos, decision approval, and open source publication.

By submitting this REP, I affirm my commitment to the following core principles for ICN Node Runtime Upgrades & Proposals:

- [x] **Protocol Neutrality**: I ensured that this specific upgrade adheres to the principle of protocol neutrality by refraining from imposing specific rules and by upholding absolute freedom of choice for developers, validators, users, and organizations.

- [x] **Non-Profit Ethos**: I ensured the non-profit ethos of this upgrade, which ensures that profit decisions remain within the purview of the proposed protocol's end-participants.

- [x] **Majority Decision**: I agree with the decision-making process outlined in this upgrade, which relies on the majority votes of participants and the approval committee on the proposal's formatting suitability for forward compatibility.

- [x] **Open Source**: I advocate for the commitment to keeping the source code open and accessible, as well as fostering open discussions.

## What to Include in a Successful REP

1. **Header/Front-matter**

    ```
    ---
    rep: id
    title: Title Here
    description: Description of the REP
    status: 
    contributors: github.username,github.username
    date: YYYY-MM-DD
    tx-hash: 0xabc123def456...
    youtube : content-id
    ---
    ```

   - **REP ID**: This field represents the unique ID of the REP. This will be filled by the maintainers of the REPs repository. For example, `rep: 123`.

   - **Title**: Describe the title of the REP under 100 characters `title: Title Here`.

   - **Description**: Provide a brief description of the REP using `description: Description of the REP`.

   - **Status**: This field represents the status of the REP. This will be filled by the maintainers of the REPs repository. For example, `status: call`

   - **Contributors**: List the contributors of the REP by order of primary authors at first with their GitHub usernames. For example, `contributors: jobyreuben,silvernberry`.

   - **Date**: Use `date: YYYY-MM-DD` to specify the date of the REP. For instance, `date: 2023-01-15`.

   - **Transaction Hash**: Record the hash of the Runtime Upgrade Transaction related to this REP as `tx-hash: Hash of the Runtime Upgrade Transaction`. For example, `tx-hash: 0xabc123def456...`. This is only provided after the REP submission is accepted and the status is updated to "call".

   - **YouTube Content**: If there is related the REPs video content, provide the content ID with `youtube: content-id`. For example, `youtube: abcd12345efg`. It is mandatory for the REP authors to attest a video that includes explaining the proposal in fine details.

   - You can use this format to populate the frontmatter of your REP, and the detailed sections can follow.

2. **Abstract**: The abstract should provide a concise overview of the key points covered in this REP.

3. **Motivation**: Explain the motivation behind this proposal or upgrade and why it is necessary to ICN.
4. **Specification**: Describe the technical details and specifications of the proposed changes or upgrades.
5. **Backwards Compatibility**: Discuss how the proposed changes impact backwards compatibility with existing ICN run-time.
6. **Test Cases**: Provide a set of test cases that can be used to verify the correctness and functionality of the proposed changes.
7. **Security Considerations**: Detail any security considerations or potential vulnerabilities associated with the proposed changes.
8. **Other Links**: External Links related to the REP - testing, design theory, events/meeting calls, tutorials, etc.
9.  **Core Principles Acceptance**: Accepting core-principles of REPs by the authors
10. **Copyright**: Copyright and related rights waived via [CC0](/LICENSE).

## REP Template and Format Fit

The REP Template is available [here](/_REPS/rep-template.md) and is written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) format with Jekyll front-matter.

## Copyright

All Copyright and related rights should be waived via [CC0 LICENSE](LICENSE).

Copyright belonging to the source code must be documented in the inline documentation.

# Governance

All Governance-related information will be included in a separate REP proposal. Till its live, the REPs are manually amended by [W3 Society](https://github.com/w3society).
