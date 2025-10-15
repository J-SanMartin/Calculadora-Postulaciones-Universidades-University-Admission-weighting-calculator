# Calculadora Postulaciones Universidades
El objetivo de este proyecto es consolidar la informacion de ponderaciones de las pruebas de admision PAES que requiere cada universidad en Chile para sus respectivas carreras y con esta construir una calculadora que pueda entregar una aproximacion del puntaje que esperan obtener los postulantes a estas carreras ademas de mostrarles como es el proceso de calculo. Es importante destacar que esta calculadora fue desarrollada para una escuela cientifico - humanista
## Sobre el proyecto
1. **Objetivo**: Extraer ponderaciones de cada prueba requerida de las 47 universidades adscritas al proceso de admision centralizado mediante PAES para construir una calculadora de postulaciones.
2. **Fuentes de datos**: Se utiliza informacion disponible en DEMRE (https://demre.cl)
3. **Resultado**: Archivo CSV con la informacion solicitida para construir la calculadora

## Pasos Seguidos
1. **PDF**: El DEMRE entrega la informacion sobre el proceso de postulacion a traves del archivo 'Oferta Definitiva_DEMRE' donde podemos encontrar texto, tablas e informacion mixta sobre las 47 universidades adscritas proceso, por lo que se genera un archivo PDF llamado 'Tablas' que contiene solo las tablas con la informacion que se quiere extrer
2. **Extraccion de Datos**: Utilizando la libreria 'Camelot' de Python, se extrae la informacion contenida en el archivo PDF generado, guardando todas las tablas en un unico dataframe
3. **Limpieza y ajuste de datos**: Una vez consolidada la informacion en un dataframe, se realizan ajustes en los nombres de columnas, universidades correspondientes, etc. En este paso se encontraron algunos detalles respecto a datos faltantes o problemas menores que son ajustados de manera posterior en excel
4. **Exportacion de datos**: Toda la informacion obtenida y consolidada es extraida en formato .xlsx para revision de detalles menores y su uso en la calculadora
5. **Calculadora**: Se utilizan los datos para construir una calculadora de postulaciones para los aplicantes de un colegio cientifico - humanista
