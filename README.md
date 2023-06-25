
### Authentication
Go to https://bard.google.com/

- F12 for console
- Copy the values
  - Session: Go to Application → Cookies → `__Secure-1PSID`. Copy the value of that cookie.
### Usage
Create a file named `docker-compose.yml`
```bash
services:
  chatgpt:
    image: sheepgreen/bard
    container_name: bard
    environment:
      - BARD_TOKEN="value got above"
      - TELEGRAM_BOT_TOKEN="your telegram bot token"
    restart: always
```
Then run `docker-compose up -d`,that's all!
