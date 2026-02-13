FROM golang:1.22-alpine AS build

WORKDIR /src

COPY go.mod ./
RUN go mod download

COPY . ./

RUN CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -trimpath -ldflags="-s -w" -o /out/claude-nvidia-proxy ./


FROM alpine:3.20

RUN adduser -D -H -u 10001 app

WORKDIR /app

COPY --from=build /out/claude-nvidia-proxy /app/claude-nvidia-proxy

USER app

EXPOSE 3001

ENV ADDR=":3001"
ENV CONFIG_PATH="/app/config.json"

ENTRYPOINT ["/app/claude-nvidia-proxy"]
