FROM golang:1.22-alpine AS builder

WORKDIR /app
COPY main.go .

RUN GO111MODULE=off CGO_ENABLED=0 go build -o service1 main.go

# ---

FROM alpine:latest

WORKDIR /root/


RUN apk add --no-cache curl

COPY --from=builder /app/service1 .

EXPOSE 8001
CMD ["./service1"]
