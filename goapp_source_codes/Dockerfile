FROM public.ecr.aws/docker/library/golang:1.21.0-alpine3.18e
WORKDIR /app
COPY go.mod .
COPY go.sum .
RUN go mod download
COPY *.go ./
RUN go build -o /docker-go-app
EXPOSE 5003
CMD [ "/docker-go-app" ]
