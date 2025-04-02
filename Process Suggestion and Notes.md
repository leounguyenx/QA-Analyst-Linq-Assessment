
# PROCESS SUGGESTION

As my experience working as one of the first QA in a startup company, the process should contain 5 main phases of testing process:

### 1) Strategic Test Planning & Documentation
#### 1.1) Sprint Scope Analysis 
- Begin each sprint by thoroughly analyzing the scope, user stories, and acceptance criteria.
- Collaborate with developers and product managers to understand the technical implementation and potential risks.
#### 1.2) Risk-Based Test Prioritization:
- Identify critical features and high-risk areas that require immediate attention.
- Prioritize testing efforts based on business impact and potential user issues.
### 2) Manual Testing
Manual is the first crucial part to test the product as some testing are executed at this phase:
#### 2.1) Smoke Testing (Build Verification): 
- Execute a quick set of critical test cases to ensure the build is stable and deployable.
- Focus on core functionalities and basic system health.
#### 2.2) Functional Testing
- Verify that each feature functions according to the specified requirements.
- Cover positive and negative test scenarios.
- Perform UI/UX testing to ensure a consistent and user-friendly experience.
#### 2.3) Integration Testing
- Verify the communication and data flow between different modules and systems.
- Focus on ensuring seamless integration with third-party APIs and services.
#### 2.4) Regression Testing
- Perform a small set of regression test to ensure that the new changes did not break the existing functionalities.
#### 2.5) Exploratory Testing
- Allow for ad-hoc testing to uncover unexpected issues and edge cases.
- Encourage collaboration between QA and developers during this phase.
### 3) Automated Testing
Depend on the the product phases, end-to-end/user acceptance and regression testings are the most important part to optimize testing time and product quality.
#### 3.1) Strategic Automation
- Focus on automating stable and critical test scenarios, particularly for regression testing.
- Prioritize automation for repetitive tasks and workflows.
- Automate API testing.

#### 3.2) End-to-End Testing and User Acceptance Testing
- Automate key user flows to ensure critical business processes function correctly.
- Develop test scripts that are maintainable and scalable.

#### 3.3) Performance Testing
- Conduct load, stress, and performance testing to evaluate the system's responsiveness and stability under various conditions.

### 4) Applying CI/CD
- Integrate automated tests into the CI/CD pipeline to enable continuous testing and feedback.
- Maintain separate environments for development, testing, and production.
- Integrate monitoring tools to track application performance and identify issues in production

### 5) Continious Feedback and Improvement
- Regular Retrospectives: Conduct sprint retrospectives to review the QA process and identify areas for improvement from all team.
- Track and analyze defects to identify root causes and prevent future occurrences.
- Share best practices and lessons learned with the team.
- Analyze user feedback to improve future releases.

## Exploratory Testing Approach

How I approach exploratory testing:
- Understand the context: About feature goals and feature workflows based on domain knowledge or explore with similiar apps.
- Focused Exploration: Use charters-based approach guide my exploration and ensure coverage of critical areas and constantly ask "what if" questions to uncover unexpected behaviors and edge cases.
- Notes: Document my observations, steps taken, and any issues found in real-time.
- Tool Assistance: Use browser dev tools, Postman tool to explore what happens behind the scenes
