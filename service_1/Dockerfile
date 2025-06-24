# Use Go base image
FROM golang:1.22-alpine AS builder

WORKDIR /app

# Copy Go file
COPY main.go .

# Build the Go app (no modules)
RUN GO111MODULE=off CGO_ENABLED=0 go build -o service1 main.go

# Final image
FROM alpine:latest

WORKDIR /root/
COPY --from=builder /app/service1 .

EXPOSE 8001

CMD ["./service1"]
