FROM node:20

# Set the working directory to /app
WORKDIR /Discord-MusicBot/djs-bot

# Clone the Discord MusicBot repository
RUN apt-get update && apt-get install -y git \
    && git clone https://github.com/wtfnotavailable/Discord-MusicBot.git .

# Install any dependencies
RUN npm i -g

# Set environment variables
ENV TOKEN=your_discord_bot_token

# Expose the port the app runs on
EXPOSE 8080

# Run the application
CMD ["node", "bot.js"]