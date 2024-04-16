FROM codercom/code-server:latest
RUN curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh -s -- -y &&\
    sudo apt install python3 python3-pip r-base &&\
    sudo apt autoclean &&\
    sudo apt clean &&\
    sudo rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* &&\
    R -e "install.packages('pak')"