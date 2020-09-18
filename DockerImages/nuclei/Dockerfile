FROM golang
RUN git clone https://github.com/projectdiscovery/nuclei.git; cd nuclei/cmd/nuclei/; go build; mv nuclei /usr/local/bin/; nuclei -h
RUN cd /go; git clone https://github.com/projectdiscovery/nuclei-templates


