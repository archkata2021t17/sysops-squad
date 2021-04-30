# Risks

## Business related risks

@TODO

## Technical Risks

* With microservice architecture, any of the services can go down - it shouldn't bring the whole system down. Additional means like caching can be used to reduce mutual availability requirements.
* When the system is distributed, the transactions become distributed as well. Integrity can be difficult to ensure.
* Third-party services (messaging, maps) can go down - need to think of alternatives. If we don't have contracts with those services for the company consumption, and rely on users to use the services themselves (e.g. their own Google Maps on their devices), then we need to think of backup systems (e.g. Yahoo Maps). Also, some services might classify the usage as corporate and switch off or pin down.

# Sensitive points

## Business related

@TODO

## Technical

@TODO
