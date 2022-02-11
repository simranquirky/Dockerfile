FROM ubuntu:latest
MAINTAINER simran <simrankumari1344@gamil.com>
RUN apt-get update && apt-get install -y curl wget
RUN curl -s https://api.github.com/repos/kubernetes-sigs/kind/releases/latest| grep browser_download_url | grep kind-linux-amd64 | cut -d '"' -f 4  | wget -qi -
RUN chmod a+x kind-linux-amd64
RUN sudo mv kind-linux-amd64 /usr/local/bin/kind
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
RUN chmod +x ./kubectl
RUN sudo mv ./kubectl /usr/local/bin/kubectl
RUN echo "source <(kubectl completion bash)" >> ~/.bashrc
