# System overview

## Business goal

Business goal:

To improve the current Sysops squad by redesign or process re-engineering to make the system consistence and reliable

Fix the issues with Customer Ticket fallout.
Availability issue
Unresponsiveness 
Make the application consistentant and exit gracefully 
Fix the wrong assignement of Tickets

## Background:

Things have not been good with the Sysops Squad lately. The current trouble ticket system is a large monolithic application that was developed many years
ago. Customers are complaining that consultants are never showing up due to lost tickets, and often times the wrong consultant shows up to fix something
they know nothing about. Customers and call-center staff have been complaining that the system is not always available for web-based or call-based problem
ticket entry. Change is difficult and risky in this large monolith - whenever a change is made, it takes too long and something else usually breaks. Due to
reliability issues, the monolithic system frequently “freezes up” or crashes - they think it’s mostly due a spike in usage and the number of customers using the
system. If something isn’t done soon, Penultimate Electronics will be forced to abandon this very lucrative business line and fire all of the experts (including
you, the architect).


### System features and responsibilities

#### User Maintenance, Expert Profile
Sysops squad experts are added and maintained in the system through an administrator, who enters in their locale, availability, and skills.

#### Customer Profile, Support Contract, Billing System and History
Customers who have purchased the support plan can enter a problem ticket using the sysops squad website. Customer registration for the support
service is part of the system. The system bills the customer on an annual basis when their support period ends by charging their registered credit card.

#### Ticket maintenance, Ticket Route and assign
Once a trouble ticket is entered in the system, the system then determines which sysops squad expert would be the best fit for the job based on skills,
current location, service area, and availability (free or currently on a job).

#### Notification, Ticket Route and assign
The sysops squad expert is then notified via a text message that they have a new ticket. Once this happens an email or SMS text message is sent to the
customer (based on their profile preference) that the expert is on their way.

#### User Interface, Ticket Shared, KB Search
The sysops squad expert then uses a custom mobile application on their phone to access the ticketing system to retrieve the ticket information and
location. The sysops squad expert can also access a knowledge base through the mobile app to find out what things have been done in the past to fix the
problem.

#### KB Maintenance
Once the sysops squad expert fixes the problem, they mark the ticket as “complete”. The sysops squad expert can then add information about the
problem and fix to the knowledge base.

#### Survay, Notification
After the system receives notification that the ticket is complete, the system send an email to the customer with a link to a survey which the customer then
fills out.

### Numbers/Metrics
Volume of request 
- 100 per day, 
- 1000 per month, 
No. of uses - 1000s

### Users

#### Customers
The customer registers for the Sysops Squad service, maintains their customer profile, support contracts, and billing information. Customers
enter problem tickets into the system, and also fill out surveys after the work has been completed.

#### Administrators
The administrator user maintains the internal users of the system, including the list of experts and their corresponding skillset, location, and availability. The administrator also manages all of the billing processing for customers using the system, and maintains static reference data (such as supported products, name-value pairs in the system, and so on).

#### Technician
Experts are assigned problem tickets and fix problems based on the ticket. They also interact with the knowledge base to search for solutions to customer problems and also enter notes about repairs.

#### Managers
The manager keeps track of problem ticket operations and receives operational and analytical reports about the overall Sysops Squad problem ticket system.


## Out of scope

UI/UX Design 
