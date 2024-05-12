FROM infrapi.infra.bove.online:5000/centos-base
ENV K8S_VERSION=1.30.0
COPY repos.repo /etc/yum.repos.d/repos.repo
RUN dnf install --enablerepo=crb -y \
kubectl-$K8S_VERSION \
kubeadm-$K8S_VERSION \
kubelet-$K8S_VERSION \
cri-o-$K8S_VERSION \
&& dnf clean all && systemctl enable salt-minion
