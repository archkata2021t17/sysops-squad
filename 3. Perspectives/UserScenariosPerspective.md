# Important scenarios
## Ticket creation

### Stakeholders
* Customer - Interested in entering a ticket the fastest and easiest way, get it assigned to experts, and executed in a timely fashion
* Expert - Interested in receiving available tickets to execute and be paid for those
* Helpdesk/Admin - Interested in most automation and error-proof process

### Risks

* Login service can be down (not shown here) - it's duplicated under load-balancer cluster
* Appliance service can be down - the Customer can't see a list of models and pick his model. Solutions:
  * The Customer UI service has a cache of appliances, so the problem is only if there is a new model not yet propagated to the cache.
  * For that unlikely scenario, Customer can always use a free-text to specify a model
* Payment service can be down - we don't know if Customer has paid his monthly subscription charge. Solutions:
  * Cache for the paid customers in the Ticket service - only the the unlikely case that the Customer paid while the Payment data service was down gives trouble
  * If the payment data is not in the cache - the ticket is still created but flagged for the Helpdesk attention who will either resolve the problem on the backend or contact the Customer and resolve the issue with them directly
* Hard to implement a good algorithm to match Experts to tickets. Solution:
  * Let Experts see the available tickets matching their skillset, and match themselves to a ticket (we call it "UBER model"). This insentivises the Experts to reply to tickets faster and have more tickets done.
* No Experts matched for a ticket. Solution:
  * Wait the match to happen within pre-configured time. If it takes too long, then
  * Helpdesk/Admin/Manager takes care of the communication with the available Experts to get the ticket assigned.

## Ticket-to-expert matching
## Ticket execution (visits)
