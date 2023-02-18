FROM diamol/golang AS build

COPY main.go .
RUN go build -o /web/server

# app
FROM diamol/base
WORKDIR web

COPY --from=build /web/server .

RUN chmod +x /web/server

CMD ["/web/server"]

ENV USER=sixeyed
EXPOSE 80

COPY index.html .
