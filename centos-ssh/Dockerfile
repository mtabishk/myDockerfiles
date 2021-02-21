FROM centos:latest
RUN yum install -y net-tools openssh-server passwd
RUN ssh-keygen -A
RUN echo redhat | passwd root --stdin
ENTRYPOINT ["/usr/sbin/sshd", "-D"]
