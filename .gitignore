import telebot
import re

TOKEN="token"
bot = telebot.TeleBot(TOKEN)

@bot.message_handler(commands=['start', 'help'])
def send_welcome(message):
    bot.reply_to(message, "Assalom aleykum, sizga qanday yordam bera olaman?")

@bot.message_handler(func=lambda message: True)
def count_letters(message):
    text = message.text
    letter_count = len(re.findall(r'[A-Za-z]', text))
    bot.reply_to(message, f"Matnda {len(message.text.split())} ta so'z va {letter_count} ta harf mavjud.")

bot.infinity_polling
()
