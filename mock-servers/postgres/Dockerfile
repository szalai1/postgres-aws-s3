FROM postgres:13

RUN mkdir /tmp/extension
WORKDIR /tmp/extension

RUN apt-get update \ 
    && apt-get -y install python3-full python3-pip postgresql-plpython3-13 make python3-boto3
#RUN pip3 install boto3
COPY aws_s3--0.0.1.sql aws_s3.control Makefile ./
RUN make install
