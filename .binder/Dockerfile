FROM rocker/binder:4.0.2
LABEL maintainer='John Franchak'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/JohnFranchak/259-files-import/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2021-02-02/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
