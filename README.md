# Ejercicio_19

## Layout (TableLayout)

Disponer 9 botones en forma de un tablero de TaTeTi. Utilizar un TableLayout, tres TableRow y nueve botones.

1) Buscamos "TableLayout" y la arrastramos a la ventana 'Component Tree', cuando disponemos el objeto dentro de la ventana podemos ver en el "Component Tree" que el TabletLayout contiene 4 objetos de tipo "Table Row". <br>
![image](https://user-images.githubusercontent.com/66330281/219246900-8e7a7683-97a6-44fd-86ac-302cca540234.png)

2) Debemos arrastrar cada uno de los 9 botones al TableRow respectivo. <br>
![image](https://user-images.githubusercontent.com/66330281/219247476-2d730bf7-4211-4780-a450-20516da68bd4.png)

3) Ahora seleccionamos los nueve botones y fijamos la propiedad 'layout_height' con el valor 'match_parent' para que se estiren ocupando todo el espacio de la fila, También estando seleccionado los nueve botones fijamos la propiedad 'layout_weight' con 1
![image](https://user-images.githubusercontent.com/66330281/219248019-214ba1ed-552c-471d-84cd-582c756f3b14.png)

<b>De esta forma no importa que tan grande sea el dispositivo, los botones se redimensionan y ocupan todo el espacio.</b><br>
![image](https://user-images.githubusercontent.com/66330281/219248118-2abbada1-dc7a-4d75-9428-e82476b79b4d.png)
