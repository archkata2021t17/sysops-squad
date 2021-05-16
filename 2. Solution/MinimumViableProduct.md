# Minimum Viable Product

If the client's situation doesn't permit to full-blown upgrade (from the cost or development time perspective), it can go with a Minimum Viable Product (MVP).

Here is how it will be if the client is willing to take this approach.

1. The Ticketing flow is fully migrated to the new architecture - it's essential
2. The Knowledge Base is scraped from the Monolith
  * It is just text and (probably) images
  * It's detached from everything else
  * Solution: The fastest and cheapest is to migrate it (as a database) to a stand-alone Wiki server and left as is for Experts to use/search/update. It's deactivated in the current Monolith.
4. The Reporting Component stays
  * it's only used by the managers and has no requirement for high availability
  * it only needs the data from the respective DBs
  * Solution: there will be written a script that will extract the necessary data from the microservices databases, and put in the Monolith DB, after that the Reporting module can be fired.
5. The Payment Component stays
  * Only information needed for the Ticketing flow is if a Customer is covered for this specific date.
  * Solution: have a simple way (like a DB trigger) to feed the "customer paid until this date" to the new architecture
