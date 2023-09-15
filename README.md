1. Generate .htpasswd файл на https://hostingcanada.org/htpasswd-generator/
  - скопировать эти данные в .htpasswd файл
2. Открыть порт 7860 на NAT
3. docker run -d -p 7860:80 -v %cd%/nginx.conf:/etc/nginx/nginx.conf:ro -v %cd%/.htpasswd:/etc/nginx/.htpasswd:ro nginx

