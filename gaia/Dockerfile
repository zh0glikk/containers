FROM ghcr.io/notional-labs/cosmos

RUN wget -q https://github.com/cosmos/mainnet/raw/master/genesis.cosmoshub-4.json.gz && \
    gzip -d genesis.cosmoshub-4.json.gz && \
    mv genesis.cosmoshub-4.json genesis.json && \
    wget -O /addrbook.json https://quicksync.io/addrbook.cosmos.json
