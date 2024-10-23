FROM mcr.microsoft.com/devcontainers/typescript-node

ENV TZ=America/Sao_Paulo
ENV DEBIAN_FRONTEND=noninteractive.

RUN sudo apt-get update

# INSTALLING AWS CLI
# RUN apt-get install -y tzdata curl unzip groff less keyboard-configuration && \
#     curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && \
#     unzip awscliv2.zip && ./aws/install

# INSTALLING DEPENDENCIES
RUN sudo apt-get update -y && \
    npm install -g pnpm @nestjs/cli eslint