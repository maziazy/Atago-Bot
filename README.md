Atago Bot
==============

This is an android anjian script bot for "utsushiyo no tobari".
The subject of this bot is to automatically complete the redundant tasks in the game.

TL;DR
--------------
 - Import the "Atago-Bot.mqb" file into your android anjian application
 - (Optional) Set the state varible in main() as the state when you start the script
 - (Optional) You may need to fix to findPic() issue yourself

 
Import the script
--------------

You can import the "Atago-Bot.mqb" file into your android anjian application, or using the desktop version to upload it to your mobile. **To be noticed**, the anjian application needs root privilege to work and I cannot promise anything about this. You should take the risk by yourself.
After you import the script, you should edit the script a little bit according to your requirement.


The thing you should know about the script
--------------

The script is written in the finite state machine fashion, that means the process of the game would be divided into several *states* (e.g. home screen, party list screen). The most important thing is **set the state variable in main() as the state when you start the script**. The default state is "Reset" and this will reset the game every time you start the bot. You can change it to "Home" to avoid restarting the game, but you need to stay in the "home screen" when you start it.
Another issue is the findPic() function of anjian application. The findPic() function is used for matching images on the display of your mobile. We use this function to determine the state. It may not work properly since the display of each mobile are slightly different. Therefore, you need to re-capture these images yourself. Al least for now, it seems to be an extreme difficult job. Well, good luck.
