# Project Charter

## Technical Charter of the CAMARA Project
This technical charter (the “Charter”) describes the rules and governance of the CAMARA Project (the “Project”). It is meant to be followed by all the contributors and maintainers of, and other participants in (collectively, “participants”), the Project and the CAMARA Project community. Common terminology used in this governance document is defined below:
- **CAMARA - The Telco Global API Alliance**: The sum of partners and people listed in the [PARTICIPANTS](./PARTICIPANTS.MD) file, the CAMARA Project and the OPAG working group withing GSMA/OPG.
- **CAMARA Project community**: The sume of people listed in [PARTICIPANTS](./PARTICIPANTS.MD).
- **CAMARA Project**: The sum of all activities and sub-projects performed under the governance protocol defined in this document.
- **Sub-projects**: A single sub directory in the CAMARA Project led by a voluntary group, open to anyone to participate.
- **Participant**: Participant = contributor of the CAMARA Project named in the file [PARTICIPANTS](./PARTICIPANTS.MD).
- **Maintainers**: Leaders of an individual sub-project or part thereof (MAINTAINERS.MD of the respective sub-project).
- **Code Owners**: Leaders of the CAMARA Project documented in the file [CODEOWNERS](./CODEOWNERS).
- **Partner**: Partner = member, company listed in [PARTICIPANTS](./PARTICIPANTS.MD).

The Project is an independent open-source project, not controlled by any single company or organization and has been established as CAMARA Project a Series of LF Projects, LLC. LF Projects, LLC is a Delaware series limited liability company (“LF Projects”). 

For specific guidance on the practical steps for contributing to any API sub-project please see our [Contribution Guidelines](./CONTRIBUTING.md).

## Principles
The CAMARA Project community adheres to the following principles:
- Open: The Project is open source. That especially means that the project has a clear pro-competitive goal to specify/harmonzize and develop open, global, and interoperable API solutions using an open and transparent process at every time. All participants are encouraged to be observant that there is no patent ambush by SEP holders and no market power abuse and report if any.
- Welcoming and respectful: We abide by the [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
- Transparent and accessible: Changes to the Project organization, Project code repositories, and activities related to LF Projects, the Linux Foundation and CNCF (e.g. level, involvement, etc.) are done in public. A primary reason that the CAMARA Project exists is as a forum for collaboration. The work in the project should be done in the open. Excepted as authorized by the Steering Committee with respect to security and code of conduct issues, community members and contributors must communicate in the open, ensure other community members and contributors can find notes of meetings, discussions, designs, and decisions, and periodically communicate a high-level summary of their contribution work to the community. Exception to this is committee work, this may be done in private if discretion is necessary.
- Merit: Ideas and contributions are accepted according to their technical merit and alignment with project objectives, scope, and design principles.

## CAMARA Project

A global partnership could address much of the challenges in scaling API services across heterogenous operator architectures.

The development of open, global, and interoperable API solutions could benefit customers and developer ecosystems by giving access to operator capabilities in whatever network customers are in and therefore allow applications to run consistently between telco networks and countries. A new form of collaboration between various players (telcos, ISVs, device manufacturers, hyperscalers, etc.) could address much of the challenges in scaling API services across heterogenous operator architectures as well as advance the connectivity industry towards a more robust and faster core network, encourage the faster adoption of capabilities and as a result create value for the entire tech industry.

* Accelerate technology development
    * Build sustainable ecosystems around collaborative projects across industries.
    * Drive industry alignment by facilitating industry discussions with telcos, ISVs, device manufacturers, hyperscalers, etc.
* Harmonization of APIs
    * Harmonize and convert APIs to a user understandable format called “Service APIs”.
    * Achieve harmonization through working code vs. documents.
    * Implementation experience should guide harmonization process.
    * Enable interoperability (e.g. effortless portability of applications between different operators), compatibility (applicability to different network technologies) and interconnectivity (to enable interoperator collaboration).
* Education and promotion
    * Actively promote Service APIs via various forums, events, conferences, training programs, ecosystems and social media.
    * Promote best practices by aggregating and publishing lessons learned.
* Accelerate commercial adoption
    * Create awareness around use cases and services.
    * Minimize implementation effort though easy-to-consume Service APIs.
    * Foster the API integration in relevant developer’s environments and ecosystems.
    * Provide customer service and support for the design phase and experimentation.

APIs grouped by services and bundled up into “Service APIs” could reduce the complexity of accessing operator capabilities for developers and enterprises.
CAMARA Project is an independent open-source project and not controlled by any single company. How each operator monetize the API is completely out of the scope of the project. Implementation is still on the operator responsibility. Only scope of the CAMARA Project is how APIs are designed or consumed technically.

## Scope of the project

**Functional scope**

From functional perspective the scope is limited to telco APIs, that means APIs in the domain of telco mobile networks, telco fixed line networks or supporting these (e.g. for authentication). The respective API families are clarified during the ramp up of the CAMARA Project, specifically the ones exposed to customers.

**Technical scope**

Technically the scope is about northbound Service APIs, that means an abstraction / aggregation of e.g. 3GPP APIs or TM Forum APIs to hide telco complexity, keep control at the operator side and fulfill regulatory and data privacy constraints. Optionally in scope are east-/westbound APIs on the same abstraction / aggregation level.
![ServiceAPI Architecture](/documentation/ressources/ServiceAPI_Architecture.jpg)

The Service APIs (incl. mapping tables for the attributes to the southbound APIs if useful) are in scope of the project and in scope of the harmonization. The transformations functions (business logic that calls the southbound APIs, transforms the data and provides the function for the Service APIs) are in scope of the project as example / reference implementations, but not in scope of the harmonization. So each telco operator can implement the transformation functions in the best manner considering the own network topology and vendors, and can use the reference implementation as an orientation and starting point.

**Service scope**

The service scope of the CAMARA Project is limited to the following activities:
-	Collect API requirements from GSMA OPG subgroup and other sources. That can be a (prioritized) list of API families seen as useful for the customers, a functional descriptions of the APIs (attributes, function, result), and also non-functional requirements for the APIs (response time, scalability, performance, etc.). All APIs developed within GSMA/OPG and contributed to the CAMARA Project will be developed under Apache-2.0.
-	Specify Service APIs (e.g. by Swagger) and create test plan / cases / tools from a business and customer perspective
-	Develop Service APIs (and reference implementation for transformation functions)
-	Create test cases and perform verification/tests from developer perspective (to show that the Service API / transformation function has been developed correctly)
-	Create documentation for Service APIs
-	Test Service APIs from business/customer perspective (validation) in telco network(s)
-	Create deployment packages for Service APIs
-	Create a reference architecture for Service APIs (if possible preferred solution is to refer to an existing architecture)
-	Define a standard API lifecycle, development and test process incl. tools for the project

**Deliverables**

The following deliverables are provided by the CAMARA Project (all materials developed in relation to the CAMARA Project will be developed under the Apache-2.0 license):
-	Service API code (incl. reference implementation for transformation functions) and documentation and
-	Test plan, cases and tools

both contained in deployment packages.
In addition a
-	Reference architecture for Service APIs
-	Description of the standard API lifecycle, development and test process

is created.

## Governance

**Steering Committee**

The highest deciding committee is the Steering Committee of the CAMARA Project. At the inception of the project, the voting members of the Steering Committee were agreed in a bootstrap steering committee meeting, with each company represented in the Participants.md file in the project’s repository appointing one voting member of the Steering Committee. The voting members will be listed in the [CODEOWNERS](./CODEOWNERS) file within the Project’s code repository. The Steering Committee decides on adding or removing members, and may choose an alternative approach for determining the voting members of the Steering Committee, and any such alternative approach will be documented in this [Project Charter](./ProjectCharter.md). Any meetings of the Steering Committee are intended to be open to the public, and can be conducted electronically, via teleconference, or in person. 

A member of the steering board can – in case of absence or unavailability - send a representative as stand-in. The steering board has to be informed before a representation including the duration of it. To avoid much changes in the steering board each member shall name a default stand-in.

The technical roles of the Project are described in the [Project Structure And Roles](./ProjectStructureAndRoles.md) file. The Steering Committee may adopt or modify roles so long as the roles are documented in the [Project Structure And Roles](./ProjectStructureAndRoles.md) file. Participation in the Project through becoming a participant and/or maintainer is open to anyone so long as they abide by the terms of this Charter. 

The Steering Committee may (1) establish workflow procedures for the submission, approval, and closure/archiving of sub-projects and working groups, (2) set requirements for the promotion of participants from one technical role to another, and (3) amend, adjust, refine and/or eliminate any technical roles, and create new roles, and publicly document any roles, as it sees fit.

Responsibilities: The Steering Committee is responsible for all aspects of oversight relating to the Project, which may include:
- coordinating the technical direction of the Project;
- approving sub-project proposals (including, but not limited to, incubation, deprecation, and changes to a sub-project’s scope);
- organizing sub-projects and removing sub-projects;
- creating, and determining composition of, committees or working groups to focus on cross-project technical or issues and requirements;
- appointing representatives to work with other open source or open standards communities;
- establishing community norms, workflows, issuing releases, and security issue reporting policies;
- approving and implementing policies and processes for contributing (to be published in the [Contribution Guidelines](./CONTRIBUTING.md)) and coordinating with LF Projects to resolve matters or concerns that may arise as set forth in this Charter;
- discussions, seeking consensus, and where necessary, voting on technical matters relating to the code base that affect multiple projects; and
- coordinating any marketing, events, or communications regarding the Project.

## Decision Making

**Voting Principles**

The CAMARA Project usually runs by informal consensus, however sometimes a formal decision must be made (reasons for this see below).

Depending on the subject matter, different methods of voting are used as laid out below.

For all votes, voting must be open for at least one week. The end date should be clearly stated in the call to vote. A vote may be called and closed early if enough votes have come in one way so that further votes cannot change the final decision.

In all cases, all and only participants are eligible to vote, with the sole exception of the forced removal of a participant, in which said participant is not eligible to vote.

Discussion and votes on personnel matters (including but not limited to team participantship and maintainership) are held in private. All other discussion and votes are held in public on the CAMARA Project mailing list.

For public discussions, anyone interested is encouraged to participate. Formal power to object or vote is limited to participants.

**Consensus**

The default decision making mechanism for the CAMARA Project is [lazy consensus](https://couchdb.apache.org/bylaws.html#lazy). This means that any decision on technical issues is considered supported by the team as long as nobody objects based on substantiated technical grounds.

Silence on any consensus decision is implicit agreement and equivalent to explicit agreement. Explicit agreement may be stated at will. Decisions may, but do not need to be called out and put up for decision on the CAMARA Project mailing list at any time and by anyone.

Consensus decisions can never override or go against the spirit of an earlier explicit vote.

If any participant raises objections, the participants work together towards a solution that all involved can accept. This solution is again subject to [lazy consensus](https://couchdb.apache.org/bylaws.html#lazy).

In case no consensus can be found, but a decision one way or the other must be made, any participant may call a formal majority vote.

**Majority vote**

Majority votes must be called explicitly in a separate thread on the appropriate mailing list. The subject must be prefixed with [VOTE]. In the body, the call to vote must state the proposal being voted on. It should reference any discussion leading up to this point.

Votes may take the form of a single proposal, with the option to vote yes or no, or the form of multiple alternatives.

A vote on a single proposal is considered successful if more eligible to vote vote in favor than against.

If there are multiple alternatives, participants may vote for one or more alternatives, or vote “no” to object to all alternatives. It is not possible to cast an “abstain” vote. A vote on multiple alternatives is considered decided in favor of one alternative if it has received the most votes in favor, and a vote from more than half of those voting. Should no alternative reach this quorum, another vote on a reduced number of options may be called separately.

**Supermajority vote**

Supermajority votes must be called explicitly in a separate thread on the appropriate mailing list. The subject must be prefixed with [VOTE]. In the body, the call to vote must state the proposal being voted on. It should reference any discussion leading up to this point.

Votes may take the form of a single proposal, with the option to vote yes or no, or the form of multiple alternatives.

A vote on a single proposal is considered successful if at least two thirds of those eligible to vote vote in favor.

If there are multiple alternatives, participants may vote for one or more alternative, or vote “no” to object to all alternatives. It is not possible to cast an “abstain” vote. A vote on multiple alternatives is considered decided in favor of one alternative if it has received the most votes in favor, and a vote from at least two thirds of those voting. Should no alternative reach this quorum, another vote on a reduced number of options may be called separately.

**Steering board decisions**

For votes taken during a steering board meeting (in person, by telephone or online conference or similar), quorum requires at least 2/3 of all voting members of the Steering Committee to be present. The Steering Committee may continue to meet if quorum is not met but will be prevented from making any decisions at the meeting.  Except as provided elsewhere in this Charter, decisions by vote at a steering board meeting require a majority vote of those in attendance, provided quorum is met.

For votes taken by email or similar asynchronous means, voting must be open for at least one week and decisions require at least a two-thirds vote of all members of the Steering Committee. Decision is then taken by majority vote.

**Technical decisions**

Technical decisions that only affect a single sub-project are made informally by the maintainer of this sub-project, and [lazy consensus](https://couchdb.apache.org/bylaws.html#lazy) is assumed. Technical decisions that span multiple parts of the CAMARA Project should be discussed and made on the CAMARA Project mailing list.

Decisions are usually made by [lazy consensus](https://couchdb.apache.org/bylaws.html#lazy). If no consensus can be reached, the matter may be resolved by majority vote.
 
**Changes in Participantship and maintainership**

Changes in participantship and maintainership are defined in [Project Structure And Roles](./ProjectStructureAndRoles.md).

## Intellectual Property Policy

Participants acknowledge that the copyright in all new contributions will be retained by the copyright holder as independent works of authorship and that no contributor or copyright holder will be required to assign copyrights to the Project. 

Except with respect to alternative licenses approved by the Steering Committee as described below, all contributions to the Project are subject to the following: 
- All new inbound contributions to the Project must be made using the Apache License, Version 2.0, available at https://www.apache.org/licenses/LICENSE-2.0 (the “Project License”). 
- All new inbound contributions must also be accompanied by a Developer Certificate of Origin (http://developercertificate.org) sign-off in the source code system that is submitted through a steering committee approved contribution process which will bind the authorized contributor and, if not self-employed, their employer to the applicable license;
- All outbound materials and contributions will be made available under the Project License.
- The Project may seek to integrate and contribute back to other open source projects (“Upstream Projects”). In such cases, the Project will conform to all license requirements of the Upstream Projects, including dependencies, leveraged by the Project. Upstream Project code contributions not stored within the Project’s main code repository will comply with the contribution process and license terms for the applicable Upstream Project.

The Steering Committee may approve the use of an alternative license or licenses for inbound or outbound contributions on an exception basis. To request an exception, please describe the contribution, the alternative open source license(s), and the justification for using an alternative open source license for the Project. License exceptions must be approved by a two-thirds vote of the entire Steering Committee. 

Contributed files should contain license information, such as SPDX short form identifiers, indicating the open source license or licenses pertaining to the file.

## Policies

Participants will comply with the policies of LF Projects as may be adopted and amended by LF Europe, including, without limitation the policies listed at https://lfprojects.be/policies/.  

When amending or adopting any policy applicable to the Project, LF Europe will publish such policy, as to be amended or adopted, on its web site at least 30 days prior to such policy taking effect; provided, however, that in the case of any amendment of the Trademark Policy or Terms of Use of LF Europe, any such amendment is effective upon publication on LF Europe’s web site.

All participants must allow open participation from any individual or organization meeting the requirements for contributing under this Charter and any policies adopted for all participants by the Steering Committee, regardless of competitive interests. Put another way, the Project community must not seek to exclude any participant based on any criteria, requirement, or reason other than those that are reasonable and applied on a non-discriminatory basis to all participants in the Project community.

LF Europe will hold title to all trade or service marks used by the Project (“Project Trademarks”), whether based on common law or registered rights, and domain names and code repository accounts.  Project Trademarks will be transferred and assigned to LF Projects to hold on behalf of the Project. Any use of any Project Trademarks by Collaborators in the Project will be in accordance with the license from LF Projects and inure to the benefit of LF Projects.  

Under no circumstances will the project undertake or will LF Projects be expected or required to undertake any action on behalf of the Project that is inconsistent with the tax status or purpose, as applicable, of LF Projects or its affiliates.

## Amendment

This Charter may be amended by a two-thirds vote of the entire Steering Committee and is subject to approval by LF Projects.
