# pyanon
## Api for new anonym client

### Echo bot
```python3
import pyanon
import asyncio

client = pyanon.AnonClient()

async def main():
    await client.auth("your login", "your password")
    print("Successfully logged in")

@client.onChatMessage
async def messageListener(event: pyanon.Notification):
    await client.sendMessage(event.payload.roomId, f"Your message text is '{event.payload.message.text}'")

asyncio.get_event_loop().run_until_complete(main())
```

### Installation: pip install pyanon
