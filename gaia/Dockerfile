FROM ghcr.io/faddat/cosmos

RUN wget -q https://github.com/cosmos/mainnet/raw/master/genesis.cosmoshub-4.json.gz && \
    gzip -d genesis.cosmoshub-4.json.gz && \
    rm genesis.cosmoshub-4.json.gz && \
    wget -O addrbook.json https://quicksync.io/addrbook.cosmos.json
