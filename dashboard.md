# Dashboard
_This feature is still under development and might be a little buggy, please help us by [reporting the issues](https://github.com/dudeee/dude/issues)_

 You will feel the need to send messages using your bot (He announces his own changes in our team!) and also monitor it's activity and received messages.
 
 The Dude dashboard gives you the ability to chat (send and receive simple messages) and send messages with custom parameters (attachments, etc). You can also read the logs and monitor memory and cpu usage of your bot, along with error/rejection rate.
 
 ![Dashboard - Chat](Screen Shot 2016-05-18 at 11.22.49.png)
 
 The dashboard uses a messaging channel to communicate with your Dude channel. In order to use the dashboard you have to first run your dude process. Let's try it!
 
 ```bash
 npm start;
 ```
 Switch to another tab and do:
 ```bash
 npm run dashboard
 ```
 
 ![npm start || npm run dashboard](Screen Shot 2016-05-18 at 11.27.26.png)
 
You can access different tabs (logs, stats, message, chat) and quit by un-focusing (press esc) and typing the first letter of the tab (e.g. `s`).

![Stats](Screen Shot 2016-05-18 at 11.30.26.png)