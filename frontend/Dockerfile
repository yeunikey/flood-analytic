# Используем официальный образ Node.js
FROM node:18-alpine

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем файлы package.json и package-lock.json
COPY package*.json ./

# Устанавливаем зависимости
RUN npm install

# Устанавливаем Vite глобально
RUN npm install -g vite

# Копируем весь фронтенд-код
COPY . .

# Открываем порт для фронта
EXPOSE 7001

# Запускаем приложение
CMD ["npm", "run", "dev"]
