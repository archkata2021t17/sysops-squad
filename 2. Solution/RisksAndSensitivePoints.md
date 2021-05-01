# Risks

## Business related risks

* The Customer UI is down - loss of customer/revenue
  * Option: Multiple DNS entry points, 2 load balancers in different clouds (AWS/MS)
* The Customer UI is up but shows stale data - possible loss of customer
  * Option 1: leave to manual process with Helpdesk
  * Option 2: identify what exactly is stale and what parts still work, maybe tickets can be entered/processed in some reduced form and enriched by the Helpdesk later - notify the customer later
  * Option 3: if the customer not in a hurry, allow setting up a notification when the UI is fully back
* The Customer can't find his particular model in the list of supported modules - loss of customer/revenue
  * Option 1: leave to manual process with Helpdesk
  * Option 2: allow entering customer's model as free form, to be resolved by experts/helpdesk, with a related warning
    * If resolved, the model is added to the list of supported models
* The customer paid but the data is stale so he can't enter the ticket - loss of customer/revenue
  * Option 1: leave to manual process with Helpdesk - still possible loss
  * Option 2: Allow customers enter tickets even if they haven't paid, to resole the payment status later with helpdesk
    * Risk of DDOS with unactionable tickets
* The ticket is in pending state for too long (no assigned Expert) - loss of customer/revenue
  * Option 1: after configured pending time, Helpdesk/Admin/Manager decide with Experts directly who's gonna action
  * Option 2: automatically raise the Expert fee for taking long pending tickets
    * Risk of abuse by Experts
  * Option 3: add a notion of "urgent" ticket, with additional fee on Customer
    * Risk of abuse by Experts
* For a ticket, there are available Experts but their available timeslots don't match any of Customer's timeslots
  * Option 1: the ticket will stay in a pending state, use the pending ticket process
  * Option 2: Let Customer know about available Experts' slots, maybe the Customer will adjust his slots to be serviced earlier/faster
* 

## Technical Risks

* With microservice architecture, any of the services can go down - it shouldn't bring the whole system down. Additional means like caching can be used to reduce mutual availability requirements.
* When the system is distributed, the transactions become distributed as well. Integrity can be difficult to ensure.
* Third-party services (messaging, maps) can go down - need to think of alternatives. If we don't have contracts with those services for the company consumption, and rely on users to use the services themselves (e.g. their own Google Maps on their devices), then we need to think of backup systems (e.g. Yahoo Maps). Also, some services might classify the usage as corporate and switch off or pin down.
* Migration can fail - should be ready to switch back to the existing system.

# Sensitive points

## Business related

@TODO

## Technical

@TODO
