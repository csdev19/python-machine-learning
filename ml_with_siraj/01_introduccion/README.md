# Introduccion del curso de Data Cience con Python


## Para realizar un modelo de clasificacion usaremos **4 pasos**:

1. Install Python
2. Setup Environment
3. Install Dependencies
4. Write Python Script


## Justificacion:

Ahora los primeros dos pasos los obviaremos. Porque? porque la instalacion de python es algo un poco tedioso de hacer para mi en cada documentacion y segundo a lo que se refiere con **setup environment** es instalar **sublime text3** y usarlo como ambiente de desarrollo y compilandolo desde terminal.

## Ahora lo insteresante:

Los paquetes que vamos a usar y obviamente el script. En este caso tratare de dejar un **requirements.txt** para los paquetes usados si llegan a ser muchos. Y explicare lo que hace el script y si no lo entiendo lo googleo igual  XD.

Bueno segun parece solo usaremos **scikit-learn** asi que pondre el como se instala. Y lo recomendable como siempre seria usar ambientes virtuales y ya tengo un repo acerca de eso asi que ni me esforzare en explicar que es.

En caso de fallas entrar a este [link](https://stackoverflow.com/questions/46113732/modulenotfounderror-no-module-named-sklearn) a mi me sirvio

```console
pip install scikit-learn # actualizacion si no compila porque no encuentra sklearn usa el -U

# En caso de querer instalarlo de forma global tendrian que usar sudo como prefijo desde el inicio

# Y en el tutorial decia

## De prferencia usar este comando
pip install -U scikit-learn
# pero en este caso no lo usaremos -U es para actualizar (upgrade)
```


Ahora veremos la parte del script. En caso de ser muy largo sera puesto en un archivo aparte en caso de no serlo sera incrustado gracias al MD.
Dado que el codigo es un poco corto vamos a mostrarlo todo y luego lo explicaremos.

```python
from sklearn import tree


# [height, weight, shoe_size]
X = [[181, 80, 44], [177, 70, 43], [160, 60, 38], [154, 54, 37], [166, 65, 40], [190, 90, 47], [175, 64, 39], [177, 70, 40], [159, 55, 37], [171, 75, 42], [181, 85, 43]]

Y = ['male', 'male', 'female', 'female', 'male', 'male', 'female', 'female','female', 'male', 'male']


# CHALLENGE - ...and train them on our data
clf = tree.DecisionTreeClassifier()
clf = clf.fit(X, Y)

prediction = clf.predict([[190, 70, 43]])

# CHALLENGE compare their results and print the best one!

print(prediction)
```

Este fue el codigo ahora la explicacion.

```python
from sklearn import tree
```
En este pedazo de codigo importamos el modulo TREE de SCIKIT-LEARN (sklearn). Este modulo nos permitira construir un modelo de machine learning llamado DECISION TREE, y este es como un diagrama de flujo que almacena datos, y a cada dato etiquetado le hace una pregunta de SI/NO.

```python
# [height, weight, shoe_size]
X = [[181, 80, 44], [177, 70, 43], [160, 60, 38], [154, 54, 37], [166, 65, 40],
     [190, 90, 47], [175, 64, 39],
     [177, 70, 40], [159, 55, 37], [171, 75, 42], [181, 85, 43]]

Y = ['male', 'male', 'female', 'female', 'male', 'male', 'female', 'female',
     'female', 'male', 'male']
```
Aqui vemos que estan las listas de los datos. Donde "X" representa las tres medidas por las cuales vamos a saber si es hombre o mujer. Y "Y" es la variable que almacena una lista de **etiquetas** las cuales serian los generos asociados a la variable anterior por sus medidas.

```python
clf = tree.DecisionTreeClassifier()
clf = clf.fit(X, Y)
```

Ahora la variable **"clf"** sera aquella en la cual guardaremmos o inicializaremos para ser mas precisos nuestro modelo de decision de arbol (**TREE**).Y luego lo entrenaremos con nuestro **dataset** (conjunto de datos), con el metodo **FIT** pasandole nuestras dos variables **X** y **Y**.


```python
prediction = clf.predict([[190, 70, 43]])
print(prediction)
```

Luego de haber entrenado nuestro modelo vamos a pedirle que nos de una prediccion. Mandandole como parametro una lista con las caracteristicas de una persona. Y luego la respuesta la imprimiremos.



## Ahora el reto sera usar el mismo dataset pero con otro modelo de clasificacion de datos y ver que resultado nos da


- Aqui estara el [link del a pagina de scikit-learn](http://scikit-learn.org/stable/auto_examples/classification/plot_classifier_comparison.html): para que se pueda ver la documentacion oficial de los distintos modelos y como se usan.
- El reto sera usar otro modelo y ver el output. Porfavor recuerden esto yo tambien lo quiero recordar xd.
