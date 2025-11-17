## Al-Driven Development Lifecycle (AI-DLC) Method Definition

## I. CONTEXT

Raja SP, Amazon Web Services

[cite_start]The evolution of software engineering has been a continuous quest to enable developers to focus on solving complex problems by abstracting away lower-level, undifferentiated tasks. [cite: 8] [cite_start]From early machine code to high-level programming languages and the adoption of APIs and libraries, each step has significantly boosted developer productivity. [cite: 9] [cite_start]Now, the integration of Large Language Models has revolutionized how software is created, introducing conversational natural language interactions for tasks like code generation, bug detection, and test generation. [cite: 10] [cite_start]This marks the Al-Assisted era, where Al enhances such fine-grained, specific tasks. [cite: 11] [cite_start]As Al evolves, its applications are expanding beyond code generation to include requirements elaboration, planning, task decomposition, design, and real-time collaboration with developers. [cite: 12] [cite_start]This shift is kick-starting the Al-Driven era, where Al actively orchestrates the development process. [cite: 13] [cite_start]But, existing software development methods, designed for human-driven, long-running processes, are not fully aligned with Al's speed, flexibility, and advanced capabilities (ex. agentic). [cite: 14] [cite_start]Their reliance on manual workflows and rigid role definitions limits the ability to fully leverage Al. [cite: 15] [cite_start]Retrofitting Al into these methods not only limits its potential, but also reinforces outdated inefficiencies. [cite: 16] [cite_start]To fully leverage Al's transformative power, SDLC methods need to be reimagined. [cite: 17] [cite_start]This reimagination requires Al to be a central collaborator, aligning workflows, roles, and iterations to enable faster decision-making, seamless task execution, and continuous adaptability. [cite: 18] [cite_start]This paper introduces and defines the Al-Driven Development Lifecycle (AI-DLC), a reimagined, Al-native methodology designed to fully integrate the capabilities of Al, setting the foundations for the next evolution in software engineering. [cite: 19]

## II. KEY PRINCIPLES

[cite_start]The principles in this section form the foundation for defining Al-DLC, shaping its phases, roles, artifacts, and rituals. [cite: 21] [cite_start]These assumptions are critical for validating the proposed method, as they provide the underpinning rationale behind its design. [cite: 22]

### 1. REIMAGINE RATHER THAN RETROFIT

[cite_start]We choose to reimagine a development method rather than keeping the existing methods like SDLC or Agile (e.g., Scrum) and retrofitting Al into them. [cite: 24] [cite_start]These traditional methods were built for longer iteration duration (months and weeks), which led to rituals like daily standups and retrospectives. [cite: 25, 26] [cite_start]In contrast, proper application of Al leads to rapid cycles, measured in hours or days. [cite: 27] [cite_start]This needs continuous, real-time validation and feedback mechanisms, rendering many of the traditional rituals less relevant. [cite: 28] [cite_start]Would effort estimation (ex. story points) be as critical if Al diminishes the boundaries between simple, medium and hard tasks? [cite: 29] [cite_start]Would metrics like velocity be any relevant or should we start replacing it with Business Value, as an example? [cite: 30] [cite_start]Also, Al is increasingly evolving to automate manual practices including planning, task decomposition, requirements analysis, application of design techniques (ex. domain modelling), thereby shortening the number of phases it takes from moving intentions to code. [cite: 31] [cite_start]These new dynamics warrant a reimagination based on first principles thinking, rather than a retrofitting. [cite: 32] [cite_start]We need automobiles and not the faster horse chariots. [cite: 33]

### 2. REVERSE THE CONVERSATION DIRECTION

[cite_start]Al-DLC introduces a fundamental shift where Al initiates & directs the conversations with humans instead of humans initiating the conversation with Al to complete their tasks. [cite: 35] [cite_start]Al drives workflows by breaking down high-level intents (ex. implementing a new business function) into actionable tasks, generating recommendations, and proposing trade-offs. [cite: 36] [cite_start]Humans serve as approvers, validating, selecting options, and confirming decisions at critical junctures. [cite: 37] [cite_start]This Al-driven approach allows developers to focus on high-value decision-making while Al handles planning, task decomposition, and automation. [cite: 38] [cite_start]By reversing the traditional dynamic, Al-DLC ensures that human involvement is purposeful, concentrating on oversight, risk mitigation, and strategic alignment, thereby enhancing both velocity and quality. [cite: 39, 40] [cite_start]An analogy to illustrate this is Google Maps: humans set the destination (the intent), and the system provides step-by-step directions (Al's task decomposition and recommendations). [cite: 41] [cite_start]Along the way, humans maintain oversight and moderate the journey as needed. [cite: 42]

### 3. INTEGRATION OF DESIGN TECHNIQUES INTO THE CORE

[cite_start]Agile frameworks like Scrum or Kanban leaves the design techniques (ex. Domain Driven Design) out of scope and recommends the teams to choose their own. [cite: 44] [cite_start]This has left critical whitespaces that led to poor software quality overall. [cite: 45] [cite_start]Software quality issues in US alone was estimated to cost $2.41 Trillion in 2022 (study). [cite: 46] [cite_start]Rather than decoupling design techniques out, Al-DLC will have them as its integral core. [cite: 47] [cite_start]There will be different flavors of Al-DLC for teams following Domain Driven Design (DDD), Behavior Driven Development (BDD) or Test-Driven Development (TDD) respectively. [cite: 48] [cite_start]This paper discusses the DDD flavor of AI-DLC which will use DDD principles to break down systems into independent, right-sized bounded contexts that can be rapidly built in parallel. [cite: 49, 56] [cite_start]Al will inherently apply these techniques during planning and task decomposition, requiring developers only to validate and adjust. [cite: 57] [cite_start]This integration is key to enabling hourly or daily iteration cycles while eliminating manual heavy-lifting and maintaining software quality (the mantra of "Build Better Systems Faster"). [cite: 58]

### 4. ALIGN WITH AI CAPABILITY

[cite_start]This paper is optimistic about the future potential of Al but fully realistic about its current state. [cite: 60] [cite_start]Al-DLC recognises that current Al is advancing but not yet reliable in autonomously translating high-level intentions into executable code or independently operating without human oversight, while also ensuring interpretability and safety. [cite: 61] [cite_start]At the same time, the Al-Assisted paradigm, where developers perform the majority of the intellectual heavy lifting with Al merely providing augmentation, fails to unlock the full potential of Al in development. [cite: 62] [cite_start]Al-DLC adopts the Al-Driven paradigm, which balances human involvement with the capabilities and limitations of current Al. [cite: 63] [cite_start]In this, the developers retain ultimate responsibility for validation, decision-making, and oversight. [cite: 64] [cite_start]This balance ensures that the strengths of Al are leveraged effectively without compromising the critical safeguards provided by developer judgment. [cite: 65]

### 5. CATER TO BUILDING COMPLEX SYSTEMS

[cite_start]AI-DLC caters to building systems that demand continuous functional adaptability, high architectural complexity, numerous trade-offs management, scalability, integration and customization requirements. [cite: 67] [cite_start]These necessitate the application of advanced design techniques, patterns, and best practices, typically involving multiple teams working cohesively within large and/or regulated organizations. [cite: 68] [cite_start]Simpler systems that can be developed by non-developer personas that needed few or no trade-off management are outside the scope of AI-DLC and are better suited for low-code/no-code approaches. [cite: 69]

### 6. RETAIN WHAT ENHANCES HUMAN SYMBIOSIS

[cite_start]While reimagining the method, we will retain the artifacts and touchpoints from the existing methods that are critical for human validation and risk mitigation. [cite: 71] [cite_start]For instance, user stories align humans' and Al's understanding of what needs to be built, acting as well-defined contracts. [cite: 72] [cite_start]We will retain user stories as they are in the re-imagined method also. [cite: 73] [cite_start]Another example is the Risk Register that ensures Al-generated plans and codes comply with organizational risk frameworks. [cite: 74] [cite_start]These retained elements will be optimized for real-time use, allowing rapid iterations without compromising alignment or safety. [cite: 75]

### 7. FACILITATE TRANSITION THROUGH FAMILIARITY

[cite_start]The new method shall not demand extensive trainings and any existing practitioner should be able to orient and start practicing it in a single day. [cite: 77] [cite_start]To support easier adoption via associative learning, Al-DLC will preserve the underlying relationships between familiar terms in older methods while introducing modernized terminology. [cite: 78] [cite_start]For example, Sprints in Scrum represent iterative cycles for building and validating. [cite: 79] [cite_start]But Sprints are usually 4 to 6 weeks long in the pre-Al era. [cite: 80] [cite_start]With AI-DLC, the iteration cycles will be continuous and in terms of hours or days. [cite: 81] [cite_start]Therefore, we need to intentionally rename Sprints. [cite: 82] [cite_start]AI-DLC rebrands Sprints as Bolts, emphasizing rapid, intense cycles that deliver unprecedented velocity. [cite: 82]

### 8. STREAMLINE RESPONSIBILITIES FOR EFFICIENCY

[cite_start]By leveraging Al's ability to perform task decomposition, and decision-making, developers will be empowered to transcend traditional specialization silos such as infrastructure, front-end, back-end, DevOps, and security. [cite: 84] [cite_start]This convergence of responsibilities reduces the need for multiple specialized roles, streamlining the development process. [cite: 85] [cite_start]But Product Owners and developers remain integral to the framework, retaining critical responsibilities for oversight, validation, and strategic decision-making. [cite: 86] [cite_start]These roles ensure alignment with business objectives, maintain design quality, and maintain compliance with risk management frameworks, preserving the balance between automation and human accountability. [cite: 87] [cite_start]In the method definition, we will stick to first principles, keeping the roles minimum, with additional roles introduced only when critically necessary. [cite: 88]

### 9. MINIMISE STAGES, MAXIMISE FLOW

[cite_start]Through automation and convergence of responsibiliti4es, Al-DLC aims to minimize the handoffs and transitions, enabling continuous iterative flow. [cite: 90] [cite_start]But human validation and decision-making remain critical to ensure that Al-generated code does not become rigid ('quick-cement') but stays adaptable for future iterations. [cite: 91] [cite_start]To address this, AI-DLC incorporates minimal but sufficient number of phases specifically designed for human oversight at critical decision junctures. [cite: 92] [cite_start]These validations act as a form of 'loss function', by identifying and pruning wasteful downstream efforts before they occur. [cite: 93]

### 10. NO HARD-WIRED, OPINIONATED SDLC WORKFLOWS

[cite_start]Al-DLC avoids prescribing opinionated workflows for different development pathways (such as new system development, refactoring, defect fixes, or microservice scaling). [cite: 95] [cite_start]Instead, it adopts a truly Al-First approach where Al recommends the Level 1 Plan based on the given pathway intention. [cite: 96] [cite_start]Humans verify and moderate these Al-generated plans through interactive dialogue with Al, continuing this process through Level 2 (subtasks) and subsequent hierarchy levels. [cite: 97] [cite_start]At the task execution level, Al implements the tasks while humans maintain oversight through verification and validation of outcomes. [cite: 98] [cite_start]This flexible approach ensures the methodology is adaptable and can evolve alongside Al capabilities while maintaining human control over critical decisions. [cite: 99, 106]

---

## III. CORE FRAMEWORK

[cite_start]This section outlines the core framework of AI-DLC, detailing its phases, roles, workflows, and key artifacts. [cite: 108]

*(Diagram content omitted)*

[cite_start]**Bolts** (analogous to Sprints in Scrum) emphasize intense focus and high-velocity delivery, with build-validation cycles measured in hours or days rather than weeks. [cite: 113] [cite_start]Each Bolt encapsulates a well-defined scope of work (e.g., a collection of user stories within a Unit), enabling incremental progress while maintaining alignment with the overall objectives of the Unit it supports. [cite: 114] [cite_start]A Unit can be executed through one or more Bolts, which may run in parallel or sequentially. [cite: 115] [cite_start]Al will plan the Bolts with developers / Product Owners validating it. [cite: 116]

### 1. ARTEFACTS

**Intent**
[cite_start]An Intent in AI-DLC is a high-level statement of purpose that encapsulates what needs to be achieved, whether a business goal, a feature, or a technical outcome (ex. performance scaling). [cite: 135] [cite_start]It serves as the starting point for Al-driven decomposition into actionable tasks, aligning human objectives with Al-generated plans. [cite: 136]

**Unit**
[cite_start]A Unit represents a cohesive, self-contained work element derived from an Intent, specifically designed to deliver measurable value. [cite: 138] [cite_start]For instance, an Intent to implement a business idea may be decomposed into Units representing independent functional blocks, analogous to Subdomains in DDD or Epics in Scrum. [cite: 139] [cite_start]Each Unit encompasses a set of tasks (user stories, in this case, that articulate its functional scope) In the context of Al-DLC, the process of decomposing Intents into Units is driven by Al, with developers and/or Product Owners validating and refining the resulting Units to ensure alignment with business and technical objectives. [cite: 140] [cite_start]The units are loosely coupled, enabling autonomous development and independent deployment downstream. [cite: 141]

[cite_start]**The Domain Design** artefact models the core business logic of a Unit, independently of the infrastructure components. [cite: 142] [cite_start]In the first version of Al-DLC, Al uses domain-driven design principles to create the strategic and tactical modelling elements including aggregates, value objects, entities, domain events, repositories and factories. [cite: 143]

[cite_start]**The Logical Design** translates Domain Designs by extending them for meeting the non-functional requirements using the right choice of architectural design patterns (ex. CQRS, Circuit Breakers etc.). [cite: 144] [cite_start]Al creates the Architecture Decision Records (ADRs) for validation by the Developers. [cite: 145]

[cite_start]With the Logical Design specification, Al will generate the **Code and Unit Tests**, ensuring adherence to well-architected principles by selecting appropriate AWS services and constructs. [cite: 146] [cite_start]At this stage, the Al agent will conduct the unit testing, analyse the results and provide recommendations on fixes to the Developer. [cite: 147]

[cite_start]**The Deployment Units** are the operational artifacts encompassing the packaged executable code (ex. container images for Kubernetes environments, serverless functions such as AWS Lambda), configurations (ex. Helm Charts), and infrastructure components (ex. Terraform or CFN stacks) that are tested for functional acceptance, security, NFRs and other risks. [cite: 148] [cite_start]Al generates all associated tests, including functional tests, static and dynamic security tests, and load testing scenarios. [cite: 149] [cite_start]After the human validation and adjustments on the test scenarios and cases, the Al agent executes the test suits, analyses the results and correlate failure points with code changes, configurations or other dependencies. [cite: 150] [cite_start]Thus, these units are rigorously tested for functional acceptance, security compliance, adherence to non-functional requirements (NFRs), and mitigation of operational risks, guaranteeing their readiness for seamless deployment. [cite: 151]

### 2. PHASES & RITUALS

[cite_start]A **Bolt** is the smallest iteration in AI-DLC, designed for the rapid implementation of a Unit or a set of tasks within a Unit. [cite: 153]

[cite_start]The **Inception Phase** focuses on capturing Intents and translating them into Units for development. [cite: 154] [cite_start]This phase uses the "Mob Elaboration", a collaborative requirements elaboration and decomposition ritual. [cite: 155] [cite_start]This happens in a single room with a shared screen led by a facilitator. [cite: 156] [cite_start]During Mob Elaboration, Al plays a central role in proposing an initial breakdown of the Intent into User Stories, Acceptance Criteria and Units, leveraging domain knowledge, and the principles of loose coupling and high cohesion for rapid parallel execution downstream. [cite: 162] [cite_start]The Product Owner, Developers, QA and other relevant stakeholders (the mob) collaboratively review and refine these Al-generated artefacts by adjusting under-engineered or over-engineered parts and aligning them with real-world constraints. [cite: 163] [cite_start]The outputs of this phase include well defined Units and their respective components containing a) PRFAQ, b) User Stories, c) Non-Functional Requirement (NFR) definitions, d) Description of Risks (matching with organization's Risk Register, if present), e) Measurement Criteria that traces to the business intent and the f) Suggested Bolts using which the Units can be constructed. [cite: 164] [cite_start]Mob Elaboration condenses weeks or even months of sequential work into a few hours, while achieving deep alignment both within the mob and between the mob and the Al. [cite: 165]

[cite_start]The **Construction Phase** encompasses the iterative execution of tasks, transforming the Units defined during the Inception Phase into tested, operations-ready Deployment Units. [cite: 166] [cite_start]This phase progresses through Domain Design, where Al models the business logic independently of technical considerations, to Logical Design, where non-functional requirements and appropriate cloud design patterns are applied. [cite: 167] [cite_start]Al generates detailed code from Logical Designs by mapping components to appropriate AWS services while adhering to well-architected principles. [cite: 168] [cite_start]The phase concludes with automated testing to ensure functionality, security, and operational readiness. [cite: 169] [cite_start]Developers focus on validating Al-generated outputs at each step and making critical decisions, ensuring quality and adaptability in each iteration. [cite: 170] [cite_start]In the brown-field (existing application) scenarios, the construction phase involves first elevating the codes into a semantic rich modelling representation so that the context to Al becomes concise and accurate. [cite: 171] [cite_start]The suggested modelling representations are static models (just the domain components, responsibilities and their relationships) and dynamic models (how the components interact to realize the significant use cases) [cite: 172] [cite_start]Al plays a pivotal role throughout this phase, recommending tasks and providing options (design patterns, User Experience, Tests etc) at each task. [cite: 173] [cite_start]Al-DLC recommends that this be done with all teams collocated in a single room, similar to Mob Elaboration. [cite: 174] [cite_start]The teams exchange the integration specifications (from domain model stage), make decisions and deliver their bolts. [cite: 175] [cite_start]AI-DLC calls this the mob-construction ritual. [cite: 176]

[cite_start]The **Operations Phase** in Al-DLC centers on the deployment, observability, and maintenance of systems, leveraging Al for operational efficiency. [cite: 177] [cite_start]Al actively analyzes telemetry data, including metrics, logs, and traces, to detect patterns, identify anomalies, and predict potential SLA violations, enabling proactive issue resolution. [cite: 205, 178, 179] [cite_start]Additionally, Al integrates with predefined incident runbooks, proposing actionable recommendations such as resource scaling, performance tuning, or fault isolation and execute the resolutions when approved by the Developers. [cite: 180] [cite_start]Developers serve as validators, ensuring Al-generated insights and proposed actions align with SLAs and compliance requirements. [cite: 181]

---

### 3. THE WORKFLOW

[cite_start]*(Workflow Diagram Text)* [cite: 183, 184, 185]
[cite_start]**Inception** [cite: 183]
1. [cite_start]BUILD CONTEXT FROM EXISTING CODES [cite: 186]
2. [cite_start]ELABORATE INTENT WITH USER STORIES [cite: 187]
3. [cite_start]PLAN THE UNITS OF WORK [cite: 188]

[cite_start]**Construction** [cite: 184]
4. [cite_start]MODEL THE DOMAIN, CODE & TEST [cite: 189]
5. [cite_start]SOLVE FOR NON-FUNCTIONAL REQUIREMENTS [cite: 190]
6. [cite_start]RESOLVE DEPLOYMENT ARCH, CODE & TEST [cite: 191]
7. [cite_start]GENERATE IAAC & TEST [cite: 191]

[cite_start]**Operations** [cite: 185]
8. [cite_start]DEPLOY IN PRODUCTION [cite: 192]
9. [cite_start]MONITOR, MANAGE INCIDENTS [cite: 193]

*(Annotation)*
[cite_start]Each Step Builds Semantically Richer Context to the Next Step [cite: 194, 195]

*(End Workflow Diagram Text)*

[cite_start]Given a business intent (ex. Green-Field development, Brown-Field enhancement, modernization, or defect fixing), AI-DLC begins by prompting Al to generate a Level 1 Plan that outlines the workflow to implement the intent. [cite: 196] [cite_start]This plan serves as an initial proposal, which is then transparently reviewed, validated, and refined by humans to ensure alignment with business goals and engineering constraints. [cite: 197] [cite_start]At the heart of Al-DLC is the principle of applying human oversight to progressively enrich the artefacts of each step, transforming them into semantically rich context for the next. [cite: 198] [cite_start]Each step serves as a strategic decision point where human oversight functions like a loss function - catching and correcting errors early before they snowball downstream. [cite: 199] [cite_start]This repeats recursively. [cite: 200] [cite_start]Each step in the Level 1 Plan is further decomposed into finer-grained, executable sub-tasks by Al, again under human oversight to ensure accuracy and contextual appropriateness. [cite: 200] [cite_start]All artefacts generated (intents, user stories, domain models, or test plans) are persisted and serve as a "context memory" that the Al references across the lifecycle. [cite: 201] [cite_start]Like traditional SDLC methods, Al-DLC is inherently iterative, allowing for continuous refinement and adaptation. [cite: 202] [cite_start]Additionally, all artefacts are linked, allowing for backward and forward traceability (ex. connecting domain model elements to specific user stories) ensuring that the Al retrieves the correct and most relevant context at every stage. [cite: 203] [cite_start]Throughout the process, Al performs the strategic planning, task decomposition, generation etc. and humans provide the oversight and validation. [cite: 204]

---

## IV. [cite_start]AI-DLC IN ACTION: Green-Field Development [cite: 205]

[cite_start]We will examine the scenario in which the Product Owner commences the process by articulating a high-level intent, such as "Develop a recommendation engine for cross-selling products." [cite: 212] [cite_start]Al Recognizes this as an intent to build a new application and produces the Level 1 plan like the Workflow steps in the above section. [cite: 213] [cite_start]The team validates, verifies and adds/fixes the stages in the level 1 plan. [cite: 214] [cite_start]With the finalized Level 1 Plan, Al progresses to the Inception Phase. [cite: 215] [cite_start]Refer to the prompts in Appendix A as a way to interact and provide oversights to Al. [cite: 216]

### [cite_start]1. INCEPTION PHASE [cite: 217]

[cite_start]The following bullet points outline the key interactions in the Mob Elaboration ritual. [cite: 218]
* a. [cite_start]Al asks clarifying questions (e.g., "Who are the primary users? What key business outcomes should this achieve?"), ensuring a comprehensive understanding of the goal and minimize the ambiguity in the original intention [cite: 219]
* b. [cite_start]Al elaborates the clarified intention into user stories, non-functional requirements (NFRs), and risk descriptions. [cite: 220] [cite_start]The team validates these artefacts and provides oversight, and the corrections needed to Al. [cite: 221]
* c. [cite_start]Al composes the highly cohesive stories into Units, e.g., "User Data Collection," "Recommendation Algorithm Selection," and "API Integration." [cite: 222]
* d. [cite_start]The Product Owner validates these outputs, adjusting wherever needed to refine the Units. [cite: 223] [cite_start]Example: The Product Owner notices that User Data Collection lacks privacy compliance details and adjusts the requirements to include GDPR-specific considerations. [cite: 224]
* e. [cite_start]Al generates a PRFAQ for the module (optional), summarizing the business intent, functionality, and expected benefits. [cite: 225]
* f. [cite_start]Developers and Product Owners validate the PRFAQ and associated risks, ensuring alignment with the overall objectives. [cite: 226]

### [cite_start]2. CONSTRUCTION PHASE [cite: 227]

[cite_start]The following bullet points outline the key activities involved in this phase, focusing on the Mob Programming and Mob Testing rituals. [cite: 228]
* a. [cite_start]The Developer establishes the session with Al. [cite: 229] [cite_start]Al prompts the developer to begin with the Unit assigned to them. [cite: 229]
* b. [cite_start]Al models the core business logic for the assigned Unit using Domain-Driven Design principles. [cite: 230] [cite_start]Example: For the "Recommendation Algorithm" Unit, Al identifies relevant entities like Product, Customer, and Purchase History and their relationships. [cite: 231]
* c. [cite_start]Developers review and validate the domain models, refining business logic and ensuring alignment with real-world scenarios (e.g., how to handle missing purchase history for new customers) [cite: 232]
* d. [cite_start]Al translates the domain models into logical designs, applying NFRs like scalability and fault tolerance. [cite: 233] [cite_start]Example: Al recommends architectural patterns (e.g., event-driven design) and technologies (e.g., AWS Lambda for serverless computation). [cite: 234]
* e. [cite_start]Developers evaluate Al's recommendations, approve trade-offs, and suggest additional considerations if needed. [cite: 235] (e.g., Accepts Lambda for scalability but overrides the storage to DynamoDB for faster query performance) [cite_start][cite: 236]
* f. [cite_start]Al generates executable code for each Unit, mapping logical components to specific AWS services. [cite: 237]
* g. [cite_start]It also auto-generates functional, security, and performance tests (e.g., For the "Recommendation Algorithm" Unit, Al creates code to implement collaborative filtering and integrates it with a DynamoDB data source) [cite: 260]
* h. [cite_start]Developers review the generated code and test scenarios/cases, making adjustments where necessary to ensure quality and compliance. [cite: 267]

[cite_start]**Testing and Validation:** [cite: 268]
* a. [cite_start]Al Executes all tests (functional, security, and performance), analyzes results, and highlights issues. [cite: 269]
* b. [cite_start]Proposes fixes for failed tests, e.g., optimizing query logic for better performance. [cite: 270]
* c. [cite_start]Developers validate Al's findings, approve fixes, and rerun tests as needed. [cite: 271]

### [cite_start]3. OPERATIONS PHASE [cite: 272]

[cite_start]**Deployment:** [cite: 273]
* a. [cite_start]Al packages the module into Deployment Units (e.g., container images, serverless functions). [cite: 274]
* b. [cite_start]Developers approve the deployment configuration and initiate rollout to staging and production environments. [cite: 275]

[cite_start]**Observability and Monitoring:** [cite: 276]
* a. [cite_start]Al analyzes metrics, logs, and traces to identify anomalies and predict potential SLA violations. [cite: 277] [cite_start]Example: Al detects a latency spike during peak usage and proposes scaling the recommendation engine to handle increased traffic. [cite: 278]
* b. [cite_start]Al integrates with playbooks to suggest actions for operational issues. [cite: 279] [cite_start]If API response times degrade, Al recommends increasing DynamoDB throughput or rebalancing API Gateway traffic. [cite: 280]
* c. [cite_start]Developers validate $AI^{\prime}s$ recommendations, approve mitigations, and monitor resolution outcomes. [cite: 281]

---

## [cite_start]V. AI-DLC IN ACTION: Brown-Field Development [cite: 282]

[cite_start]Brown-field refers to making changes to an existing system in terms of either adding new features, optimizing it for non-functional requirements or fixing technical debts including refactoring and fixing defects. [cite: 283] [cite_start]In this context, we will examine a scenario where the product manager needs to add a new feature to an existing application. [cite: 284]

### [cite_start]1. INCEPTION PHASE [cite: 285]

[cite_start]The inception phase activities in the brown-filed are same as that of the green-field [cite: 286]

### [cite_start]2. CONSTRUCTTION PHASE [cite: 287]

* a. [cite_start]Al elevates the codes into a higher-level modelling representation. [cite: 288] [cite_start]The models comprise of static models (components, descriptions, responsibilities and relationships) and dynamic models (how the components interact to realize the most significant use cases) [cite: 288, 289]
* b. [cite_start]Developers collaborate with product managers to review, validate and correct the static and dynamic models that are reverse engineered by Al. [cite: 290]
* c. [cite_start]With these extra steps, the rest of the construction phase is similar to that of the green-field scenario. [cite: 291]

### [cite_start]3. OPERATIONS PHASE [cite: 292]

[cite_start]The operations phase activities in the brown-filed are same as that of the green-field [cite: 293]

---

## VI. [cite_start]ADOPTING AI-DLC [cite: 294]

[cite_start]AI-DLC does not deviate much from the existing Agile methods and it is designed with easier adoption as a key outcome. [cite: 295] [cite_start]Still organizations that are practicing the traditional methods for longer and those who are in the process of inventing their own variation of Al-Native methods need specific strategies for adopting Al-DLC. [cite: 296] [cite_start]We believe the following 2 approaches will make this easier. [cite: 297]

* a. [cite_start]**Learning by Practicing**-AI-DLC is actually a set of rituals (Mob Elaboration, Mob Construction etc.) that can be practiced as a group. [cite: 298] [cite_start]Instead of learning the method via documentation and traditional trainings, we will get the practitioners to practice the rituals with the AI-DLC guides in multiple real world scenarios that are currently being solved by the practitioners. [cite: 299] [cite_start]The AWS Solution Architects have created a field offering called Al-DLC Unicorn Gym that packages this approach for hyper-scaling adoption in large organizations. [cite: 300]
* b. [cite_start]**By embedding Al-DLC in the new Developer Experience Tooling** our customers are building their own orchestration tools that cut across SDLC, providing a unified experience for their developers. [cite: 301] (ex. FlowSource from Cognizant, CodeSpell by Aspire, AlForce by HCL etc.) [cite_start][cite: 302] [cite_start]By embedding AI-DLC in these tools, the developers in large organizations will seamlessly practice Al-DLC without any need for significant adoption drives. [cite: 302]

---

## [cite_start]APPENDIX A [cite: 309]

[cite_start]The following prompts can be used to interact with Al for practicing Al-DLC. [cite: 310]

### [cite_start]##Setup Prompt [cite: 311]

[cite_start]We will work on building an application today. [cite: 312] [cite_start]For every front end and backend component we will create a project folder. [cite: 312] [cite_start]All documents will reside in the aidic-docs folder. [cite: 313] [cite_start]Throughout our session I'll ask you to plan your work ahead and create an md file for the plan. [cite: 313] [cite_start]You may work only after I approve said plan. [cite: 314] [cite_start]These plans will always be stored in aidic-docs/plans folder. [cite: 314] [cite_start]You will create many types of documents in the md format. [cite: 315] [cite_start]Requirement, features changes documents will reside in aidlc-docs/requirements folder. [cite: 316] [cite_start]User stories must be stored in the aidic-docs/story-artifacts folder. [cite: 316] [cite_start]Architecture and Design documents must be stored in the aidic-docs/design-artifacts folder. [cite: 317] [cite_start]All prompts in order must be stored in the aidlc-docs/prompts.md file. [cite: 318] [cite_start]Confirm your understanding of this prompt. [cite: 318] [cite_start]Create the necessary folders and files for storage, if they do not exist already. [cite: 319]

### [cite_start]##Inception [cite: 320]

### [cite_start]## User stories [cite: 321]

[cite_start]**Your Role:** You are an expert product manager and are tasked with creating well defined user stories that becomes the contract for developing the system as mentioned in the Task section below. [cite: 322] [cite_start]Plan for the work ahead and write your steps in an md file (user\_stories\_plan.md) with checkboxes for each step in the plan. [cite: 323] [cite_start]If any step needs my clarification, add a note in the step to get my confirmation. [cite: 324] [cite_start]Do not make critical decisions on your own. [cite: 325] [cite_start]Upon completing the plan, ask for my review and approval. [cite: 325] [cite_start]After my approval, you can go ahead to execute the same plan one step at a time. [cite: 326] [cite_start]Once you finish each step, mark the checkboxes as done in the plan.. [cite: 327]
[cite_start]**Your Task:** Build user stories for the high-level requirement as described here << describe product descrition>> [cite: 328]
[cite_start]<<<After reviewing and changing the plan>>>> [cite: 329]
[cite_start]Yes, I like your plan as in the <<md file>>. [cite: 330] [cite_start]Now exactly follow the same plan. [cite: 330] [cite_start]Interact with me as specified in the plan. [cite: 331] [cite_start]Once you finish each step, mark the checkboxes in the plan. [cite: 331]

### [cite_start]## Units [cite: 332]

[cite_start]**Your Role:** You are an experienced software architect. [cite: 333] [cite_start]Before you start the task as mentioned below, please do the planning and write your steps in the units\_plan.md file with checkboxes against each step in the plan. [cite: 333] [cite_start]If any step needs my clarification, please add it to the step to interact with me and get my confirmation. [cite: 334, 335] [cite_start]Do not make critical decisions on your own. [cite: 336] [cite_start]Once you produce the plan, ask for my review and approval. [cite: 336] [cite_start]After my approval, you can go ahead to execute the same plan one step at a time. [cite: 337] [cite_start]Once you finish each step, mark the checkboxes as done in the plan. [cite: 338]
[cite_start]**Your Task:** Refer to the user stories mvp\_user\_stories.md file. [cite: 339] [cite_start]Group the user stories into multiple units that can be built independently. [cite: 339] [cite_start]Each unit contains highly cohesive user stories that can be built by a single team. [cite: 340] [cite_start]The units are loosely coupled with each other. [cite: 341] [cite_start]For each unit, write their respective user stories and acceptance criteria in individual md files in the design/folder. [cite: 341]
[cite_start]<<<<<<<After reviewing and changing the plan> [cite: 342]
I approve. [cite_start]Proceed. [cite: 343]

### [cite_start]###Construction [cite: 344]

### [cite_start]## Domain (component) model creation [cite: 345]

[cite_start]**Your Role:** You are an experienced software engineer. [cite: 346] [cite_start]Before you start the task as mentioned below, please do the planning and write your steps in an design/component\_model.md file with checkboxes against each step in the plan. [cite: 346] [cite_start]If any step needs my clarification, please add it to the step to interact with me and get my confirmation. [cite: 347] [cite_start]Do not make critical decisions on your own. [cite: 348] [cite_start]Once you produce the plan, ask for my review and approval. [cite: 348] [cite_start]After my approval, you can go ahead to execute the same plan one step at a time. [cite: 349] [cite_start]Once you finish each step, mark the checkboxes as done in the plan. [cite: 350]
[cite_start]**Your Task:** Refer to the user stories in the design/seo\_optimization\_unit.md file. [cite: 351] [cite_start]Design the component model to implement all the user stories. [cite: 352] [cite_start]This model shall contain all the components, the attributes, the behaviours and how the components interact to implement the user stories. [cite: 353] [cite_start]Do not generate any codes yet. [cite: 354] [cite_start]Write the component model into a separate md file in the /design folder. [cite: 354]
[cite_start]<<<After reviewing and changing the plan>>>> [cite: 355]
[cite_start]I approve the plan. [cite: 356] [cite_start]Proceed. [cite: 356] [cite_start]After completing each step, mark the checkbox in your plan file. [cite: 356]

### [cite_start]##: Code Generation [cite: 357]

[cite_start]**Your Role:** You are an experienced software engineer. [cite: 358] [cite_start]Before you start the task as mentioned below, please do the planning and write your steps in an md file with checkboxes against each step in the plan. [cite: 358] [cite_start]If any step needs my clarification, please add it to the step to interact with me and get my confirmation. [cite: 359] [cite_start]Do not make critical decisions on your own. [cite: 360] [cite_start]Once you produce the plan, ask for my review and approval. [cite: 360] [cite_start]After my approval, you can go ahead to execute the same plan one step at a time. [cite: 361, 368] [cite_start]Once you finish each step, mark the checkboxes as done in the plan. [cite: 368]
[cite_start]**Task:** Refer to component design in the search\_discovery/nlp\_component.md file. [cite: 369] [cite_start]Generate a very simple and intuitive Python implementation for the Natural Language Processing (NLP) Component that is in the design. [cite: 369] [cite_start]For the processQuery(queryText) method, use amazon bedrock APIs to extract the entities from the query text. [cite: 370] [cite_start]Generate the classes in respective individual files but keep them in 'vocabMapper directory. [cite: 371] [cite_start]Refer to the generated codes in vocabMapper directory. [cite: 372] [cite_start]I want the EntityExtractor component to make a call to GenAl. [cite: 372] [cite_start]The current implementation uses the local vocabulary\_repository. [cite: 373] [cite_start]Can you analyse and give me a plan on how I can leverage GenAl for both the Entity Extraction and Intent Extraction. [cite: 373]

### [cite_start]##: Architecture [cite: 374]

[cite_start]**Your Role:** You are an experienced Cloud Architect. [cite: 375] [cite_start]Before you start the task as mentioned below, please do the planning and write your steps in a deployment\_plan.md file with checkboxes against each step in the plan. [cite: 375] [cite_start]If any step needs my clarification, please add it to the step to interact with me and get my confirmation. [cite: 376] [cite_start]Do not make critical decisions on your own. [cite: 377] [cite_start]Once you produce the plan, ask for my review and approval. [cite: 377] [cite_start]After my approval, you can go ahead to execute the same plan one step at a time. [cite: 378] [cite_start]Once you finish each step, mark the checkboxes as done in the plan. [cite: 379]
[cite_start]**Task:** [cite: 380]
[cite_start]Refer component design model: design/core\_component\_model.md, units in the UNITS/ folder, cloud architecture in the ARCHITECTURE/ folder, and backend code in the BACKEND/folder. [cite: 381, 382]
Complete the following:
[cite_start]Generate a end-to-end plan for deployment of the backend on AWS cloud using [CloudFormation, CDK, Terraform]. [cite: 383]
* [cite_start]Document all the pre-requisites for the deployment, if any. [cite: 384]
Once I approve the plan:
* [cite_start]Follow the best practice of clean, simple, explainable coding. [cite: 385] [cite_start]All output code goes in the DEPLOYMENT/folder. [cite: 385]
* [cite_start]Validate that the generated code works as intended, by creating a validation plan, generate a validation report. [cite: 386]
* [cite_start]Review the validation report and fix all identified issues, update the validation report. [cite: 387]

### [cite_start]##: Build laC/Rest APIs [cite: 388]

[cite_start]**Your Role:** You are an experienced software engineer. [cite: 389] [cite_start]Before you start the task as mentioned below, please do the planning and write your steps in an md file with checkboxes against each step in the plan. [cite: 389] [cite_start]If any step needs my clarification, please add it to the step to interact with me and get my confirmation. [cite: 390] [cite_start]Do not make critical decisions on your own. [cite: 391] [cite_start]Once you produce the plan, ask for my review and approval. [cite: 391] [cite_start]After my approval, you can go ahead to execute the same plan one step at a time. [cite: 392] [cite_start]Once you finish each step, mark the checkboxes as done in the plan. [cite: 393]
[cite_start]**Task:** Refer to the services.py under the construction/<>/folder. [cite: 394] [cite_start]Create python flask apis for each of the service there. [cite: 394]