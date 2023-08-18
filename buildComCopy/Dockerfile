FROM nginx:latest
LABEL maintainer 'luisa'

# Acessar index.html
RUN echo '<h1>Sem conteudo<h1>' > /usr/share/nginx/html/conteudo.html

# copy -> para que o index.html esteja na img gerada tem que ter copy
# qualquer arquivo .html que estiver na pasta do dockerfile vai ser enviado para pasta /usr
COPY *.html  /usr/share/nginx/html