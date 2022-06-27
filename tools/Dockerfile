FROM archlinux

RUN yes | pacman --sync --refresh \
    ansible \
    docker \
    ipmitool \
    make \
    openssh \
    python-pip

RUN pip install docker
