FROM golang AS builder

WORKDIR /src

COPY main.go /src/
RUN go build main.go

FROM scratch
WORKDIR /src
COPY --from=builder /src/main .
ENTRYPOINT [ "./main" ]
