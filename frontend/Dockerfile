FROM node:20-alpine

EXPOSE 5173

RUN mkdir /lms-admin && chown -R node:node /lms-admin

WORKDIR /lms-admin

COPY --chown=node:node package.json package-lock.json ./

RUN npm install

COPY --chown=node:node . ./

# RUN npm run build

CMD ["npm", "run", "dev"]
