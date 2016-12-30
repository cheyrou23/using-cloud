##Evaluating Trello

June 2016

Read this guide to understand the risks and mitigations when using Trello.

We assessed Trello Enterprise using the [Cloud Security Principles](https://www.gov.uk/government/publications/cloud-service-security-principles/cloud-service-security-principles) as a guide.  We have also included recommendations in areas where customers can further reduce the risks to their information.

This guidance is suitable for UK government organisations operating at OFFICIAL but is not intended to inform your organisation's buying decisions.

We aim to support the adoption of cloud-based applications in government.  If you are concerned that this guidance won't help you do that please contact us.

>Trello meets the objectives of the Cloud Security Principles in most areas *but there are several areas* where organisations should have technical or policy protections in place to prevent data loss

### Assessing against the Cloud Security Principles

#### 1. Data in transit protection

>Trello meets the objectives of this principle

* connections to trello.com are encrypted between the browser and the trello.com web servers using TLS. The web servers support a [good cryptographic profile](https://www.gov.uk/guidance/transport-layer-security-tls-for-external-facing-services)

* connections to trello.com APIs are encrypted in the same way

Trello meet the requirement through:

* supplier assertion of commercial statements

* independent technical assessment

When making the assessment we found:

* the web server supports a good TLS configuration but an old or poorly configured browser could still compromise information

* deprecated versions of SSL are not supported

* we were not able to test how data was protected in transit within the service

Our independent validation of the TLS configuration was performed in April 2016 and only covered the servers that we were able to reach at the time.

>Recommendation: Customers should ensure that their browsers and mobile applications enforce secure connections using TLS 1.2 or better

#### 2. Asset protection and resilience

>Trello meets the objectives of this principle

* all information is hosted Amazon Web Services (AWS) data centres in the United States and is subject to US law

* data centre locations are certified to ISO27001 and PCI-DSS

* Trello is hosted in three AWS EC2 Availability zones, including hot mirrors, so failures would recovery in real-time

* the third zone is replicated on a one-hour delay and would only be used in the event of a failure in the other two zones 

* Trello have Model Contract clauses available for customers exporting personal data outside the EU to the US (see Cabinet Office [offshoring guidance](https://ogsirooffshoring.zendesk.com/hc/en-us/article_attachments/202389402/Offshoring_Information_Assets_Classified_at_OFFICIAL_v1.1.pdf))

* we have no information on Amazon equipment disposal policies

Trello meet the requirement through:

* supplier assertion and contractual commitment of commercial statements

* independent technical assessment

When making the assessment we found:

* Trello cards are not encrypted at rest

* file attachments on cards are encrypted at rest and stored on AWS

* the loss of the hot mirrors would result in a one hour data loss

* the loss of all three Availability zones would require result in a loss of 24hr of data

* a backup snapshot of the primary database is taken once every 24 hours and stored for up to 90 days

* data is destroyed at the end of a contract at the customer's request

>*Recommendation*: ask Trello to destroy your data if you leave the service

#### 3. Separation From Other Consumers

>Trello partially meets the objectives of this principle

* Trello is hosted on the AWS EC2 public cloud environment which is a multi-tenant

* the service is certified against ISO27001:2013 and PCI-DSS standards

* Trello assert that their staff policy only allows access to customer data when the customer has given prior permission

Trello meet the requirement through:

* supplier assertion of commercial statements

When making the assessment we found:

* Trello assert that they perform IT Security Health Checks but we have not seen the results of these tests

* Trello will provide summaries of the latest penetration tests and vulnerability scans to customers on request and under the terms of a non-disclosure agreement	

#### 4. Governance framework 

>Trello does not meet the objectives of this principle

* Trello have not provided any information on their security governance functions.

#### 5. Operational security

>Trello partially meets the objectives of this principle

* enterprise customers can report incidents to Trello Customer Support during office hours by phone or email

* Trello assign a severity level (SVR) ranging from 1 (complete service outage) to 4 (minor/cosmetic fault)

* Business Class users can access Trello support via email.

* free Trello users can access customer service, but at a lower priority to paid users

Trello meet the requirement through:

* supplier assertion of commercial statements

When making the assessment we found:

* Trello aim to provide a temporary resolution to SVR1 incidents within 4 hours for Enterprise customers with a permanent fix in place within 7 hours

* minor issues assessed as SVR4s are resolved at Trello's discretion

>_Recommendation_: Buy Business or Enterprise Trello if you need reliable support

#### 6. Personnel security

>Trello meets the objectives of this principle

* Trello perform background checks on staff who have access to customer data, including Social Security number traces, address history, US criminal records checks, and a check against the US domestic terrorist watch list.

* staff without access to customer data do not undergo any security clearance.

Trello meet the requirement through:

* supplier assertion of commercial statements

#### 7. Secure development

>Trello partially meets the objectives of this principle

* Trello assert that their Change Management processes ensure that code and system configuration changes are peer-reviewed for functional and security concerns before deployment.

Trello meet the requirement through:

* supplier assertion of commercial statements

#### 8. Supply chain security

>Trello partially meets the objectives of this principle

* Trello have contracts with third party suppliers to make sure security controls are compatible Trello's

* We have seen any of these contracts.

Trello meet the requirement through:

* supplier assertion and contractual commitment of commercial statements

#### 9. Secure consumer management

>Trello partially meets the objectives of this principle

* Trello [boards](https://trello.com/guide/board_basics.html) are private by default, however customers can expose boards to other trello users or to the public.

* Administrators can control visibility settings available to their users.

Trello meet the requirement through:

* supplier assertion of commercial statements

When making the assessment we found that:

* although there is no specific management interface in Trello, all customers can employ 2FA for their accounts

* for the business class offering, there are three user roles:

 * team member
 * team admin
 * board admin

Of these, the team admin is most powerful as they can add and remove boards and board admins, as well as being able to view all boards including ones which have been set to private.

>*Recommendations*:
> * admins should have a separate account for their day-to-day work
> * keep boards private unless you need to make them public
> * admin roles should be used sparingly

#### 10. Identity and authentication

>Trello partially meets the objectives of this principle

* sign on is via username and password. There are no enforced complexity requirements for the password. 

* two factor authentication using Google 2FA using mobile devices is available for all users.

* user accounts are entirely managed by customer administrators

Trello meet the requirement through:

* supplier assertion of commercial statements

When making the assessment we found that:

* customers using Google Apps can synchronise their accounts with Trello Business Class and Trello Enterprise and use them for authentication via an API

* Trello use cookies to persist user sessions when browser sessions are closed.

* single sign on is available for Trello Enterprise customers using SAML v2.0 compliant providers.

>*Recommendations*: customers should use strong passwords that meet corporate password policies, make sure users log out when they have finished using Trello.

#### 11. External interface protection
>Trello meets the objectives of this principle

* Trello have undertaken an independent penetration test

* Trello offer a Bug Bounty program and have an online relationship with independent security testers through hackerone.com, which provides some assurance that vulnerabilities are being actively addressed

* customers can employ two-factor authentication

Trello meet the requirement through:

* supplier assertion of commercial statements

When making the assessment we found that:

* we were not able to review the results of the penetration test.

#### 12. Secure service administration

>Trello partially meets the objectives of this principle

* some Trello Operations staff have full operational access to customer information. 

* they are prevented from having ad-hoc access by policy.

* activity is logged and audited, with intrusion detection systems to alert for unusual activity performed on customer information.

Trello meet the requirement through:

* supplier assertion of commercial statements

When making the assessment we found that:

* customers should assume that Trello operations staff could access their data.

#### 13. Audit information provision to consumers

>Trello partially meets the objectives of this principle

* some audit information, such as additions, modifications and deletions of data, are available to customers.

Trello meet the requirement through:

* supplier assertion of commercial statements

When making the assessment we found that:

* audit information is available in the customer interface of via an API.

>*Recommendation*: customers should use audit options in Trello to have visibility of user activity on their information.

#### 14. Secure use of the service by the consumer

>Trello partially meets the objectives of this principle

* Trello has three types of user permission: Team Admin, Board Admin and Normal user.

* Team Admin users have full access, including user access management functionality. Board Admins have full access to Board data.

* Business Class and Enterprise users can apply more granular security controls to apply different permission to team members.

* Trello's free edition does not include any administrative controls.

Trello meet the requirement through:

* supplier assertion of commercial statements

### Read more about trello

Trello publish [security](https://trello.com/security) and [privacy](https://trello.com/privacy) pages and a list of security issues via a [Hackerone page](https://hackerone.com/trello).
