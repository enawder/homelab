FROM archlinux

RUN yes | pacman --sync --refresh \
    ansible \
    docker \
    ipmitool \
    make \
    openssh \
    python-pip \
    vagrant

RUN pip install docker
