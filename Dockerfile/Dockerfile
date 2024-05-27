# Use uma imagem base com suporte a Terraform
FROM hashicorp/terraform:latest

# Instalar tfsec
RUN apt-get update && \
    apt-get install -y wget unzip && \
    wget https://github.com/aquasecurity/tfsec/releases/download/v1.5.3/tfsec-linux-amd64 && \
    chmod +x tfsec-linux-amd64 && \
    mv tfsec-linux-amd64 /usr/local/bin/tfsec

# Definir diretório de trabalho
WORKDIR /workspace

# Definir ponto de entrada padrão
ENTRYPOINT ["/bin/bash"]