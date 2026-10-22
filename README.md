# Instalacion base de datos mariaDB

## 1 Paso preparar el sistema
Lo primero sera actualizar las listas de paquetes y comprobar que el apache2 sigue funcionando, para hacer esto utilizaremos (sudo apt update) y (systemctl is-active apache2) 
<img width="439" height="64" alt="image" src="https://github.com/user-attachments/assets/08dfe1ea-380c-435a-bffd-d02518f60560" />
## 2 Paso instalacion mariadb
Ahora instalaremos mariadb que es el programa que gestiona la base de datos; usaremos (sudo apt install mariadb-server -y) para instalar el programa
<img width="932" height="74" alt="Captura de 2026-10-20 15-46-13" src="https://github.com/user-attachments/assets/eebbe85b-a501-48c3-b4b8-6b79e235e6e2" />

### 2.1 
Tambien comprobamos la version instalada con (mariadb --version) y deberemos ver algo parecido a esto 
<img width="817" height="55" alt="imagen" src="https://github.com/user-attachments/assets/f0336f66-e45c-4a68-bbca-965b8ca04209" />
## 3 Paso comprobar el funcionamiento
debemos moxtrar el estado del servicio para saber si esta activado correctamente; para ello usaremos los siguientes comandos "sudo systemctl status mariadb" para saber el estado, "systemctl is-enabled mariadb" para saber si el mariadb esta activado 
<img width="832" height="215" alt="imagen" src="https://github.com/user-attachments/assets/f7a77ddb-8c5c-4127-9bb7-ebd0b1e01a5f" />
<img width="438" height="33" alt="imagen" src="https://github.com/user-attachments/assets/8670885a-41a0-4f14-b024-886d79e0a058" />
### 3.2 
comprobaremos que podemos entrar en la base de datos poniendo "mariadb" y nos deberia salir algo como esto
<img width="716" height="200" alt="imagen" src="https://github.com/user-attachments/assets/417b24ba-e25a-4837-8aa0-aa69b57f6e15" />
despues pondriamos exit para salir de maria db
## 4 Instalacion de PHP
Instalamos el PHP ya que wordpress esta hecho en php; Instalaremos todo esto (sudo apt install php libapache2-mod-php php-mysql php-curl php-gd php-mbstring php-xml php-zip php-intl -y) tal cual.
Y luego deberemos hacer "php -v" y nos deberia salir algo como esto <img width="583" height="23" alt="imagen" src="https://github.com/user-attachments/assets/b1ffcac4-8b4c-4f79-8756-18aa8710ae32" />
tambien reiniciaremos el apache con "sudo systemctl restart apache2"
### 4.5 comprobar que apache ejecuta php
Para comprobar que se ejecuta el php pondremos lo siguiente (echo '<?php phpinfo();' | sudo tee /var/www/html/info.php) y abriremos la pagina con tu ip en el navegador y debaera aparecer una pagina morada
<img width="963" height="703" alt="Captura de 2026-10-22 18-41-36" src="https://github.com/user-attachments/assets/773c6cf5-f48d-47b1-9dda-b36c589bd6fe" />
## 5 comprobacion final
Para comprobar que lo hemos hecho todo bien usaremos (systemctl is-active apache2 mariadb y php -v)
<img width="576" height="145" alt="imagen" src="https://github.com/user-attachments/assets/5484a58c-1b6a-4843-9102-ab0cbc099f2c" />
