FROM golang:1.16.6 as go-build
WORKDIR /app
COPY main.go ./
RUN go build main.go

FROM scratch
WORKDIR /app
COPY --from=go-build /app/ .
CMD ["./main"]