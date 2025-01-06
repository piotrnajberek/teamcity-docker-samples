# Użyj oficjalnego obrazu TeamCity Agent jako bazowego
FROM docker.io/jetbrains/teamcity-minimal-agent:2024.12-linux

# Zaloguj się jako root, aby mieć odpowiednie uprawnienia
USER root

# Zainstaluj Ansible i inne zależności
RUN apt-get update && \
    apt-get install -y --no-install-recommends software-properties-common && \
    apt-get install -y gnupg \
    apt-add-repository --yes --update ppa:ansible/ansible && \
    apt-get install -y ansible && \
    apt-get clean && rm -rf /var/lib/apt/lists/*
