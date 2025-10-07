FROM mcr.microsoft.com/devcontainers/go:dev-1.25-bookworm

LABEL maintainer="Avocatl Software"

RUN apt-get update && apt-get install -y exa bat curl && apt-get clean

RUN git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting \
    && git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

RUN go install github.com/go-task/task/v3/cmd/task@latest
RUN go install github.com/princjef/gomarkdoc/cmd/gomarkdoc@latest
RUN go install github.com/goreleaser/goreleaser/v2@latest
RUN go install github.com/pressly/goose/v3/cmd/goose@latest
RUN go install github.com/sqlc-dev/sqlc/cmd/sqlc@latest
