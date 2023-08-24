import discord
from discord.ext import commands
import random, os
from sampah import organic, non_organic

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='!', intents=intents)

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')

@bot.command()
async def organic(ctx):
    await ctx.send(organic())

@bot.command()
async def non_organic(ctx):
    await ctx.send(non_organic())

bot.run(")
