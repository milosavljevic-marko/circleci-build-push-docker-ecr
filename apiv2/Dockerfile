# Docker image for FollowUP API
# ==============================================
#FROM 436598850111.dkr.ecr.us-east-1.amazonaws.com/h10-alpine-node:10.15
FROM node:10-alpine
# prebuild modules
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci --production

# Bundle app source
COPY . .

# Start server
EXPOSE 3000
CMD [ "node", "./bin/followup.start.js" ]
