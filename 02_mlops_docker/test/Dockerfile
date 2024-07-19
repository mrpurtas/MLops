FROM rockylinux:8.6

RUN yum -y update && yum clean all

RUN yum -y install openssh-server python3 sudo passwd

RUN adduser -m test_user && \
    echo "Ankara06" | passwd test_user --stdin && \
    usermod -aG wheel test_user && \
    mkdir /home/test_user/.ssh && \
    chown test_user:test_user -R /home/test_user/.ssh && \
    chmod 700 /home/test_user/.ssh

RUN echo "%wheel ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers

RUN echo "PasswordAuthentication yes" >> /etc/ssh/sshd_config

RUN systemctl enable sshd.service

VOLUME ["/sys/fs/cgroup"]

CMD ["/usr/sbin/sshd", "-D"]