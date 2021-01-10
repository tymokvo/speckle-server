FROM node:12-buster

ENV WORKDIR=/exec
WORKDIR ${WORKDIR}

COPY package.json ${WORKDIR}
COPY package-lock.json ${WORKDIR}

RUN npm install

ADD . ${WORKDIR}

CMD ["npm", "run", "dev"]
