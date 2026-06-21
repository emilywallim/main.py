from telegram import Update
from telegram.ext import Application, CommandHandler, ContextTypes

TOKEN = "7907926455:AAErOeMcZk3BtQOE81lGjqz6eIfR-V9Hgds"

async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    await update.message.reply_text("🤖 Bot Running on Railway ✔")

app = Application.builder().token(TOKEN).build()
app.add_handler(CommandHandler("start", start))

print("Bot Running...")
app.run_polling()
