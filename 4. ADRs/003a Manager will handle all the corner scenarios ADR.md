# 3a. Manager will handle all the corner scenarios

Date: 2021-04-29

## Status

Approved

## Context

This decision is an extension of decision [001 Will Use Uber Model]
This decision talks about the Tickets which doesn't cover by any Expert (e.g. may be location is quite far away like suberbs etc.)  

## Alternatives

#### Auto Assign by Sysops Sqad System

If customer Ticket is not picked up by any of the Expert since the area is not covered by any expert e.g. Suberbs etc. System will wait for a configured time and then further assign it to relevant Expert.

#### Manually Assign by the Manager

Since this sitation is a clear corner case of loosing the ticket - this needs to be handled by Manager so that he can make sure ticket is handled properly and customer is managed properly.

## Decision

Clearly, this is solving the current problem where tickets are getting lost - we decided that Manager will took additional responsibility to manage these corner cases (left after implementation of Uber self assignment model).

## Consequences
Manager may need to set a side a time to handle these activities along with current activities assigned to him.
