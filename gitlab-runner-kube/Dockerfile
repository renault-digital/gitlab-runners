FROM renaultdigital/gitlab-runner-base


ENV GLIBC_VERSION 2.26-r0
ENV HELM_VERSION 2.7.0

RUN     curl -L -o /etc/apk/keys/sgerrand.rsa.pub https://raw.githubusercontent.com/sgerrand/alpine-pkg-glibc/master/sgerrand.rsa.pub  && \
	curl -L -O https://github.com/sgerrand/alpine-pkg-glibc/releases/download/${GLIBC_VERSION}/glibc-${GLIBC_VERSION}.apk && \
	apk add glibc-${GLIBC_VERSION}.apk && \
	rm glibc-${GLIBC_VERSION}.apk && \
	curl -L https://storage.googleapis.com/kubernetes-helm/helm-v${HELM_VERSION}-linux-amd64.tar.gz | tar xz && \
	mv linux-amd64/helm /usr/bin/ && \
	helm version --client && \
	curl -L -o /usr/bin/kubectl https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl && \
	chmod +x /usr/bin/kubectl && \
	kubectl version --client
