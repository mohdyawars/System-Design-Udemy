Types of API:

1. **Public API** - These are the APIs that are available to general public, good rule is user must sign up for API that they want to use. And then the system should provide them access to make the requests for API.
2. **Private API** - These are the APIs which are exposed within the company only. Team can take advantage of this API to make a robust system. These APIs doesn't expose our system to the outside world.
3. **Partner API** - Similar to the Public APIs. These are exposed only to the users which have businesses with us.
   
Best Practices to design an API:
1. **Complete Encapsulation** - It means that client should not have understanding of how our API is implemented. Client should use only the end product i.e. API. API should be separate from our internal design  and implementation. We can change the design later without breaking the contract with our clients.
2. **Easy to Use** - API must be easy to understand, impossible to misuse. Only one way to get certain data / perform a task. Descriptive names for actions and resources. Exposing only the info and actions that users need.
3. **Keeping the operations Idempotent** - "An operation doesn't have any additional effect on the result if it is performed more than once". For e.g multiplying bunch of 1's in the result we would get only 1, same is the case for API if we send multiple identical request only the first request will make a change in the system and all the following requests will not make any changes to the system.
4. API Pagination - It is important when a response from our system to the client request contains a very large payload. Without pagination most client applications will not be able to handle big responses, results in a poor user experience. 
5. Asynchronous Operations - A client application receives a response immediately without having to wait a final result for e.g one API is running a report on large CSV file if it is an async API client will get the response Report started processing and this function is sent to celery. To track the result of this operation client will get the **task_id** or some identifier to track this task.
6. Versioning our API - By this we can keep two versions of the API at the same time and deprecate the older version gradually

[[System Design - RPC]]