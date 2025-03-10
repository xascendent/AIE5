FROM ghcr.io/astral-sh/uv:python3.13-bookworm-slim

# Set the home directory and path
ENV HOME=/home/user \
    PATH=/home/user/.local/bin:$PATH     


# Copy the app to the container
COPY --chown=user . $HOME/app


# Install the dependencies
# RUN uv sync --frozen
RUN uv sync


# Start LangGraph Studio
CMD ["uv", "langgraph", "studio"]
