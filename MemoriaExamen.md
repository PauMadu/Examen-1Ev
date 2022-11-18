# Introduccion.

## Indice.
Este trabajo recopila información de los tres ejercicios propuestos en el Examen de la 1a Evaluación.

## Contexto.
Este proyecto se ha realizado en el centro didáctico ["Ágil Centros"](https://www.agilcentros.es/audio/index.php), 
en la asignatura de Despliegue de Aplicaciones Web donde ha sido el Examen de la 1a Evaluación.

## Ejercicio 2.
En este ejercicio primeramentre tendremos que entrar en una maquina mediante SSH, y lo haremos de la siguiente forma:
```
$ ssh ejerciciossh@192.168.0.---
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

## Ejercicio 4.

## ¿Qué se ha conseguido?
Con este trabajo realizado se ha conseguido recopilar toda la información aprendida durantes estos dos meses, 
además queda justificada con los ejercicios practicos, y almacenada en Github.

## Valoración personal.
Personalmente estoy contento con mi prograso, aunque siento que soy el que mas perdido va de toda la clase en esta asignatura, 
aunque es totalmente noramal porque nunca habia tocado linux ni su terminal, aparte de MarkDown, Apache y SSH.

## Bibliografía.
- []()
- []()
