FROM ghcr.io/notional-labs/cosmos

ADD https://github.com/cosmos/mainnet/raw/master/genesis.cosmoshub-4.json.gz /genesis.cosmoshub-4.json.gz 

RUN gzip -d genesis.cosmoshub-4.json.gz && \
    mv genesis.cosmoshub-4.json genesis.json && \
    wget -O /addrbook.json https://quicksync.io/addrbook.cosmos.json
