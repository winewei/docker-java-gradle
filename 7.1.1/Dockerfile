FROM inutano/wget:latest AS downloader

RUN wget -q https://w-tools.oss-cn-hongkong.aliyuncs.com/gradle-7.1.1.tar.gz --no-check-certificate
RUN tar xf gradle-7.1.1.tar.gz


FROM pristtlt/java:1.8

COPY --from=downloader /gradle-7.1.1 /usr/local/gradle-7.1.1

ENV PATH=$PATH:/usr/local/gradle-7.1.1/bin
