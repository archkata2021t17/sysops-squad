### Pre-requisites
1. Automated regression test suite.

### Migration Approach
1. The first service to be migrated is the "Ticket Service". Followed by one micro-service at a time.
This is only service, which has functional changes as per solution design.
1. The migration will be based on 'phased delivery' for each micro-service.
1. The Strangler Pattern will be used. The monolith will be decommissioned after six months of successful run of the last micro-services.
1. Another benefit of Strangler Pattern is that the expected downtime is minimal, still the initial few
deployments will be done during non/low business hours.
1. Below steps will be followed for each microservice deployment in production environment.   
   1. The monolith application will be stopped
   1. Any running microservice will be stopped.
   1. Database of the new deploying microservice will be migrated from old to new DB.
   1. Microservice will be started followed by the monolith application.
   1. Post deployment smoke test.


<s>* Downtime is OK, so we can:
  * take the current system down,
  * do the data migration (shouldn't be big -- clarify??? how many tickets there already?)
  * Run QA UI to ensure the new system works (need all the key test cases ready)
  * Bring the new system live
</s>
----
Existing to new Components Mapping

| # | Existing Systems's Component | New System's Component | Action |
|----|----|----|----|
|1.  | Login                 | Login Service         | Rename of the service                         |
|2.  | Billing Payment       | Billing Service       | Merged into new service                       |
|3.  | Billing History       | Billing Service       | Merged into new service                       |
|4.  | Customer Notification | Notification Service  | New Service for all notifications             |
|5.  | Ticket Notify         | Notification Service  | New Service for all notifications             |
|6.  | Survey Notify         | Notification Service  | New Service for all notifications             |
|7.  | Customer Profile      | Customer Service      | Merged into new service                       |
|8.  | Support Contract      | Customer Service      | Merged into new service                       |
|9.  | Expert Profile        | Expert Service        | Rename of the service                         |
|10. | KB Maintenance        | KB Service            | Merged into new service                       |
|11. | KB Search             | KB Service            | Merged into new service                       |
|12. | Reporting             | Reporting Service     | Rename of the service                         |
|13. | Ticket Shared         | Ticket Service        | Merged into new service                       |
|14. | Ticket Assign         | Ticket Service        | Changed ticketing business process -> ADR.003 |
|15. | Ticket Route          | Filter Service        | Redesign functionality                        |
|16. | Survey                | Survey Service        | Merged into new service                       |
|17. | Survey Template       | Survey Service        | Merged into new service                       |
|18. | User Maintenance      | User Service          | Rename of the service                         |

![Mapping of components](./img/ServiceMapping.png)

## Database mapping
| # | Existing DB Table | New DB |
|----|----|----|
|1.  | ss.Customer                   | Customer DB, Billing DB, Ticket DB, Survey DB |
|2.  | ss.Customer_Notification      | Notification DB, Customer DB  |
|3.  | ss.Survey                     | Survey DB, Report DB  |
|4.  | ss.Survey_Question            | Survey DB  |
|5.  | ss.Customer_Survey            | Survey DB, Report DB  |
|6.  | ss.Customer_Survey_Question   | Survey DB  |
|7.  | ss.Customer_Survey_Response   | Survey DB  |
|8.  | ss.Billing                    | Billing DB, Report DB |
|9.  | ss.Contract                   | Billing DB, Report DB |
|10. | ss.Payment_Method             | Billing DB |
|11. | ss.Payment                    | Billing DB |
|12. | ss.SysOps_User                | Expert DB, Ticket DB, Notification DB, Knowledge Base DB, Report DB, Survey DB, Expert Shortlist DB, User DB  |
|13. | ss.Profile                    | Expert DB, Report DB, User DB  |
|14. | ss.Expert_Profile             | Expert DB, Expert Shortlist DB, Report DB  |
|15. | ss.Expertise                  | Expert DB, Expert Shortlist DB, Report DB  |
|16. | ss.Location                   | Expert DB, Expert Shortlist DB  |
|17. | ss.Article                    | Knowledge Base DB, Report DB  |
|18. | ss.Tag                        | Knowledge Base DB  |
|19. | ss.Keyword                    | Knowledge Base DB  |
|20. | ss.Article_Tag                | Knowledge Base DB  |
|21. | ss.Article_Keyword            | Knowledge Base DB  |
|22. | ss.Ticket                     | Ticket DB, Report DB  |
|23. | ss.Ticket_Type                | Ticket DB, Report DB |
|24. | ss.Ticket_History             | Ticket DB, Knowledge Base DB, Report DB  |
