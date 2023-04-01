# Julia Survey 2023 - Traducción al español


El notebook  `parse and compare julia survey.ipynb` toma las versiones 2023 y la 2022, las preprocesa y divide por pregunta. También tiene una cabecera y una cola (la cola la separe a mano).
Vectoriza cada parte para luego buscar el vecino más cercano de cada pregunta del 2023 en la 2022. Todo esto lo guarda en el directorio `survey` separado por id de bloque / pregunta (con un directorio asociado).

Con cada directorio se generaron 3 archivos:
- `23.txt`: pregunta del 2023
- `nearest-22.txt`: vecino más cercano de la pregunta en la versión del 2022
- `scores.txt`: resultados de la busqueda de los 3 vecinos cercanos (de la consulta del 23 y los 3nn del 22). Tiene id de los cercanos y distancia.
  La distancia es `1-cos`, entonces:
     - entre más cercano a cero quiere decir que se parecen las pregunta del 23 con el vecino del 22.
     - si la distancia es grande, se puede pensar que la pregunta no tiene correspondiente en el 22 o que cambio mucho
     - en cualquier coso se ponen los archivos para que la persona encargada de esa pregunta la traduzca


Propongo que haya un 4to archivo donde este la traducción

