FROM golang:1.14.2-alpine3.11 AS builder

COPY ./main.go /home

WORKDIR /home

RUN go build -o main.sh

FROM scratch

COPY --from=builder /home/main.sh /home/main.sh

CMD ["./home/main.sh"]
