# Gnoland development and execution environment
# It is unified, so they don't diverge
# the idea is that it is better to ensure that the build env and runtime env are consistent between ci and development
# this feeds gitpod

FROM ghcr.io/notional-labs/archlinux

ENV GOPATH=/go

# everything needed for gno development
RUN pacman -Syyu --noconfirm go base-devel git leveldb rocksdb make snappy lz4 git-lfs jq wget curl protobuf

# Useful tools:
# gofumpt for formatting
# gopls to ensure all editor features work well when coding with this image
RUN go install mvdan.cc/gofumpt@latest && \
      go install github.com/golangci/golangci-lint/cmd/golangci-lint@latest && \
      go install golang.org/x/tools/gopls@latest && \
      cp /go/bin/* /usr/bin && \
      mkdir /go && \
      chmod -R 777 /go

