# Introduccion.
Este trabajo recopila información de los tres ejercicios propuestos en el Examen de la 1a Evaluación.

## Palabras Clave
1. SSH.
2. VirtualHost.
3. Hosts.

## Indice.
- Contexto 
- Ejercicio 2
- Ejercicio 3
- Ejercicio 4
- Que se ha conseguido
- Valoracion personal
- Bibliografia

## Contexto.
Este proyecto se ha realizado en el centro didáctico ["Ágil Centros"](https://www.agilcentros.es/audio/index.php), 
en la asignatura de Despliegue de Aplicaciones Web donde ha sido el Examen de la 1a Evaluación.

## Ejercicio 2.
En este ejercicio primeramentre tendremos que entrar en una maquina mediante SSH, y lo haremos de la siguiente forma:
```
$ ssh usuario@192.168.0.---
```
E introduciremos la contraseña.
A continuacion nos pide que vayamos a /var/www
```
$ cd /var/www
```
Pero nos deja viajar porque no existe el directorio.
Se me ha ocurrido entrar en /var, par comprobar si este existe y buscar directamente dentro de el.
```
$ cd /var
$ ls 
$ ls -a
```
Tampoco he conseguido nada.
Despues de 30 minutos entrando y saliendo de directorios, intentando buscar, siendo sinceros no entiendo porque, he vuelto a introducir "$ cd /var/www"
y ahora si que he conseguido entrar.
Por lo tanto vamos a crear la carpeta con nuestro nombre.
```
$ sudo mkdir PauMadueño
```
No nos deja porque no tenemos permisos...
```
$ sudo mkdir PauMadueño
```
Ahora ya tenemos creada la carpeta.
Nos posicionamos dentro de ella.
```
$ cd /var/www/PauMadueño
```
Y por último crearemos un archivo:
```
$ sudo touch ejercicio2.txt
```
Y la comprobación:  
![comprobación](https://github.com/PauMadu/Examen-1Ev/blob/main/Comprobacion%20Ej2.png)

## Ejercicio 3.
He buscado como descragar una imagen, pero no he encontrado una solucion util, asi que he intentado descargarme la imagen en mi usuario, y pasarla dentro de mi carpeta en la maquina.
```
$ sudo scp Escritorio/daw.png usuario@192.168.0.168:/var/www/PauMadueño/
```
No entiendo que esta mal, pero resulta que no tengo permiso.

## Ejercicio 4.
Para crear un VirtualHost primero deberemos crear un directorio:
```
$ sudo mkdir /var/www/gci
```
Le damos permisos:
```
$ sudo chmod 777 /var/www/gci
```
Y creamos la pagina:
```
$ sudo nano /var/www/gci/index.html
```
Y cuando se nos habra el editor le he añadido:
```
<html>
    <head>
        <title>Welcome to Your_domain!</title>
    </head>
    <body>
        <p>Pau Madueño Sanchez</p>
    </body>
</html>
```
Guardamos y cerramos.
Para configurar el archivo de configuración de VirtualHost.
```
$ cd /etc/apache2/sites-available/
$ sudo cp 000-default.conf gci.conf
```
Entonces ya podremos editar la configuración.
```
$ sudo nano gci.conf
```
Y dentro...
> ServerName daw.ejercicio4.com  
> DocumentRoot /var/www/gci/
Para finalizar la configuración de nuestro sitio web tendremos que activar el archivo de hosts virtuales;
```
$ sudo a2dissite gci.conf
$ service apache2 reload
$ sudo a2ensite gci.conf
$ service apache2 reload
```
En mi caso me ha surgido un error por lo cual he tenido que hacer lo siguiente:
```
$ sudo gedit /etc/hosts
```
> 127.0.0.1 gci.example.com

## ¿Qué se ha conseguido?
Con este trabajo realizado se ha conseguido recopilar toda la información aprendida durantes estos dos meses, 
además queda justificada con los ejercicios practicos, y almacenada en Github.

## Valoración personal.
Personalmente estoy contento con mi prograso, aunque siento que soy el que mas perdido va de toda la clase en esta asignatura, 
es totalmente noramal porque nunca habia tocado linux ni su terminal, aparte de MarkDown, Apache y SSH.

## Bibliografía.
- [Mis apuntes](https://github.com/PauMadu/Tema-3/blob/main/MemoriasApache.md)
- [Comandos](https://apuntesjulio.com/comandos-para-linux/)
