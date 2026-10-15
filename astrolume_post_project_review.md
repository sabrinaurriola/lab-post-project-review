# Astrolume — Post-Project Review

## Part 1: Project Snapshot

Astrolume was developed to address the lack of personalization in traditional podcasts, which offer the same content to every listener regardless of their individual questions or interests. Our intended users are people interested in astrology-inspired self-reflection who want audio content that feels more relevant to their personal experiences. We built a working prototype using Python, Gradio, and OpenAI that generates a conversation between two AI podcast hosts, Alex and Sam, based on the user's question and an astrology reference PDF. The application then converts the conversation into an MP3 podcast using text-to-speech technology. One key limitation is that the prototype relies on a single PDF, so a future version could incorporate a broader collection of relevant astrology books and reference materials, potentially using Retrieval-Augmented Generation (RAG).

## Part 2: Stakeholder Analysis

The following stakeholder analysis considers how Astrolume would operate as a real product. The roles and influence/interest assessments are based on a hypothetical production environment.

| Stakeholder | Relationship | What they need | Risk if ignored | Influence | Interest |
|---|---|---|---|---|---|
| End users | Direct — generate and listen to podcasts | Relevant, engaging, easy-to-use personalized content | Poor user experience and low adoption | Low | High |
| Product owner / sponsor | Direct — defines priorities and approves investment | Clear product value, user adoption, and controlled costs | Misaligned priorities or loss of funding | High | High |
| Development team | Direct — builds and maintains the application | Clear requirements, maintainable architecture, and reliable integrations | Technical failures and difficult maintenance | High | High |
| Astrology content experts | Direct — advise on reference material and content quality | Appropriate sources and consistent interpretations | Misleading, repetitive, or inconsistent content | Low | High |
| IT / Operations team | Indirect — responsible for service reliability | Monitoring, deployment procedures, and incident ownership | Outages without clear recovery procedures | High | High |
| Privacy / compliance team | Indirect — oversees personal data handling | Appropriate collection, retention, and protection of user data | Privacy risks or deployment delays | High | High |
| Finance team | Indirect — monitors financial sustainability | Visibility into API usage and operating expenses | Unexpected costs as usage increases | High | Low |

End users are a priority because their feedback helps determine whether Astrolume solves a meaningful problem. However, the product owner has the authority to approve investments, such as expanding the knowledge base or introducing RAG. Technical, content, operational, and privacy stakeholders provide the expertise needed to make those decisions responsibly.

## Part 3: From Demo to Real Project

### 1. Data Privacy and Lifecycle

In our current prototype, users provide birth information and personal questions to generate a personalized podcast, but we haven't implemented a formal data retention or deletion policy. For a production version, we would minimize data collection, automatically delete personal inputs and generated files after a defined period, and verify how third-party API providers handle user data.

### 2. Content Quality and Knowledge Management

Our current prototype relies on a single astrology PDF, which limits the variety and depth of the generated podcasts. For a production version, we would consider expanding the knowledge base with additional books and reference materials, potentially using RAG to retrieve relevant information for each user's question. An astrology subject-matter expert would help select and review the sources, while the technical team would evaluate retrieval quality and ensure the generated content remains grounded in those materials.

### 3. Operations and Reliability

Our current prototype runs locally through Gradio and depends on external OpenAI APIs to generate scripts and audio. We haven't implemented production monitoring, automated alerts, or a formal incident response process. For a production rollout, an operations team would monitor application availability, API failures, and generation times, while the development team would implement error handling, recovery mechanisms, and clear procedures for resolving incidents.

### 4. Cost Management

Our current prototype uses OpenAI APIs for script generation and text-to-speech, but we haven't implemented cost monitoring or usage limits. For a production version, we would track API consumption and cost per generated podcast, set a maximum podcast length, and limit the number of podcasts each user can generate. These measures would help control operating expenses as the number of users increases.

## Part 4: Revision Brief

### Before — Original Project Scope

Our initial goal was to build a functional prototype of Astrolume that could generate a personalized podcast based on a user's question. We focused mainly on integrating the different technical components, generating a conversation between two AI hosts, and converting it into playable audio. We considered the project successful if the complete workflow worked from user input to podcast generation.

### After — Revised Project Scope

After considering the stakeholders and the requirements of a real deployment, we would define success beyond simply generating a podcast. We would first validate whether users find the content relevant and engaging, then evaluate expanding our single-PDF knowledge base with additional expert-reviewed sources, potentially using RAG. We would also introduce clear requirements for data privacy, application reliability, API cost control, and operational ownership before considering a production rollout.

## Lab Checkpoints

- [x] **Recognize:** Named Astrolume and identified its intended beneficiaries.
- [x] **Apply:** Identified seven stakeholders with needs, risks, influence, and interest.
- [x] **Integrate:** Addressed four dimensions with concrete changes for production.
- [x] **Verify:** Demonstrated a clear shift from technical functionality to user value and production readiness.
- [x] **Stretch (optional):** Included the finance team as an indirect stakeholder whose concerns could otherwise be overlooked.