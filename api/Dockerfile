FROM node:20-alpine3.17
# створення робочої папки застосунку
WORKDIR /usr/src/app
# копіювання package.json та встановлення залежностей
COPY package*.json ./
# Встановлення nodemon 
RUN npm install && npm install -g nodemon
# копіюємо вихідний код в робочу папку
COPY . .
# повідомляємо Docker, що в контейнері є застосунок, що прослуховує даний порт
EXPOSE 3001
# реєструємо команду для необхідності запуску застосунку при запуску контейнера
CMD [ "npm", "run", "dev" ]