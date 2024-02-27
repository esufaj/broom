<div align="center">

  <img alt="Broom logo" src=https://rbcgithub.fg.rbc.com/PCC0/automation/blob/master/broom/logo/logo.png width="200px" height="200px" />

</div>

# Broom

## Description:
Broom is an RBC internal ticketing and exemption management system designed and created by me.


## Where Broom is deployed:
Two teams across RBCs Global Cyber Security (GCS) have currently been onboarded to Broom where four seperate Jira projects have been fully automated by the product. Below you can see a summary of the team that was onboarded and the Jira projects that were fully automated by Broom:
- Cloud Security Scanning: Cloud tickets
- Vulnerability Management Group: Cloud | TSS OS and IIS | Server Vulnerabilities tickets

Additional teams are currently being onboarded.

  
## Features
Broom supports a number of custom features for use by a member of the Jira project that has been onboarded to Broom. To use a feature, a user should simply leave an internal comment in the ticket the user wants the feature to be apply to. Broom will then scan the ticket for the feature keyword and process the ticket. It is important to note that these features only need to be used in certain cases when Broom requires additional approval or other considerations in the ticket. Below is a list of features and a brief description of what they do:

- **\#override**: Broom will ignore all verification checks and complete the ticket flow as defined for that specific project.
- **\#approved**: Allows Broom to proceed and complete the ticket when certain criteria has either breached or failed verification checks. In this case, Broom will send an email and tag project users in the ticket letting them know they must review the ticket and approve it if needed.
- **\#ignore**: Broom will not consider the ticket for processing.
- **\#temp \<DURATION\>**: Broom will create and apply rules and exemptions set to expire at a date that is some number of days in the future given in the <DURATION> tag.
- **\#global**: Broom will apply created rules and exemptions to teams across RBC globally for blanket coverage.
- **\#update**: Broom will update rules and exemptions with current data and extend expiry dates as detailed in an SQL DB that maintains those rules. This is not automatically completed considering the rules and exemptions being updated are time sensitive and need to be considered case by case. Broom will send an email and tag project users who can then approve Broom to update those details by leaving this keyword in the ticket.

Additional features to be onboarded per team request and feedback.

## Verification Checks
There are a number of verification checks that can be configured and customized on Broom for your Jira project based on how you want tickets to be processed, what actions Broom should take and any considerations that it should consider during processing. Currently, there are 24 unique verifications. Some of these checks include:
### Jira
- Jira ticket Data
- Jira Ticket Structure
- SQL DB Data
### Aqua Security:
- Docker Image Names
- VMs
- Repositories/Branches
- Audits
- Compliance
- Malware
- Blacklists
- Super User
- High or Critical CVEs
- Expiry Due Dates
### SCR Portal [internal tool]
- Platform Names
- Expiry Due Dates
- Comments
- Creation Dates
- Tech Names
- Plugin IDs
- Technology Numbers
- Severity
- Ticket IDs
- Remediation Owners
- Application Codes
- Rule IDs

Additional checks to be onboarded per team request and feedback.
