# HelloWorld

References: 
- https://www.youtube.com/watch?v=NwBWW8cNCP4
- https://dev.to/poojaghodmode/telebot-using-python-3akh


Code:
```python
# Remember to add telegram bot API key generated to ".env" in the same directory.

import telebot
import os
from dotenv import load_dotenv

load_dotenv()
API_KEY = os.getenv('AUTH_TOKEN')
bot = telebot.TeleBot(API_KEY)

@bot.message_handler(commands=['Greet'])
def greet(message):
    bot.reply_to(message, "Hey, how's it going?")

@bot.message_handler(commands=['Wave'])
def greet(message):
    bot.send_message(message.chat.id, "👋")

# keep checking for user input
bot.polling()
```

## Requirements
- Telegram Account (with Mobile Phone or VM)
- Scripting Environment
   - Python >= 3.6
   - Libraries (for now)
   ```
   pip install pyTelegramBotAPI==3.7.9
   pip install python-dotenv==0.17.1
   pip install requests==2.25.1
   ```
   
## Results
![image](https://user-images.githubusercontent.com/48358569/204119239-13cd3deb-15d1-4f4b-a41b-81daf4c581f1.png)

