FROM archlinux

RUN yes | pacman --sync --refresh \
    ansible \
    docker \
    ipmitool \
    make \
    python-pip

RUN pip install docker
