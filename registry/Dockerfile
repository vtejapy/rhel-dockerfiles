FROM 10.3.13.125:5000/brew/rhel7:latest
MAINTAINER Stephen Tweedie <sct@redhat.com>

RUN yum update -y; yum clean all
RUN yum install -y docker-registry; yum clean all
ADD run-registry.sh /opt/registry/run-registry.sh
RUN chmod -v 755 /opt/registry/run-registry.sh
CMD ["/opt/registry/run-registry.sh"]
EXPOSE 5000

