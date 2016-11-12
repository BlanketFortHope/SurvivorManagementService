1. Define Business Process
--------------------------

### 1.1. Define Roles/Business Owners

### 1.2. Map Level 1 Process

### 1.3. Map Level 2 Processes

### 1.4. Define Problems/Risks

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

* Database encryption
  * Storing connection string and public/private creds in encrypted key store.

# Infrastructure
* Web Server
* Data Base
* Encrypted Key Store
  * Public Private Key auth to encrypted key store
* Two-Factor Authentication
  * Time-based one time password generation
  * SMS service for mobile phone Authentication

* Access Control Policy
  * Identity Management Business Process
    * How users will be created.
    * How users will be given Access
  * Open Source Identity Management Service
    * Deploy service and couple with identities
  * Token based SAML

# Technical Budget Requirements

* Hosting Services
* Domain Cost
* Certificate Authority

### 5.1. Est. Physical Arch.

### 5.2. Logical Arch.

### 5.3. ID Sec. Controls

### 5.4. Define Access and Authentication Parameters

### 5.5. Define Physical Controls

6. Project Management Plan

### 6.1. How the project is run

How work is divided: there should be a project manager (point person) for each step above who alerts the larger team when they can move to the next step. Project managers should continue to manage a list of critical bugs and a list of non-critical bugs. An issue should be created for any bug/group of related bugs. 

How work is accessed: 
Non-project managers should either consult a project manager or look to the issues list to work on important components of this project. 

How it is accepted
* GitHub pull request review board
  * Who the reviewers will be:
  * This will require only certain people have access to directly push to the project
  * Any push to the project should be accompanied by a image or screenshot representing what the web tool looks like before and after changes submitted for review. 
  *All volunteers should make sure that their edits are made to the most recent branch and thus do all they can to avoid submitting requests that create merge conflicts.
  *Issue will be closed by project managers specifically. 



7. Release
----------

### 7.1. Define User Base

### 7.2. Create User Accounts

### 7.3. Go
