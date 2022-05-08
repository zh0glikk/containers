FROM ghcr.io/faddat/cosmos

ENV GOPATH=/GO
RUN git clone https://github.com/notional-labs/evmos --branch v3.0.0-fast-badger-danger

CMD /bin/bash /evmos/scripts/statesync-rocks.bash
