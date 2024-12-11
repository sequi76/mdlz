# Bayesian Machine Learning for Mondelez

Hay 2 archivos para hacer las predicciones y un archivo para testear.  Cada archivo se debe correr con una semana de diferencia.  Se corre el long.ipynb en la semana $n$, luego el short.ipynb el lunes temprano de la semana $n+1$ y genera las predicciones de compra para esa semana.  Y luego en la semana $n+2$ se corre un file la-vendimia-test\_short-long.ipynb que permite copmrar el output del short.ipynb con lo sucedido en la semana anterior.

Para correr cada script hace falta traer el output del query al directorio data/vendimia/ y llamarlo (p.ej.) 20241204-rosario-full.csv si es del día 2024/12/04. También se debe modificar ese filename en los correspondientes scripts long.ipynb, short.ipynb y la-vendimia-test\_short-long.ipynb.  Cada script requiere el output del query de su correspondiente semana, y también cad script utiliza el output del script de la semana anterior (que también hay que updatearle el nombre correpsondiente).

## Semana n

- long.ipynb : se debe correr durante la semana sin apuro con los datos hasta el último día que se updateó la base.  Le toma unas 2-3 horas correr (con 32 núcleos).  Este script genera un output en         
data/vendimia/details_'+timestamp+'.pkl 


## Semana n+1

- short.ipynb : se corre apenas se updatea la base de Mondelez, generalmente lunes temprano.  Utiliza el output del script anterior, y genera el file 

data/vendimia/results\_short\_days_'+str(maxday)+'-'+str(maxdaynew)+'.pkl

## Semana n+2

Para testear el resultado de la predicción de la semana anterior con las transacciones que verdaderamente ocurrieron, se debe correr el archivo

- la-vendimia-test\_short-long.ipynb

### Nota:

[Por una cuestión de espacio en el github, no hay en este repo ninguno de los files enormes de las queries a la database]



