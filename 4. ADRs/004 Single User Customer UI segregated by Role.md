# 4. Multiple UI Interface for each Sysops User Role

Date: 2021-04-29

## Status

Approved

## Context

Decision about the User/Customer UI design. There are 4 different Actors who work for Sysops Squad and 1 other Actor is Customer.

### Sysops Users

## Expert
## Admin
## Manager
## Customer Service
## Customer


## Alternatives

#### Single User/Customer UI segregated by Role

This is more favorable since this model allows re-use of components and easy to maintenance; however may not be good from 
security point of view (people trying to access the system beyond their Role).
Also, when development team needs to update the UI then it needed to regress other's as well.

#### Individual UIs for each

This solution was becoming more complex therefore hard to maintain; however this will provide a solution which is currently 
a problem where sometime system is not available for anyone even the internal staff.

## Decision

We will go for Individual UIs for each SysOps User Role, the common UI libraries will be used, so that common features 
like Authentication and Authorisation can be managed at single place.

## Consequences

Dev team need to maintain multiple UI code but will provide the decoupling which is badly needed to solve the current 
problem of System not available ALL users.
