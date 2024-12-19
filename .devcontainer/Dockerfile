FROM mcr.microsoft.com/devcontainers/universal:2-linux

# Update package lists and install system dependencies
RUN apt-get update && apt-get install -y \
    python3-pip \
    python3-venv \
    curl

# Install Flask
COPY .devcontainer/requirements.txt /workspace/requirements.txt
RUN pip install --no-cache-dir -r /workspace/requirements.txt

# Install Node.js and Vue CLI
RUN curl -fsSL https://deb.nodesource.com/setup_16.x | bash -
RUN apt-get install -y nodejs
RUN npm install -g @vue/cli
