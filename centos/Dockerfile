FROM centos:latest
WORKDIR /build
RUN yum -y install epel-release \
                   gcc \
                   python-devel \
                   openldap-devel
RUN yum -y update
RUN yum -y install python-pip
RUN pip install virtualenv && virtualenv /tmp/venv
CMD ["/tmp/venv/bin/pip", "install", "-r", "requirements.txt", "-t", "/build"]
