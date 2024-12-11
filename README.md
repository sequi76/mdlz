# Bayesian Machine Learning for Mondelez

Hay 2 archivos claves y un archivo para testear.  Cada archivo se debe correr con una semana de diferencia.


## Semana n

- long.ipynb : se debe correr durante la semana sin apuro con los datos hasta el último día que se updateó la base.  Le toma unas 2-3 horas correr (con 32 núcleos).  Este script genera un output en         
data/vendimia/details_'+timestamp+'.pkl 


## Semana n+1

- short.ipynb : se corre apenas se updatea la base de Mondelez, generalmente lunes temprano.  Utiliza el output del script anterior, y genera el file 

data/vendimia/results\_short\_days_'+str(maxday)+'-'+str(maxdaynew)+'.pkl

## Semana n+2

Para testear el resultado de la predicción de la semana anterior con las transacciones que verdaderamente ocurrieron, se debe correr el archivo

- la-vendimia-test\_short-long.ipynb

## Instrucciones generales

En cada semana se debe hacer la query al Google Cloud y traer los datos correspondientes.  Todos esos files van en el directorio 'data/vendimia', que es también donde van los outputs de los scripts.



