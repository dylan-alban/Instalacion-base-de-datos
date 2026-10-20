# Instalacion base de datos mariaDB

## 1 Paso
Lo primero sera actualizar las listas de paquetes y comprobar que el apache2 sigue funcionando, para hacer esto utilizaremos (sudo apt update) y (systemctl is-active apache2) 
<img width="439" height="64" alt="image" src="https://github.com/user-attachments/assets/08dfe1ea-380c-435a-bffd-d02518f60560" />
## 2 Paso 
Ahora instalaremos mariadb que es el programa que gestiona la base de datos; usaremos (sudo apt install mariadb-server -y) para instalar el programa
<img width="932" height="74" alt="Captura de 2026-10-20 15-46-13" src="https://github.com/user-attachments/assets/eebbe85b-a501-48c3-b4b8-6b79e235e6e2" />

### 2.1 
Tambien comprobamos la version instalada con (mariadb --version) y deberemos ver algo parecido a esto (imagen)

