FROM ghcr.io/notional-labs/cosmos

COPY . .

ENV GOPATH=/GO
RUN pacman -Syyu --noconfirm unzip
RUN git clone https://github.com/notional-labs/evmos --branch dangerously-fast


RUN wget -q -O /evmos/genesis.json.zip https://github.com/tharsis/mainnet/raw/main/evmos_9001-2/genesis.json.zip && \
       cd /evmos && \
       unzip genesis.json.zip
RUN ls
RUN rm -rf genesis.json.zip


CMD /bin/bash start.bash

