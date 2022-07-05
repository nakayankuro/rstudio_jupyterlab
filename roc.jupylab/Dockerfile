From rocker/tidyverse:4.2
RUN apt -o Acquire::Check-Valid-Until=false -o Acquire::Check-Date=false update
RUN apt install -y python3-pip
ENV PATH "$HOME/.local/bin:$PATH"
COPY ./install.R /tmp/install.R
RUN yes n | Rscript /tmp/install.R
RUN pip3 install Jupyter \
    && pip3 install jupyterlab \
    && pip3 install pandas \
    && pip3 install Scipy \
    && pip3 install seaborn \
    && pip3 install matplotlib \
    && pip3 install scikit-learn \
