FROM rust:latest as build

WORKDIR /app
COPY . .
RUN cargo build --release

FROM rust:latest
COPY --from=build /app/target/release/privnote_server .
EXPOSE 4000
CMD ["./privnote_server"]
