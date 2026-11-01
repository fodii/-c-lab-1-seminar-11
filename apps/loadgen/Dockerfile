FROM gcc:13-bookworm AS builder

WORKDIR /project

COPY include/ include/
COPY lib/ lib/
COPY apps/loadgen/ apps/loadgen/

RUN make -C lib
RUN make -C apps/loadgen

FROM debian:bookworm-slim

WORKDIR /app

COPY --from=builder /project/apps/loadgen/loadgen ./loadgen

CMD ["./loadgen"]
