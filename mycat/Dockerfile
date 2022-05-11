FROM java:8-buster

ADD http://dl.mycat.org.cn/2.0/1.21-release/mycat2-1.21-release-jar-with-dependencies.jar /usr/local
ADD http://dl.mycat.org.cn/2.0/install-template/mycat2-install-template-1.21.zip /usr/local

RUN cd /usr/local && unzip mycat2-install-template-1.21.zip && rm mycat2-install-template-1.21.zip && ls -lna \
      && mv mycat2-1.21-release-jar-with-dependencies.jar mycat/lib/mycat2-1.21-release-jar-with-dependencies.jar \
      && chmod +x /usr/local/mycat/bin/mycat \
      && chmod +x /usr/local/mycat/bin/wrapper-linux-x86-64

# VOLUME /usr/local/mycat/conf
# VOLUME /usr/local/mycat/logs

EXPOSE 8066 9066

# 前台运行
CMD ["/usr/local/mycat/bin/mycat", "console"]