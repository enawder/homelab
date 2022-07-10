FROM archlinux

RUN yes | pacman --sync --refresh \
    ansible \
    docker \
    ipmitool \
    make \
    openssh \
    packer \
    python-pip \
    vagrant

RUN pip install docker
