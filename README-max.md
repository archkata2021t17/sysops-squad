# sysops-squad

* the final product should be enough to pass to dev team to start implementing
* later need a video(?) presentation, if passed simefinals
* microservices - beware of distributed transactions, data dependency/migration
* no judging based on tech platfrom
* no need to specify particular tech platform, just type is enough (like pub/sub, queue, sync/async etc) unless smth like "gRPC has a unique specific feature which really makes a difference"


* it's a franchise, not a gloabal system. A city can have several of them.
* cost should be low, client is looking for value (bit no specific limitation)
* out of band migration is OK, no need to do it live
* volume of request  - 100 per day, 1000 per month, # of uses - 1000s
* users have monthly subscriptions (i.e. no users out of the blue, they should be logged in and paying)
* client has CI/CD
* single IT support team, no subdomains currently
* already have a mobile app for experts
* no need to reuse the existing code as it's considered a wreck
* The user processes can (should? must?) be improved/upgraded, no need to stick to the existing processes.

(stopped at minute 113 of the video)




Users:
* clients: enter tickets, pay subscriptions, feedback about service done
* experts: are assigned to tickets, do the job, report what's done, any additional cost (if hw needs to be replaced?)
* managers: superwise overall company performance
* admins: backend work (create users etc)
