FROM rust:1.79-alpine

WORKDIR /usr/src/app
COPY . .

RUN cargo install --path .

CMD ["project-rust"]