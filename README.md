# Nginx_Proxy_Nodejs
Configuracion basica proxy aplicación Nodejs en Nginx

Puerto de Nginx -> 80

Puerto de app Nodejs -> 3000

Dominio -> example.com

location / {
		proxy_pass http://localhost:3000;
		proxy_http_version 1.1;
		proxy_set_header Upgrade $http_upgrade;
		proxy_set_header Connection 'upgrade';
		proxy_set_header Host $host;
		proxy_cache_bypass $http_upgrade;
	}
