# based1
Proyecto de una base de dato para el Liceo municipal F860

Que códigos utilizamos en la base de datos.
CREATE TABLE PAIS(
    ID_PAIS INT PRIMARY KEY NOT NULL,
    PAIS TEXT(15));
este código o tabla sirve para identificar de que país o nacionalidad, de donde proviene el autor.


CREATE TABLE EDITORIAL(
    ID_EDITORIAL INT PRIMARY KEY NOT NULL,
    EDITORIAL TEXT(20));
este código o tabla sirve para identificar la editorial de cada libro.


CREATE TABLE AUTOR(
    ID_AUTOR INT AUTO_INCREMENT PRIMARY KEY NOT NULL,
    AUTOR TEXT(30));
Esta table sirve para identificar el autor del libro.


CREATE TABLE UBICACION(
    ID_UBICACION INT AUTO_INCREMENT PRIMARY KEY NOT NULL,
    UBICACION TEXT(30));
Esta tabla nos servirá para saber dónde está el libro en la biblioteca o quien se lo ha llevado anteriormente.

CREATE TABLE LIBRO(
ID_LIBRO Int PRIMARY KEY NOT NULL,
TITULO VARCHAR(30),
EDICION VARCHAR(20),
TIPO_LIBRO VARCHAR(30),
FECHA_LANZAMIENTO Date,
ID_EDITORIAL Int,
ID_AUTOR Int,
ID_PAIS Int,
ID_UBICACION Int,
COPIA_LIBRO Int,
CONSTRAINT EDITORIAL FOREIGN KEY (ID_EDITORIAL) REFERENCES EDITORIAL(ID_EDITORIAL),
CONSTRAINT AUTOR FOREIGN KEY (ID_AUTOR) REFERENCES AUTOR(ID_AUTOR),
CONSTRAINT PAIS FOREIGN KEY (ID_PAIS) REFERENCES PAIS(ID_PAIS),
CONSTRAINT UBICACION FOREIGN KEY (ID_UBICACION) REFERENCES UBICACION(ID_UBICACION) 
)

Esta es la tabla que esta totalmente conectado con casi todos los atributos de las otras tablas (autor, ubicación, editorial,  )
