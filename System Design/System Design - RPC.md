**RPC** - A RPC is the ability of the client application to execute sub routine/task on the remote server.

#### Unique Features of the RPC

1. The remote method invocation looks like calling a normal location method. This is referred to as location transparency.
2. To the dev of the client application a method executed locally or remotely looks the same.
3. RPC framework support multiple langs. Application written in different langs can talk to each other using RPC
   
#### How RPC works

1. **Client Initiates Call:** The client (your application) wants to get something done. It makes a call to a function, just like it would call any other function in its code.
2. **Call Is Packaged:** The client's RPC library takes care of the details. It packages the function name, any arguments you provided, and other necessary information into a message.
3. **Message is Sent:** This message is sent over the network to the server. This could be over the internet, a local network, or even between processes on the same machine.
4.  **Server Receives and Executes:** The server receives the message, unpacks it, and figures out what function the client wants to run. It then executes that function with the provided arguments.
5.  **Results are Sent Back:** If the function produces any results, the server packages those results into another message and sends it back to the client.
6.  **Client Receives Results:** The client's RPC library receives the response, unpacks the results, and gives them back to your application code, as if the function had just finished running locally.
![[Pasted image 20240723200942.png]]


 
#### Drawbacks 

1. **Slowness** - The client never knows how long the method invocation will take