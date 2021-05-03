ADRs - Big bang vs Phased Migration


Date: 2021-05-02

## Status

Approved

## Context
SysOps squad is an existing application with a number of issues. Also any change / fix in the current application code takes too long and breaks something else. To get rid of these issues, we have proposed a new architecture. Now we need to decide if we should change few components at a time or all components at once.


## Alternatives

#### Phased Migration
In general Phased migration of one or few components at a time seems like a safe approach. However here it could become error prone since there has been a history of things getting broken with every change. Also it would result in code duplication, since a special arrangement has to be worked out for the migrated components every release.

#### Big bang Migration
Big bang migration, i.e. migration of the entire application to the new architecture with an automated test regression suite that covers all the functionality, seems less complex and will get us sooner with fewer issues. Many of the existing components will be refactored to work as a separate service with its own database. To further mitigate the risk, we could run the old and new applications in parallel, with both receiving the requests and run tests that compare the results between the old and new applications.

## Decision
Big bang migration


## Consequences

The decision to go for Big bang migration should allow us to get to the new architecture sooner. The automation regression suite is a critical component that should make it possible, and hence needs appropriate focus and investment. Also, a test suite to compare results of new application with that of the old application, needs to be built.
