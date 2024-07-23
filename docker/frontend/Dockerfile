# frontend/Dockerfile

FROM node:14-alpine

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем package.json и package-lock.json
COPY package*.json ./

# Устанавливаем зависимости
RUN npm install

# Копируем весь проект
COPY . .

# Строим проект
RUN npm run build

# Экспонируем порт
EXPOSE 3000

# Запускаем приложение
CMD ["npm", "start"]
