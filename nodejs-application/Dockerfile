from centos:centos7.6.1810

RUN curl -sL https://rpm.nodesource.com/setup_10.x | bash - && \
  yum install -y nodejs && \
  adduser -r nodejs && \
  rm -rvf /var/lib/rpm /var/cache/* && \
  npm init -y && \
  npm install express --save 

USER nodejs

COPY . .

EXPOSE 3000

CMD node app.js
