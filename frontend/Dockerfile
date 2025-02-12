# Usar a imagem base do Node.js com Debian
FROM node:22

# Instalar dependências do sistema necessárias para o Next.js
RUN apt-get update && apt-get install -y libc6

# Definir o diretório de trabalho
WORKDIR /app

# Copiar os arquivos de dependência (package.json e package-lock.json)
COPY package.json package-lock.json ./

# Instalar as dependências do projeto
RUN npm install

# Copiar o restante dos arquivos do projeto
COPY . .

# Expor a porta 3000 para o Next.js
EXPOSE 3000

# Comando para iniciar o servidor Next.js
CMD ["npm", "run", "dev"]
