FROM quay.io/informaticslab/r

#Clojure    
RUN update-ca-certificates -f
RUN curl -k https://raw.githubusercontent.com/technomancy/leiningen/stable/bin/lein > /usr/local/bin/lein
RUN chmod +x /usr/local/bin/lein
RUN apt-get install -y default-jre
RUN git clone https://github.com/roryk/clojupyter
RUN mkdir -p /etc/pki/tls/certs && ln -s /etc/ssl/certs/ca-certificates.crt /etc/pki/tls/certs/ca-bundle.crt
RUN apt-get -y install make cmake
RUN cd clojupyter && make && make install && cd .. && rm -rf clojupyter