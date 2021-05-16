# Business Drivers

## Business goal:

Business goal:

To improve the current Sysops squad by process re-engineering or redesign to make the system consistence, reliable and customer centric

## Business Drivers (BD)

Loosing business, regular complaints from customers, not sustainable due to losses

| # | Business Driver |
|----|----|
| BD.001 | Changes to the system must be quick, easy and non disruptive 
| BD.002 | Zero Customer's Ticket loss
| BD.003 | 100% correct assignment of tickets to relevant Experts
| BD.004 | The system must be highly available to Customers (internal/external)
| BD.005 | Resolve the frequent system crash
| BD.006 | The system must be responsive during the peak business hours


## Significant Architectural Requirements (SAR)

List of architecture driving requirements (primary functional, quality attribute, and life-cycle requirements)

| # | Significant Architectural Requirements | From BD |
|----|----|----|
| SAR.001 | Migrate Monolith application to microservice architecture                       | BD.001                 |
| SAR.002 | Create a CI/CD pipeline for automatic build, test, deploy in all environments   | BD.001                 |
| SAR.003 | Add Automated Regression Test Suite as part of CI/CD                            | BD.001                 |
| SAR.004 | Re-design the Ticketing system module                                           | BD.002, BD.003         |
| SAR.005 | Deploy the system in Highly available mode                                      | BD.004, BD.005, BD.006 |
