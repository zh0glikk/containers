FROM ghcr.io/faddat/cosmos

COPY . .

ENV GOPATH=/GO
RUN git clone https://github.com/notional-labs/evmos --branch v3.0.0-fast-badger-danger

EXPOSE 1317 26656 26657 9090 8545 

CMD /bin/bash start.bash

