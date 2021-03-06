# 5. Use the current Mobile App for the Experts

Date: 2021-04-29

## Status

Approved

## Context

Decision for re-using the current Mobile app with update of self assigning the tickets.

## Alternatives

#### Use the current Mobile App for the Experts

##### Positive points

With ease of updates to the Mobile application, we can continue using the Mobile app. Experts are already familiar with 
Mobile App.

New update will give them confidence and self management.

It will help in Ticket Notification

##### Negative points

Unclear how easy to decouple the current Mobile App from the monolith and point to the new architecture. If APIs are not
 well thought and segregated, if the code of Mobile App depends on specific replies from the monolith 
 (coupled to its inner working), then it might be not worth the effort.

#### Use the Omni channel browser based UI for Experts

We have the devs who will work on Web UIs for all other roles, they can take over the Expert Mobile App functionality 
to the web, and to some extent replicate the behavior.

The firm is not focusing on best mobile experience for Experts, so it's OK to give them a completely new web-based 
experience (which can be even better than the old one)

## Decision

We agreed to go ahead with Use of the current Mobile App for the Expert with reasonable modifications.

## Consequences

Already described above as positives/negative points.
