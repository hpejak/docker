FROM jupyter/scipy-notebook

#USER $NB_UID

RUN conda install -c plotly --quiet --yes \
    'plotly_express' && \
    jupyter labextension install jupyterlab-plotly --no-build && \
    jupyter labextension install @jupyter-widgets/jupyterlab-manager && \
    jupyter labextension install plotlywidget

RUN conda install --quiet --yes \
    'clickhouse-driver=0.1.*' \
    'clickhouse-cityhash=1.0.2.*' \
    #'aioch=0.0.*' \
    'jinja2=2.11.*' \
    'jinjasql=0.1.*' \
    'kafka-python=2.0.*' \
    'lxml=4.6.*' \
    'lz4=3.1.*' \
    'natsort=7.0.*' \
    'jupyterlab-git' \
    'psycopg2' \
    #'jupyter-lsp' \
    #'python-language-server' \
    'jupyter-lsp-python' \
    'xeus-python=0.8.6' \
    'notebook=6' \
    'jupyterlab=2' \
    'ptvsd' \
    'nodejs' \
    && \
    conda clean --all -f -y && \
    jupyter labextension install @jupyterlab/toc --no-build && \
    jupyter labextension install @aquirdturtle/collapsible_headings --no-build && \
    jupyter labextension install jupyterlab-execute-time --no-build && \
    #jupyter labextension install @jupyterlab/git --no-build && \
    jupyter labextension install @krassowski/jupyterlab_go_to_definition --no-build && \
    jupyter labextension install @krassowski/jupyterlab-lsp --no-build && \
    jupyter serverextension enable --py jupyter_lsp && \
    jupyter labextension install jupyterlab-execute-time --no-build && \
    jupyter labextension install nbdime-jupyterlab --no-build && \
    jupyter labextension install @jupyterlab/debugger --no-build && \
    jupyter lab build -y && \
    jupyter lab clean -y && \
    npm cache clean --force && \
    rm -rf "/home/${NB_USER}/.cache/yarn" && \
    rm -rf "/home/${NB_USER}/.node-gyp" && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"


USER root
COPY ./customspace ./customspace
WORKDIR ./customspace
RUN python setup.py install
RUN pip install aioch && fix-permissions "/home/${NB_USER}"
RUN pip install pyppeteer
WORKDIR  "/home/${NB_USER}"
RUN rm -rf customspace

USER $NB_UID
COPY bg_gradient.ipynb /home/${NB_USER}/
RUN fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"


WORKDIR  "/home/${NB_USER}"
