FROM centos:centos7

MAINTAINER lulichn

# add td-agent repository and gpg key
ADD td-agent.repo /etc/yum.repos.d/td-agent.repo
ADD RPM-GPG-KEY-td-agent /etc/pki/rpm-gpg/RPM-GPG-KEY-td-agent

# install td-agent
RUN yum -y install td-agent && yum clean all

# install fluent biquery plugin
RUN /usr/sbin/td-agent-gem install fluent-plugin-bigquery  --no-ri --no-rdoc -V
RUN /usr/sbin/td-agent-gem install fluent-plugin-google-cloud --no-ri --no-rdoc -V
RUN /usr/sbin/td-agent-gem install fluent-plugin-s3 --no-ri --no-rdoc -V

VOLUME ["/etc/td-agent"]

ENTRYPOINT ["td-agent"]

