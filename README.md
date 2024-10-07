# AutomatePhoneController

An [Automate](https://llamalab.com/automate/) flow. Use Telegram bot to send sms, make phone calls, etc.

No root needed.

## Feature

Use Telegram bot to:
- Send sms
- Make phone calls
- Answer/end calls
- Get phone location
- Reduce spam by automacally answer and hang up calls

## Install

Buy and install [Automate](https://llamalab.com/automate/) to your phone

Install https://llamalab.com/automate/community/flows/46295 in Automate

Click on "Edit" (right buttom floating button), **Edit Telegram bot token and whitelist**

> If you don't know your Telegram user id for whitelist, check [UserID Bot](https://t.me/chatIDrobot)

Go to Automate settings, check "Run on system startup", also set SMS/call rate limit if you need.

Use it with https://github.com/pppscn/SmsForwarder to also get notified on incoming SMSs and calls. You can use the same userid and bot token on both softwares :3

Setup command list with:

```bash
curl https://api.telegram.org/botYOURTOKEN -H 'Content-type: application/json' -d '{"commands": [{"command":"call","description":"/call [subid] [toNumber]"},{"command":"sms","description":"/sms [subid] [toNumber] [text]"},{"command":"accept","description":"Accept the call."},{"command":"decline","description":"Decline the call."}, {"command": "autoanswer", "description": "/autoanswer [0|1] Set automatically answer the call and hang up after 2 secs."}, {"command": "getLocation", "description": "Get device location."}]}'
```

## Screenshots

![image](https://github.com/leohearts/AutomatePhoneController/assets/24632029/fa431aa7-da22-43cf-a325-a7ea1af873d6)


![Control phone with Telegram](https://github.com/leohearts/AutomatePhoneController/assets/24632029/74bd4233-92de-4d67-a3f7-3bd3f3cc1e21)
