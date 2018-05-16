FROM dhub.sqil.by/oxdemo/oxdemo-core
MAINTAINER Alex Asabin

RUN apt-get update

#Clone oxdemo from github application
WORKDIR /root/projects
RUN git clone https://github.com/AlexAsabin/oxdemo

#Build oxdemo
WORKDIR /root/projects/oxdemo
RUN dotnet restore
RUN dotnet build

ENTRYPOINT ["/usr/bin/supervisord"]