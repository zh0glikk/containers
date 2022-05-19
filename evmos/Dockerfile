FROM ghcr.io/faddat/cosmos

COPY . .

ENV GOPATH=/GO
RUN pacman -Syyu --noconfirm unzip
RUN git clone https://github.com/notional-labs/evmos --branch dangerously-fast
RUN wget -q -O /evmos/genesis.json https://github.com/tharsis/mainnet/raw/main/evmos_9001-2/genesis.json.zip && \
      unzip genesis.json.zip

CMD /bin/bash start.bash

