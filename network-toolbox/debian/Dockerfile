FROM debian:stretch-slim

RUN apt-get update && apt-get install -y --no-install-recommends \
		bash-completion \
		ca-certificates \
		curl \
		dnsutils \
		gnupg dirmngr \
		inetutils-ping \
		iperf \
		iproute2 \
		iptables \
		nbtscan \
		net-tools \
		netcat-openbsd \
		openssh-client \
		procps \
		rsync \
		socat \
		traceroute \
		tshark \
		wget \
	&& rm -rf /var/lib/apt/lists/*

RUN wget https://github.com/fullstorydev/grpcurl/releases/download/v1.0.0/grpcurl_1.0.0_linux_x86_64.tar.gz \
	&&	tar -xzf grpcurl_1.0.0_linux_x86_64.tar.gz \
	&&	mv grpcurl /usr/local/bin/ \
	&&	rm LICENSE grpcurl_1.0.0_linux_x86_64.tar.gz

CMD ["bash", "--login", "-i"]
