
### Build stage

FROM golang as build

WORKDIR /go/src
ADD main.go .

RUN CGO_ENABLED=0 go build -o hello .


### Run stage

FROM scratch

COPY --from=build /go/src/hello .

CMD ["./hello"]
