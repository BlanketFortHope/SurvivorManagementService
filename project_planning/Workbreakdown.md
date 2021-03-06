1. Define Business Process
--------------------------
### 1.1. Define Roles/Business Owners
 * From a functional/Business perspective, define the following roles:
   - Participants: Take Action or own specific activities within the process :: Participants will become swimlanes in the resulting process maps.
   - Business Owners: Responsible for the outcome of a particular milestone or collection of activities
   - Stakeholders: External or Internal Participants in the process (includes customers, involved 3rd party actors, service providers, etc.)
   - Customers: Groups or individuals who derive or receive value from the activity being performed
   

### 1.2. Map Level 1 Process
 Level 1 Processes defined as high level milestones or functions of the business - For Example: Identify, Intake, Monitor/Manage, Discharge, Report. 
 
 Major activities within the level one process should be included as well as activity owners, inputs, outputs, dependencies, known risks or issues, policy/doctrine requirements, and general activity narrative.

### 1.3. Map Level 2 Processes

Level 2 processes break down each of the level 1 activities into their detailed steps. This shoudld include decision points, process variants, and exception handling. Any time/duration and activity  values should be included.

Also include required forms/signatures/approvals per activity.

### 1.4. Define Problems/Risks

In review of the level 1 and level 2 process map, consider any risks to the process. Risks may be technical, functional, process, data, communication, security, etc. In evaluating risk, consider the risk probability and impact along with the consequeces if the risk materializes and define a mitigation strategy to reduce likelihood/impact.


2. Define Database
------------------

### 2.1. Elements

### 2.2. Master Tables

### 2.3. Relationships

3. Define Backend
-----------------

### 3.1. Logical BP

### 3.2. Role Based Security

### 3.3. Establish API

#### 3.3.1. ID Data Required per View

#### 3.3.2. User Auth

4. Define Front End
-------------------

### 4.1. User Views

### 4.2. User Workflow

5. Define Architecture
----------------------
Work items that must be performed to do the initial software and infrastructure discovery for the application. Items on this list will require some research to determine what the best solutions are that balance:

* Cost
* Security
* Flexibility and Features

### 5.1 Determine Language
Language and hosting environments should be identified based on:

* Expertise of volunteers
* Available OpenSource/free resources to enable the capabilities listed in the architectural discovery section.

### 5.1. Architectural Discovery

Identify:
* Encrypted Key Store
  * Public Private Key Auth to encrypted key store
  * For storing encrypted parameters, connection information, private keys.
Once Programming language is determined:
* Web Hosting
  * Identify a solution for hosting the solution that will provide a minimum of hosting costs and maintenance requirements, while providing integration:
    * In-flight encryption
    * At rest encryption
* Database
  * At rest encrypted data-store

Optional Discovery Work:
* Two-Factor Authentication
  * Time-based one time password generation
  * SMS service for mobile phone Authentication

### 5.2 Identify Access Control Policy
* Identity Management Business Process
  * How users will be created.
  * How users will be given Access
* Open Source Identity Management Service
  * Deploy service and couple with identities
* Token based SAML

6. Project Management Plan

### 5.1 Determine Infrastructure

#### 5.1.2 Breakdown Budge Requirements

* Hosting Services Cost
* Domain Cost
* Certificate Authority

##### 5.1.2.1 Optional Additional Costs

* SMS service for communication and multi-factor phone authentication.

### 6.1. How the project is run

How work is divided: there should be a project manager (point person) for each step above who alerts the larger team when they can move to the next step. Project managers should continue to manage a list of critical bugs and a list of non-critical bugs. An issue should be created for any bug/group of related bugs.

How work is accessed:
Non-project managers should either consult a project manager or look to the issues list to work on important components of this project.

How it is accepted
* GitHub pull request review board
  * Who the reviewers will be:
  * This will require only certain people have access to directly push to the project
  * Any push to the project should be accompanied by a image or screenshot representing what the web tool looks like before and after changes submitted for review.
  * All volunteers should make sure that their edits are made to the most recent branch and thus do all they can to avoid submitting requests that create merge conflicts.
  * Issue will be closed by project managers specifically.

7. Release
----------

### 7.1. Define User Base

### 7.2. Create User Accounts

### 7.3. Go
