FROM golang:1.22.10-alpine3.21 AS builder

WORKDIR /app

COPY go.* .

COPY main.go .

RUN go build -o ola_mundo_rsan main.go

FROM scratch

COPY --from=builder /app/ola_mundo_rsan /app

CMD [ "/app" ]
