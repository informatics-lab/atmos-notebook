FROM base_python

# Python 2
RUN conda create -y -n py2 python=2 ipykernel
RUN bash -c "source activate py2 && \
             conda install -y -c scitools iris cartopy"
RUN bash -c "source activate py2 && jupyter kernelspec install-self"