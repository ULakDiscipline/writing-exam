# What's New – WidgetApp Administrator Guide 2.0
We're constantly working to improve your Anonymous experience with fixes, improvements, and new features to help your users and your team. Here's a summary of our recent changes:
## Housekeeping / Reminders
### <span style="color: #1D2591;">Superior User Experience</span>
Most user actions, such as searching (using the search bar for immediate query suggestions or autocomplete) or scrolling through a page are implemented by calling ajax/ endpoints. 
This provides a seamless user experience because AJAX communicates with the server without refreshing the web page, providing better performance.
### <span style="color: #1D2591;"> Authentication</span>
The way WidgetApp authenticates user information remains unchanged from previous versions of the application.  Authentication is managed through the existing WidgetApp frontend (WFE). Any management, diagnosis or troubleshooting should be managed through the client-side.
## What's New! 
### <span style="color: #1D2591;">WidgetApp Streaming Frontend</span>
<span style="color: orange;">**SMEs:**</span> _This sounds like a big deal. Is there some introductions/context we can supply for the Admins here?_

The WidgetApp frontend (WFE) handles existing API requests as per previous versions. However, the WFE will now hand over to the new Streaming frontend (SFE) for any authorised connections using the new Streaming API. The SFE then manages the session as per WFE, but with Streaming API capabilities.
#### What are the capabilities of the new SFE? 
A detailed overview of the WidgetApp SFE can be found in the _WidgetApp Administrator's Guide_, which includes detailed descriptions and use cases of the following: 
* Registration of Users
* User Information
* Privacy Preferences
* Search Capability
* Interactive UX
* Ratings and Reviews
* Screen Sharing

### <span style="color: #1D2591;">Restarting Streaming frontend Instances</span>
To restart **_sfe** instances use the following format: 
~~~~
widgetapp_admin -process _sfe -n {num_instances} -start
~~~~
### <span style="color: #1D2591;">External System Port Usage</span>
For external systems to use SFE, they must listen on port 200 for stream messages such as: 
* widgetApp_useraction_xxx APIs (widgetApp_useraction_refresh()
* widgetApp_useraction_edit()

<span style="color: orange;">**SMEs:**</span> _Do we mean TCP or UDP Port here? And does it matter? I'd like to provide more context, if possible._
### <span style="color: #1D2591;">Default on Startup</span>
The default is for one Streaming Frontend (SFE) to run on startup. Another will be started in parallel for every 10 streaming API clients.  
#### What are the benefits of this? 
<span style="color: orange;">**SMEs:**</span> _I'd like to know why this is important/beneficial. Does it streamline performance? Mitigate errors? Is it simply best practice? Why am I mentioning this here?_  
## Troubleshooting
### <span style="color: #1D2591;">Processes Using Memory</span>
* **Possible issue:** It is advised to monitor both **_sfe** and **_stream** processes for any issues involving CPU and memory. Both processes have been found to sit at or above 50% usage. 
* **Solution:**  Restart any processes that approach >~50% memory usage and monitor.

### <span style="color: #1D2591;">Key Terms</span>
The following terms are used throughout this guide. For more information about terminology, see the [glossary].
* **AJAX** (Asynchronous JavaScript and XML). A set of tools used to make calls to the server to fetch some data. AJAX is typically a set of client-sided web development techniques. 
* **WidgetApp frontend (WFE)**.  SME definition required.
* **WidgetApp Streaming frontend (SFE)**.  SME definition required.


[glossary]: http://www.reddit.com 
[release notes]: http://www.reddit.com 
--- 

  
> For more details, see the WidgetApp 2022.r20 release notes.
