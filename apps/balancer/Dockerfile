FROM gcc:13-bookworm AS builder

WORKDIR /project

COPY include/ include/
COPY lib/ lib/
COPY apps/balancer/ apps/balancer/

RUN make -C lib
RUN make -C apps/balancer

FROM debian:bookworm-slim

WORKDIR /app

COPY --from=builder /project/apps/balancer/balancer ./balancer

EXPOSE 8080

CMD ["./balancer"]
