FROM golang:1.16

ENV APP_HOME /go/src 
WORKDIR $APP_HOME
ENV PATH="/go/bin:${PATH}"
ENV GO111MODULE=on
ENV GOFLAGS=-mod=vendor
ADD ./ $APP_HOME
RUN GOOS=linux go build $APP_HOME/main.go
EXPOSE 8000
CMD ["./main"]