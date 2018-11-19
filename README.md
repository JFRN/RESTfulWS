# RESTfulWS
Evidencia de Computación avanzada en Java

## Instalación
1. Clona el proyecto
2. Importa el proyecto en tu IDE favorito
3. Conviertelo a Maven y actualizalo

Con esto debería ser posible correrlo en un servidor como Tomcat

## Uso
RESTful API

**Recurso /api/v1/**  
1. **GET**: Lista los recursos disponibles.
2. **OPTIONS**: Documentación del recurso.

**Recurso /api/v1/file**  
1. **GET**: Descarga un archivo mediante el parámetro path. 
```
api/v1/file/?path=
```
2. **POST**: Sube un archivo mediante los parámetros name, dir y file.
```
api/v1/file/ name="imagen.jpg" dir="/Files" file@/Users/Usuario/Downloads/imagneasubir.jpg --form
```
3. **DELETE**: Elimina un archivo mediante el parámetro path.
```
api/v1/file/?path=
```
4. **OPTIONS**: Documentación del recurso.

**Recurso api/v1/directory**  
1. **GET**: Lista los archivos de un directorio mediante el parámetro dir. 
```
api/v1/directory/?dir=
```
2. **OPTIONS**: Documentación del recurso.

**Recurso api/v1/notify**  
1. **GET**: Lista las notificaciones enviadas.
2. **POST**: Envía una notificación mediante los parámetros subject, message, toAddress y ccAddress.
```
api/v1/notify subject="hola" message="Hola de RestfulWS" toAddress="a@b.com" ccAddress="a@b.com"
```
3. **OPTIONS**: Documentación del recurso.

**Recurso api/v1/user**  
1. **GET**: Lista los usuarios.
2. **POST**: Crea un usuario mediante los parámetros username, password y fullName.
```
api/v1/user username="user" password="pass" fullName="John Doe"
```
3. **OPTIONS**: Documentación del recurso.

**Recurso api/v1/user/{username}**  
1. **GET**: Muestra la información del usuario.
2. **PUT**: Actualiza la información del usuario mediante los parámetros username, password y fullName.
```
api/v1/user/user username="user" password="pass" fullName="Jose Martinez"
```
3. **DELETE**: Elimina al usuario.
4. **OPTIONS**: Documentación del recurso.

## Créditos

José Rada 2716544
Curso de CAJ

## Licencia MIT

Copyright (c) 2018 Jose Rada

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.