FROM codercom/code-server:latest
RUN curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh -s -- -y &&\
    sudo apt update &&\
    sudo apt install -y python3 python3-pip r-base &&\
    sudo apt autoclean &&\
    sudo apt clean &&\
    sudo rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* &&\
    sudo chmod -R u+w /usr/local/lib/R/site-library &&\
    R -e "install.packages('pak')" &&\
    R -e "pak::pak('rainoffallingstar/cargor')" &&\
    R -e "pak::pak('rstudio/reticulate')" &&\
    pip3 install --upgrade pip 
