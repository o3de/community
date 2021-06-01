**SIG Testing QA Charter**

This charter adheres to the Roles and Organization Management specified in <sig-governance>.
 Team information may be found in the <readme.md>

**Overview of SIG**

Provide quality assurance bars for testing involved for quality.
set expectations for the quality bar

Two concise lines explaining what this SIG does with bullet points of the major responsibilities

- Responsibility 1

**Goals**

- Major goals that SIG seeks to generally achieve

**Scope**

* Provide AR automated review framework
* Develop and maintain testing framework
* Develop and maintain the rules and code for prevalidation scripts
* Develop and manage the platforms supported in the framework for coverage
* Invocation and management of asset processing framework for tests to run (questioned other SIGs)
* Discovery, scheduling, node sizing, and harness invocation of test cases with result reporting  (build team question)
* Define and maintain guidelines for requirements of test nodes
* Define and maintain database of standard tags and test cases 

**In scope**

* Any testing that tests the framework itself or its tools 
* Responsible to maintain and define versions used for LYTest tools, google test and related tools
* Design and maintain jenkins code and configuration (Move to Contrib/Dev Workflow?)
* Design and maintain scripts executed by jenkins for the framework (Move to Contrib/Dev Workflow?)
* Define KPI and SLAs for test metrics
* Creation and reporting of metrics to devstats dashboard and related systems related to QA stats
  * Documentation of prioritization of test cases, define categories and actions for each
  * Perform Testing across platforms in both automated or manual forms, but not responsible for development of invocation scripts per platform.
  * Provide performance and ensure meets the minimum defined accepted quality bar
  * Define and provide guardraids of minimum accepted quality experience and performance 
  * Define SLA of action on discovery of issues found.
  * Maintain bug test database for purposes of test cases and bugs.
  * Maintain and define stabilization of test cases to ensure tech debt limits are not exceeded. 
  * Periodic reviews of test cases and collateral
  * SLA to define frequance of maintance of test stabilization
  * Define quality bar of branch marked for release potential
  * Responsible for all other forms not defined in functional testing in or out of automation, but not responsible for the test code written by other SIGs or community (or maintain / write)

**Cross-cutting Processes**

* Provide guidelines and procedures around manual testing models to work with SIGs
* Provide guidelines and procedures around automated testing methods.
* Provide automated root cause analysis of failed tests to SIGs
* Provide information and mitigation steps for tests that break another unrelated area.
* Define mechanism and procedures to escalate to disable test failures

**Out of Scope**
 
* Not responsible for writing tests for code - 
* Not responsible for specific scripts that operate under the toolchain or framework
* Not directly responsible for manual testing, but may provide assistance or guidance to SIG teams to do manual testing of features.
* Not responsible for development of asset processing extensions 
* Not responsible for the provisioning of test node infrastructure, but may advise teams on how to implement extensions

**SIG Links and lists:**

- Joining this SIG
- Slack/Discord
- Mailing list
- Issues/PRs
- Meeting agenda & Notes

**Roles and Organization Management**

SIG Docs adheres to the standards for roles and organization management as specified by <sig-governance>. This SIG opts in to updates and modifications to <sig-governance>

**Individual Contributors**
Code must be included with a description of the test case requirements
++ Define number of tests and tagging test cases to determine if can be done in parallel or special case, or sequence, or impacts to other test cases.
++ Must follow debug guidelines - get docs from nusrath on guidelines


**Maintainers**

Additional information not found in the sig-governance related to contributors

**Additional responsibilities of Chairs**

Additional information not found in the sig-governance related to SIG Chairs

**Subproject Creation**

Additional information not found in the sig-governance related to subproject creation

**Deviations from sig-governance**

Explicit Deviations from the sig-governance
