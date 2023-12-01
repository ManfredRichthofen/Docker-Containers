FROM node:20

# Set the working directory to /app
WORKDIR /djs-bot

RUN apt-get update -y && \
    apt-get install -y \
      build-essential \
      libpango1.0-dev \
      libcairo2-dev \
      librsvg2-dev \
      libjpeg-dev \
      libgif-dev

# Clone the Discord MusicBot repository
RUN apt-get update && apt-get install -y git \
    && git clone https://github.com/wtfnotavailable/Discord-MusicBot.git .

# Install any dependencies
RUN ls
RUN npm install
RUN npm run update
RUN npm run deploy
# Set environment variables
ENV TOKEN=your_discord_bot_token

# Expose the port the app runs on
EXPOSE 8080

# Run the application
CMD ["npm", "run", "start"]