FROM python:3.6
LABEL maintainer 'ALUNO COD3R'

#A partir daqui é criado novas layers
#É possível concatenação de comandos -> criada apenas uma layer
#&& -> concatenação de comandos 
# \ -> quebra linha
#mkdir -> gera pasta /pasta
#chown -> dono da pasta
RUN useradd www && \
    mkdir /app && \ 
    mkdir /log && \
    chown www /log

#Define usuário ativo -> quem vai realizar processos dentro do container
#VOLUME -> aponta para pasta log -> outro container pode ler 
#workdir -> diretorio de trabalho
#Expor porta -> pode ser remapeada ou não
USER www
VOLUME /log
WORKDIR /app
EXPOSE 8000

#Local que será iniciado

ENTRYPOINT [ "/usr/local/bin/python" ]
CMD ["run.py"]