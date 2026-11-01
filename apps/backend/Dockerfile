FROM gcc:13-bookworm AS builder

WORKDIR /project

COPY include/ include/
COPY lib/ lib/
COPY apps/backend/ apps/backend/

RUN make -C lib
RUN make -C apps/backend

FROM debian:bookworm-slim

WORKDIR /app

COPY --from=builder /project/apps/backend/backend ./backend

EXPOSE 9000

CMD ["./backend"]
