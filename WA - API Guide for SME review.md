# What's New – WidgetApp API Guide 2.0
## Known Issues and Limitations 
### <span style="color: #1D2591;">Server Load Issues </span>
The new Streaming frontend (SFE) and streaming API processes have been found to add to the load on the server.

<span style="color: orange;">**SMEs:**</span> _I'm going to need a lot more info here. What kind of loads are we talking about? Are servers in danger of falling over? What is the solution for this? How do the Admins mitigate it if they receive a ticket for this?_
### <span style="color: #1D2591;">Existing Connections Stopped on SFE Restart</span>
When the WidgetApp Streaming frontend was restarted, it automatically stopped any *_stream* processes for existing connections.

<span style="color: orange;">**SMEs:**</span> _"Killed" (past tense) implies this has been fixed? Assuming this was a bug, What version was it fixed in and what was the fix? How do Admins address this issue if they run across it from previous versions? If it wasn't a bug, why are we mentioning it here?_ 
## What's New? 
### <span style="color: #1D2591;">Multiple Services can now Use the same Websocket</span>
The WidgetApp streaming API runs over Websockets. This allows different services to use the same websocket connection.
**Note:** The WebSocket API makes it possible to open a two-way interactive communication session between the user's browser and a server. Using websockets, you can send messages to a server and receive event-driven responses without having to poll the server for a reply.

<span style="color: orange;">**SMEs:**</span> _Again, I'm going to need a bit more info here. Is this a new feature? Have we only started using the Websocket API since the last release – were we using something else before now? Is this simply a reminder for the Admins. Help?_ 
### <span style="color: #1D2591;"> Robust Authorisation</span> 
Streaming API is authorised for approved user groups only. This is managed using OAuth2.0 access tokens.
*Note:* OAuth 2.0 (Open Authorisation) is the de facto industry standard for online authorisation. It provides consented access so applications can access the user's data without the disclosure of the user's credentials to the application. The API will grant access only when it receives a valid access token from the application.

<span style="color: orange;">**SMEs:**</span> _What were we using before? Can we give some tips for use here?_ 

---
For more details, see the WidgetApp 2022.r20 release notes.