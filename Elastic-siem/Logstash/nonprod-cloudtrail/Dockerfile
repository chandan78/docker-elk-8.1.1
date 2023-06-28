FROM logstash:7.16.1

USER root

RUN yum -y install wget && wget https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm

RUN yum -y install epel-release-latest-7.noarch.rpm
RUN echo 'assumeyes=1' >> /etc/yum.conf
RUN yum update && yum install haveged && chkconfig haveged on

# RUN bin/logstash-plugin install logstash-input-cloudwatch
RUN bin/logstash-plugin install --preserve logstash-input-cloudwatch_logs