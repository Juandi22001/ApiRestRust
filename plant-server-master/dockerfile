# Use the official Rust image.
# https://hub.docker.com/_/rust
FROM rust:1.60.0

# Copy local code to the container image.
WORKDIR /usr/src/app
COPY . .

# Install production dependencies and build a release artifact.
RUN cargo build --release

# Service must listen to $PORT environment variable.
# T his default value facilitates local development.
ENV PORT 8088

# Run the web service on container startup.
CMD ["./target/debug/plant_server.exe"]