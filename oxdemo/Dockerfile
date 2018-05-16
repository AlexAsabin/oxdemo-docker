FROM dhub.sqil.by/oxdemo/oxdemo-core
MAINTAINER Alex Asabin

RUN apt-get update

#Clone OXF from github application
WORKDIR /root/projects
RUN git clone https://github.com/AlexAsabin/oxdemo

#Build OXF
WORKDIR /root/projects/oxf
RUN dotnet restore
RUN dotnet build

ENTRYPOINT ["/usr/bin/supervisord"]