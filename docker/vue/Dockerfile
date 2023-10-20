FROM node:lts-alpine

RUN apk update 
RUN apk add git

RUN mkdir /srv/dev_data

RUN chmod -R 777 /srv/dev_data
WORKDIR /srv/dev_data
RUN git clone https://github.com/rony-novaes/orders_cli.git
# faz da pasta 'app' o diretório atual de trabalho
WORKDIR /srv/dev_data/orders_cli
# instala dependências do projeto
RUN npm install
# compila a aplicação de produção com minificação
RUN npm run dev

EXPOSE 80 443