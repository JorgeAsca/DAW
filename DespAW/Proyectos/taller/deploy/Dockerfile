FROM httpd:2.4

# Declarar las variables para que Docker las reconozca desde los --build-arg
ARG TIPO
ARG PROYECTO

# Ahora las variables tendrán el valor pasado por consola
COPY ./proyectos/${TIPO}/${PROYECTO}/src/ /usr/local/apache2/htdocs/

EXPOSE 80