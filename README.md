# Practica-13-Moodle

# 1 crearmos la maquina en amazon con ubuntu

- 1.1 Seleccionamos la AMI para instalar el sistema
- 1.2 Seleccionamos el tipo de instancia
- 1.3 Configuramos la instancia (red, ip...)
- 1.4 Le asignamos una unidad de almacenamiento y su capacidad
- 1.5 TAGS: palabras clave que ayudan a encontrar la maquina
- 1.6 Reglas de seguridad: agragamos SSH ,HTTP y HTTPS para que se abran esos puertos y podamos acceder a tanto la maquina como la pagina web
- 1.7 Creamos un certificado para poder acceder la maquina via SSH remotamente
- 1.8 Accedemos por consola a  la carpeta donde se encuentra el certificado
- 1.9 Le cambiamos los permisos al certificado
   
  ```bash
    chmod +x nombre-certificado.pen
  ``` 
    
- 1.10 Conectamos a la maquina poniendo en consola:    
     ```bash
    ssh -i "nombre-certificado.pem" usuario@DNS-publico-de-la-maquina
		  Ejemplo:
            		ssh -i "ubuntu-18.04.pem" ubuntu@ec2-18-212-164-248.compute-1.amazonaws.com
    ```


# 2 Descargamos Drupal
```bash
		wget https://bitnami.com/redirect/to/371224/bitnami-moodle-3.5.3-1-linux-x64-installer.run
  ```
# 3 le cambiamos los permisos

```bash
		chmod +x bitnami-moodle-3.5.3-1-linux-x64-installer.run
```
# 4 comenzamos la instalacion
```bash
	sudo	./bitnami-moodle-3.5.3-1-linux-x64-installer.run
```
- 4.1 Utilidades 
- 4.2 Seleccionamos la carpeta donde la vamos a instalar
- 4.3 Creamos el usuario de administrador (	nombre, correo, usuario, contraseña)
-	4.4 Le ponemos un nombre a la pagina
-	4.5 Le podemos configurar el soporte de correo (en este caso no)
-	4.6 Comienza a instalarse
