# imagem base (fixar a versão da imagem garante que não vai quebrar o projeto por alguma atualização)
FROM node:16.13.2

# expõe a porta 8080 para o container
EXPOSE 8080

# cria o diretório de trabalho corrente
WORKDIR /app

# copia o package.json e o package-lock.json
COPY package*.json ./

# instala as dependências
RUN npm install

# copia o restante dos arquivos (importante usar um arquivo .dockerignore para ignorar arquivos desnecessários como a node_modules)
COPY . .

# executa a aplicação
CMD [ "node", "server.js" ]

# criar imagem: docker build -t gabriel9820/conversao-temperatura:v1 .
# criar container: docker container run -d -p 8080:8080 gabriel9820/conversao-temperatura:v1