# kodland_bot
import discord
import random
from discord.ext import commands

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='$', intents=intents)

@bot.event
async def on_ready():
    print("Bot avviato")

@bot.command()
async def rifiuti_domestici_come_ridurli(ctx):
    await ctx.send("alcuni consigli potrebbero essere: -acquistare articoli di seconda mano quando possibile, -preferire prodotti di alta qualità che durano nel tempo rispetto a quelli monouso, -coinvolgersi in progetti artigianali che trasformano materiali riciclabili in oggetti utili, -optare per prodotti riutilizzabili, come borracce, sacchetti di stoffa, piatti e posate riutilizzabili, -utilizzare contenitori riutilizzabili per conservare il cibo anziché pellicola trasparente o contenitori monouso.")

token = "MTE4NzA4ODg2MDk1ODY5OTU3MA.GoFF3g.Eg4kC0BzCFhKK_Lvt7mv58ZdxVCQl3xdAOSOoU"

bot.run(token)
