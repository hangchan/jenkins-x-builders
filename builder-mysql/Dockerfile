FROM hang/builder-base:2.1.4

ENV YUM_REPO_URL="https://dev.mysql.com/get/mysql57-community-release-el7-10.noarch.rpm"
RUN \
	yum -y install epel-release && \
	rpm -ivh ${YUM_REPO_URL} && \
	yum-config-manager --disable mysql55-community && \
	yum-config-manager --disable mysql56-community && \
	yum-config-manager --enable mysql57-community && \
	yum-config-manager --disable mysql80-community && \
	yum clean all
RUN yum -y install \
	mysql-community-client

CMD ["mysql", "--version"]
