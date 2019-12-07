# ## Dockerfile for a haskell environment
# FROM haskell:8.6.5

# # Configure apt
# ENV DEBIAN_FRONTEND=noninteractive
# RUN apt-get update \
#     && apt-get -y install --no-install-recommends apt-utils 2>&1 \
#     && apt-get install -y git procps curl apt-transport-https lsb-release \
# # Install haskell ide engine dependencies
#     && apt-get -y install libicu-dev libtinfo-dev libgmp-dev

# # Create symlink bind directory for build or haskell ide engine
# RUN mkdir -p $HOME/.local/bin

# # Install haskell ide engine
# RUN stack upgrade \
#     && git clone https://github.com/haskell/haskell-ide-engine --recurse-submodules \
#     && cd haskell-ide-engine \
#     && stack path --local-bin \
#     && stack ./install.hs help \
#     && stack ./install.hs stack-hie-8.6.5

# # Clean up
# RUN apt-get autoremove -y \
#     && apt-get clean -y \
#     && rm -rf /var/lib/apt/lists/*
# ENV DEBIAN_FRONTEND=dialog

# # Set the default shell to bash rather than sh
# ENV SHELL /bin/bash
FROM dogwith1eye/haskell-ide-engine:latest