FROM ubuntu:latest

RUN apt-get update && apt-get -y install --no-install-recommends zsh curl git ca-certificates ca-certificates ssh-client

RUN useradd -ms /bin/zsh vscode && mkdir -p /home/vscode
RUN chsh -s /bin/zsh vscode
USER vscode
WORKDIR /home/vscode

RUN sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
RUN git clone https://github.com/MikeAleksa/dotfiles.git
RUN cp /home/vscode/dotfiles/zshrc /home/vscode/.zshrc && touch ~/.z
RUN mkdir ~/.zsh && curl -L git.io/antigen > ~/.zsh/antigen.zsh
