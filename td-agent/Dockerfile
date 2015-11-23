FROM centos:centos7

MAINTAINER lulichn

# add td-agent repository and gpg key
RUN curl -L https://toolbelt.treasuredata.com/sh/install-redhat-td-agent2.sh | sh sudo

# install fluent biquery plugin
RUN /usr/sbin/td-agent-gem install fluent-plugin-bigquery  --no-ri --no-rdoc -V
RUN /usr/sbin/td-agent-gem install fluent-plugin-google-cloud --no-ri --no-rdoc -V
RUN /usr/sbin/td-agent-gem install fluent-plugin-s3 --no-ri --no-rdoc -V

VOLUME ["/etc/td-agent"]

ENTRYPOINT ["td-agent"]

