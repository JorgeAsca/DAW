FROM ubuntu

# Instalación de paquetes necesarios
RUN apt update && apt install -yq --no-install-recommends \
    apache2 \
    curl \
    nano \
    net-tools \
    iputils-ping

# Crea el directorio si no existe (Corregido: mkdir -p)
RUN mkdir -p /root/admin/base

# Directorio actual dentro del contenedor
WORKDIR /root/base/Ubuntu/admin

# Copia el script de inicio y le da permisos de ejecución
COPY ./Dockerfile/base/Ubuntu/admin/start.sh .
RUN chmod +x ./start.sh

# El script de arranque
ENTRYPOINT [ "./start.sh" ]