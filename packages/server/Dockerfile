FROM node:12-buster

# Server-specific
ENV PORT=3000
ENV POSTGRES_URL="postgres://postgres:pass@postgres:5432/pg"
ENV REDIS_URL="redis://redis:6379"
ENV CANONICAL_URL="http://localhost:3000"
ENV STRATEGY_LOCAL=true
ENV SESSION_SECRET="verysecret"
ENV FRONTEND_PORT=8080
ENV FRONTEND_HOST='frontend'

# Docker-specific
ENV WORKDIR=/exec

WORKDIR ${WORKDIR}

COPY package.json ${WORKDIR}
COPY package-lock.json ${WORKDIR}

RUN npm install

ADD . ${WORKDIR}

CMD ["npm", "run", "dev"]
