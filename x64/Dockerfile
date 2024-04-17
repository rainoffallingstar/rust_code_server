FROM codercom/code-server:latest
RUN curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh -s -- -y &&\
    sudo apt update &&\
    sudo apt install -y python3 python3-pip r-base libcurl4-openssl-dev &&\
    sudo apt autoclean &&\
    sudo apt clean &&\
    sudo rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* &&\
    sudo R -e "install.packages('pak')" &&\
    sudo R -e "pak::pak('rainoffallingstar/cargor')" &&\
    sudo R -e "pak::pak('rstudio/reticulate')" &&\
    ~/.cargo/bin/cargo install --git https://github.com/typst/typst --locked typst-cli
