# Ejercicio_14
## Almacenamiento de datos en un archivo de texto en la memoria interna

Confeccionar un programa para administrar un calendario de actividades diarias. Los nombres de archivos corresponderán a las fechas que ingresamos. Luego cuando consultamos una fecha verificamos si hay un archivo de texto que coincida con dicha fecha.

1) El diseño visual de la aplicación sera la siguiente <br>
![image](https://user-images.githubusercontent.com/66330281/219221475-50b89953-4b0d-4bdf-b5c2-131895f2bee7.png)

2) La configuración de los atributos de los botones son los siguientes:<br>
<code>TextView (text="Ingrese fecha")
  EditText de tipo "Date" (ID="et1")
  Button (text="Grabar", onClick="grabar")
  Button (text="Recuperar" onClick="recuperar")
  EditText de tipo "Multiline Text" (id="et2", background="#ffff00")</code>
  
3) Método "grabar", se ejecuta cuando presionamos el botón "Grabar" primero se extrae la fecha ingresada en el primer EditText y se reemplaza las barras de la fecha por guiones. Luego procedemos a llamar al método write y le pasamos el String a grabar, en este caso extraemos los datos del EditText. Finalmente llamamos al método flush para que vuelque todos los datos que pueden haber quedado en el buffer y procedemos al cerrado del archivo. <br>
![image](https://user-images.githubusercontent.com/66330281/219223316-4158903e-08a0-4095-b2e5-5ae4e1d9b561.png)

4) Método "recuperar", primero se recuperr del EditText la fecha que ingresó el operador para buscar, despues se reemplaza las barras por guiones y se obtiene la lista de todos los archivos que almacena la aplicación mediante la llamada al método fileList(), luego mediante un for recorremos el vector con los nombres de archivos y los comparamos con la fecha ingresada, si es "true" significa que existe el archivo por lo que procedemos a abrirlo, leerlo y cargar el et2 con los datos del archivo.
![image](https://user-images.githubusercontent.com/66330281/219223786-666ad0f1-b1df-4aec-bd09-078d66c1af69.png)

<b>La interfaz visual en tiempo de ejecución</b><br>
![image](https://user-images.githubusercontent.com/66330281/219223899-965eaaef-e944-4a90-a5cd-1c12eaadd10a.png)
![image](https://user-images.githubusercontent.com/66330281/219224089-f4fc589b-c8af-4d73-86f9-eb5e3ccc36d6.png)
![image](https://user-images.githubusercontent.com/66330281/219224215-1cc0ec82-f62a-4caa-ab0a-1cec62ab6150.png)


