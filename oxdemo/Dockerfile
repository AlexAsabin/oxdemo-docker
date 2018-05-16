FROM dhub.sqil.by/oxdemo/oxdemo-core
MAINTAINER Alex Asabin

#Clone oxdemo from github application
RUN mkdir /home/oxuser/projects
WORKDIR /home/oxuser/projects

RUN git clone https://github.com/AlexAsabin/oxdemo

#Build oxdemo
WORKDIR /home/oxuser/projects/oxdemo
RUN dotnet restore
RUN dotnet build

ENTRYPOINT ["/usr/bin/supervisord"]