from telethon.sync import TelegramClient
from telethon.tl.functions.account import UpdateStatusRequest
import asyncio
import os

api_id = int(os.environ['API_ID'])
api_hash = os.environ['API_HASH']
session_name = 'session'

client = TelegramClient(session_name, api_id, api_hash)

async def stay_online():
    await client.start()
    print("Bot doimiy onlayn holatda ishlamoqda...")
    while True:
        await client(UpdateStatusRequest(offline=False))
        await asyncio.sleep(60)

with client:
    client.loop.run_until_complete(stay_online())
