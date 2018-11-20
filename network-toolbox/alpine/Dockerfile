FROM alpine:3.8

RUN apk add --no-cache \
		bash \
		bash-completion \
		bind-tools \
		ca-certificates \
		curl \
		gnupg \
		iperf \
		iptables \
		iputils \
		libressl \
		net-tools \
		openssh-client \
		rsync \
		socat \
		tshark \
		wget
# TODO add "nbtscan" when we get to Alpine 3.9 (if it makes it out of edge for 3.9)

RUN wget https://github.com/fullstorydev/grpcurl/releases/download/v1.0.0/grpcurl_1.0.0_linux_x86_64.tar.gz \
	&&	tar -xzf grpcurl_1.0.0_linux_x86_64.tar.gz \
	&&	mv grpcurl /usr/local/bin/ \
	&&	rm LICENSE grpcurl_1.0.0_linux_x86_64.tar.gz

CMD ["bash", "--login", "-i"]
