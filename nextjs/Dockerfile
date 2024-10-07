FROM mcr.microsoft.com/vscode/devcontainers/base:0-ubuntu-20.04

ENV TZ=America/Sao_Paulo
ENV DEBIAN_FRONTEND=noninteractive.
ENV NODE_MAJOR=20

RUN sudo apt-get update -y && sudo apt-get upgrade -y

# INSTALLING AWS CLI
RUN apt-get install -y tzdata curl unzip groff less keyboard-configuration && \
    curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && ./aws/install

# INSTALLING NODE, PNPM, ESLINT 
RUN sudo apt-get install -y ca-certificates curl gnupg && \
    sudo mkdir -p /etc/apt/keyrings && \
    curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg && \
    echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_$NODE_MAJOR.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list && \
    sudo apt-get update -y && \
    sudo apt-get install -y nodejs && \
    npm install -g eslint
