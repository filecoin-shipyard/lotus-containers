FROM golang:1.20-bullseye as paramfetch

ARG LOTUS_VERSION
ARG SECTOR_SIZE

RUN go install github.com/filecoin-project/go-paramfetch/paramfetch@v0.0.4

WORKDIR /go/src/lotus
RUN git clone --depth 1 --branch ${LOTUS_VERSION} https://github.com/filecoin-project/lotus .
ENV FIL_PROOFS_PARAMETER_CACHE=/filecoin-proof-parameters
RUN paramfetch ${SECTOR_SIZE} build/proof-params/parameters.json build/proof-params/srs-inner-product.json

FROM scratch
COPY --from=paramfetch /filecoin-proof-parameter/ /filecoin-proof-parameters/

# This image is meant to be used for copying proofs; not to run. hence the dummy entrypoint.
ENTRYPOINT ["false"]