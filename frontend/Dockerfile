# Usar la imagen minimalista de Nginx
FROM nginx:alpine

# Copiar todo el contenido de la carpeta local frontend a la ruta pública de Nginx
COPY . /usr/share/nginx/html

# Exponer el puerto 80
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]