FROM quay.io/centos-bootc/centos-bootc:stream9
COPY repos.repo /etc/yum.repos.d/repos.repo
RUN dnf remove -y subscription-manager && dnf install -y epel-release
RUN dnf update -y
RUN dnf install --enablerepo=crb -y htop \
procps-ng \
sysstat \
tcpdump \
conntrack-tools \
bcc-tools \
systemd-resolved \
screen \
tmux \
teamd \
nano \
vim-enhanced \
libsemanage \
python3-dnf-plugin-versionlock \
python3-setools \
python3-dns \
salt-minion \
policycoreutils-python-utils firewalld && dnf clean all && systemctl enable salt-minion
