FROM node:16

# Set the working directory
WORKDIR /app

# Update and install dependencies
RUN apt-get update && \
    apt-get install -y \
    build-essential \
    libpango1.0-dev \
    libcairo2-dev \
    librsvg2-dev \
    libjpeg-dev \
    libgif-dev \
    git

# Clone the Discord MusicBot repository
RUN git clone https://github.com/ManfredRichthofen/Discord-MusicBot.git /download

# Install any dependencies
RUN cp -a /download/djs-bot/. /app/
RUN ls
RUN ls /
RUN ls /app
RUN npm install
RUN npm run update
RUN npm run deploy

# Set environment variables
ENV TOKEN=your_discord_bot_token

# Expose the port the app runs on
EXPOSE 8080

# Run the application
CMD ["npm", "run", "start"]
