FROM golang
RUN go get -u github.com/tomnomnom/unfurl
RUN git clone https://github.com/tomnomnom/hacks; cd hacks/kxss; go build; mv kxss /usr/local/bin/


