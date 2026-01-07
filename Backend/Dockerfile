# ---------- Build Stage ----------
FROM rust:1.92

WORKDIR /app

RUN apt-get update && apt-get install -y \
    libpq-dev \
    pkg-config

COPY . .
RUN cargo build --release

# ---------- Runtime Stage ----------
FROM ubuntu:22.04

RUN apt-get update && apt-get install -y \
    libpq5 \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY --from=0 /app/target/release/login-app-backend /app/backend

CMD ["./backend"]
