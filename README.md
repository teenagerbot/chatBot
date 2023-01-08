# chatBot
With it, you can easily create chat bots for your website

# beta function while there is a problem with styles :smirk:
# How to use?
You must first include my library like this:

:point_right: Connecting:

```html
<script src="https://googleapis.volodya-bot-developer.repl.co/libs/chatbot.min.js"></script>
```

:point_right: Usage:

```js
let mybot = new ChatBot();
//bot doctrine: a question is a question that the user can enter to which he will receive the answer "answer"
mybot.newMemory("answer|question #1|question #2...|question #999999999999999", "answer|question #1|question #2...|question #999999999999", ....);
//creating the bot
mybot.newBot(true, "chat1", "support bot", "GI", "type a problem...", "", "ru");
//starting the bot
mybot.startBot("chat1");
//stopping the bot: id=chat1
mybot.stopBot("chat1");
//deleting the messages
mybot.deleteChat("chat1");
//bot restart
mybot.restartBot("chat1", false);
```

:point_right: Result:
![GitHub Dark](https://googleapis.volodya-bot-developer.repl.co/bot.jpg#gh-light-mode-only)
# Explanation:
This bot has 6 methods:
1) mybot.newMemory(...) here we train the bot to answer a set of some possible questions with one answer
2) mybot.newBor(time, id, text, button, placeholder, image, language)

   a) time: has 2 values: true/false, that is, whether or not to display the time of sending messages in the conversation

   b) id: your bot id, as you can create multiple bots

   c) text: text-title of your bot, in my case it is "support bot"

   d) button: has 3 meanings: GI(use the google icon on the button to send the message)/TI(telegram image is used (airplane))/Or the 3 value is just your text for the button, for example: "submit"

   e) placeholder: replacement text in the field for entering a message

   f) image: your picture for the background of the chat, if you do not specify anything, my picture will be used ;)

   g) language: the language of the bot in which he will say hello to you, languages: ua, ru, de(Deutsch), en, es(Spanish), fr(French), it(Italian), ja(Japanese), pl(Polish), sr(Serbian), zh(Chinese)

3) mybot.startBot(ID) starts the bot by id = ID
4) mybot.deleteBot(id) deleting a bot by its ID
5) mybot.stopBot(id) stops the bot by its ID, that is, the field for entering a message becomes unavailable
6) mybot.deleteChat(id) delete all messages in bot with id
7) mybot.restartBot(ID, rem) restarts the bot by its ID, rem=true/false - clear chat on restart(true) or not(false)
8) mybot.clearMemory() clears the "memory" of the bot, useful for improving website speed


# WARNING: you are allowed to host 1 bot for now
