FROM infrapi.infra.bove.online:5000/centos-base
COPY repos.repo /etc/yum.repos.d/repos.repo
RUN dnf install --enablerepo=crb,highavailability -y \
libguestfs \
libguestfs-tools \
libvirt \
python3-libvirt \
corosync \
pacemaker \
pcs \
&& dnf clean all
