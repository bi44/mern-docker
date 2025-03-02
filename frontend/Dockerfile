# Используем лёгкий образ с Node.js
FROM node:20-alpine

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем package.json и устанавливаем зависимости
COPY package.json package-lock.json* yarn.lock* ./
RUN npm install

# Копируем весь код
COPY . .

# Открываем порт Vite
EXPOSE 5173

# Запускаем проект
CMD ["npm", "run", "dev"]
