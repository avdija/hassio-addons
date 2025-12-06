FROM archlinux:latest
RUN pacman -Syu --noconfirm --needed gcc make git ripgrep fd unzip neovim openssh stow ripgrep
RUN sed -i 's|^root:[^:]*:[^:]*:[^:]*:[^:]*:[^:]*:[^:]*|root:x:0:0::/data/root:/usr/bin/bash|' /etc/passwd
RUN /usr/bin/ssh-keygen -A
CMD ["/usr/sbin/sshd", "-D"]
