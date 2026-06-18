# Utilizar una imagen base oficial de Node.js ligera basada en Alpine Linux
FROM node:20-alpine

# Establecer el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar primero los archivos de dependencias para aprovechar la caché de capas de Docker
COPY package*.json ./

# Instalar solo las dependencias necesarias de producción de forma limpia
RUN npm ci --only=production

# Copiar el resto del código fuente de la aplicación
COPY . .

# Exponer el puerto en el que escucha tu API de Node.js (comúnmente 3001)
EXPOSE 3001

# Comando por defecto para arrancar la aplicación
CMD ["npm", "start"]