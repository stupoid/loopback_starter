FROM node:8.4.0-alpine

# Yarn please
RUN curl -o- -L https://yarnpkg.com/install.sh | bash

ENV PATH="/root/.yarn/bin:${PATH}"

# Installs these globally WITHIN the container, not our local machine
RUN yarn && yarn global add loopback-cli && yarn global add nodemon

# Any commands start from this directory IN the container
WORKDIR /usr/src/api
