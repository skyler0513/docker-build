FROM node:latest
ENV  TIME_ZONE Asia/Shanghai
RUN npm install -g hexo-cli \
    && npm cache clear --force \
    && mkdir /blog \
    && chown root:root /blog
RUN git config --global user.email "suyang0513@126.com"
RUN git config --global user.name "sysummer"
USER root

WORKDIR /blog

EXPOSE 4000
ENTRYPOINT [ "hexo" ]
CMD [ "help" ]
