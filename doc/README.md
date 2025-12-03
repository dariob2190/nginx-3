# Práctica 2.3: Acceso seguro con Nginx

## Sumario:

1.  Configuración de Nginx
2.  Configuración del cortafuegos
3.  Generar un certificado autofirmado
4.  Configuración final y activación SSL
5.  Prueba de funcionamiento

## 1. Configuración de Nginx

Lo primero que haremos será modificar el nombre del servidor para incluir el subdominio `www`. Editamos el fichero de configuración de nuestro sitio:

```
sudo nano /etc/nginx/sites-available/luisdario.test
```

Buscamos la directiva `server_name` y la dejamos así:

```
server_name luisdario.test www.luisdario.test;
```

Una vez modificado, comprobamos que no hemos introducido ningún error de sintaxis y reiniciamos el servicio:

```
sudo nginx -t
sudo systemctl restart nginx
```
