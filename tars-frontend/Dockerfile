FROM node:18-alpine

WORKDIR /app

# Install git with apk
RUN apk add --no-cache git

# Clone the frontend code
RUN git clone https://github.com/consulthunter/tars-frontend.git .

RUN ls -al

# Install dependencies
RUN npm install

# Expose port for Vite dev server
EXPOSE 5173

CMD ["npm", "run", "dev"]