FROM node:16-bullseye

ENV LANG C.UTF-8

RUN npm install -g npm@8.3.0 && \
    npm install -g nodemon && \
    npm install -g http-server && \
    npm install -g sass

ENV ENTRYKIT_VERSION 0.4.0
RUN wget https://github.com/progrium/entrykit/releases/download/v${ENTRYKIT_VERSION}/entrykit_${ENTRYKIT_VERSION}_Linux_x86_64.tgz \
    && tar -xvzf entrykit_${ENTRYKIT_VERSION}_Linux_x86_64.tgz \
    && rm entrykit_${ENTRYKIT_VERSION}_Linux_x86_64.tgz \
    && mv entrykit /bin/entrykit \
    && chmod +x /bin/entrykit \
    && entrykit --symlink

RUN mkdir /app

WORKDIR /app

ENTRYPOINT [ \
  "prehook", "node -v", "--"]
