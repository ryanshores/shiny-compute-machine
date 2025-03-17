# Use the official Home Assistant image as the base image
FROM ghcr.io/home-assistant/home-assistant:stable

# Set environment variables
ENV TZ=UTC

# Expose the Home Assistant port
EXPOSE 8123

# Set the working directory
WORKDIR /config

# Copy custom configuration files (if any) to the container
COPY config/lovelace_dashboards /config/.storage/lovelace_dashboards
COPY config/lovelace.dashboard_portainer /config/.storage/lovelace.dashboard_portainer

# Start Home Assistant
CMD [ "python", "-m", "homeassistant", "--config", "/config" ]