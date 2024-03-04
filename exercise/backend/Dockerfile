
FROM node:20.11.1-bullseye-slim

WORKDIR /backend

COPY package.json package-lock.json /backend/
COPY index.js utils.js /backend/

RUN ["npm", "install"]

ENV PORT=8000

VOLUME [ "/backend/history.log" ]

EXPOSE 8000

CMD ["node", "index.js"]