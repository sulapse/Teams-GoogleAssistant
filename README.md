# Teams-GoogleAssistant
Send Teams messages using Google Assistant, Powerautomate and IFTTT.<br>
Thanks to Microsoft and their mediocre API for Teams - Powerautomate must be used.<br><br>
Personally I use this to send a message to my boss if I'm late for work, I feel it's easier to just shout at my Google Assistant while heading for the shower instead of opening up Teams and typing.
<br><br>

Note: This is more of a guide than a project.

## Requirements:
* <a href="https://ifttt.com/">IFTTT account</a>
* Google Assistant
* Microsoft account with Powerautomate access
* Gmail account

## Setup:
1. Go to IFTTT and create a new applet
2. "If this" add Google Assistant V2 (Follow the instructions on IFTTT to link your Google Assistant to IFTTT)
3. Add the "Activate Scene" trigger
4. Give your scene a name (I'll name mine I'm late)
5. "Then That" add Gmail
6. Add action "Send an email"
* To address should be your Microsoft email
* Subject and body can be whatever, but remember the subject you set as this will later be used in Powerautomate.
7. Create action
8. Continue, Finish
9. Head over to PowerAutomate
10. Create a new "Automated cloud flow"
11. Set a flow name
12. Flow trigger should be "When a new email arrives (V3) - Make sure it's part of Office 365 Outlook
13. Show advanced options on the email arrive trigger
14. Set the from adress to your gmail address
15. Set the "Subject filter" to the same as your IFTTT subject
16. Click "+ New Step"
17. Add Microsoft Teams "Post message in a chat or channel"
18. Set "Post As" to "User"
19. Set "Post in" to 'Group Chat' or 'Channel' depending on where you want to send your message
20. Set "Conversation ID" to the chat or group you want to post in
21. Set the message you want to post and hit "Save"
22. Make sure the flow is activated
* You can now shout at your Google Assistant to run the custom event - Within a few seconds your message will appear in Teams
