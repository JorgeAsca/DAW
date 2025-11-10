FROM ubuntu
RUN apt update && apt install -yq --no-install-recommends \
    apache2 \
    curl \
    nano \
    net-tools iputils-ping+
# tail es un proceso que nunca acaba 
# Delegamos la configuracion de las imagenes a los llamos script points (scrpit de inicio para un contenedor)
# CMD [ "tail", "-f", "/dev/null" ]

RUN -p mkdir /root/base/Ubuntu/admin
# Directorio actual dentro del contenedor
WORKDIR /root/base/Ubuntu/admin
COPY ./Dockerfile/base/Ubuntu/admin .
RUN chmod o+x ./start.sh

# Script de arranque para crear la ISO y ejecutar el contenedor 
ENTRYPOINT [ "./start.sh" ]