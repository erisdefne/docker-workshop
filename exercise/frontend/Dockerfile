
FROM node:20.11.1-bullseye-slim

WORKDIR /frontend

ENV REACT_APP_BACKEND_URL='http://localhost:8000'

COPY package.json package-lock.json tailwind.config.js /frontend/
COPY src /frontend/src
COPY public /frontend/public

RUN ["npm", "install"]
RUN ["npm", "run", "build"]

RUN ["npm", "install", "-g", "serve"]

EXPOSE 3000

# CMD ["npm", "start"]
CMD ["serve", "-s", "build", "-l", "3000"]