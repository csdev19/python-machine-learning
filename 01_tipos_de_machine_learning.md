# Tipos de Machine Learning

**Machine Learning** (aprendizaje automatico) puede ser clasificado en **3 categorias** basados en las caracteristicas de los datos que son devueltos y la **metodologia de entrenamiento**:

- [Supervised Learning]()
- [Unsupervised Learning]()
- [Reinforcement Learning]()

Vamos a examinar a cada uno en detalle.

## Supervised Learning - Aprendizaje Supervisado

Con **aprendizaje supervisado**, la maquina es entrenada usando un conjunto de datos etiquetados, donde cada elemento esta compuesto por pares de E/S (entrada y salida). La maquina **aprende** la relacion entre la entrada y salida, y la meta es **predecir un comportamiento** o **tomat una decision** basada en los datos suministrados previamente. Por ejemplo, podemos proveer a la maquina con los siguientes datos para conseguir las siguientes respuestas:

- Un grupo de **numeros enteros** (o letras), y luego entrenar para reconocer un numero (o letra) escrita a mano.
- Un grupo de notas musicales, y luego reconocer el nombre y el tono asociado.
- Fotos de animales con sus respectivos nombre, y luego entrenar para identificar al animal que se entregue.
- Una lista de peliculas que una persona ha visto, y luego entrenar para determinar si a esa persona le gustara otra pelicula (si es asi, darle una recomendacion).
- Un numero de correos recibidos en nuestro "inbox", y luego entrenar para distinguir los mensajes de **spam** de los que son legitimos.
- Una lista de habitos de buscadores web, y luego entrenar para proveer sugerencias de busqueda acordes. Una persona cuyas busquedas en la web estan principalmente relacionadas con viajes cuando ingresaria la palabra **entrenar** en un motor de busqueda podria devolver algunos resultados distintos a cuando busca por oportunidades de entrenamiento cuando ingrese la palabra **entrenar** en el motor de busqueda.

En los ejemplos anteriores, ten en cuenta que necesitaremos una etiqueta para los datos antes de enviarlos a la maquina. En el ejemplo de lista de peliculas, vamos a considerar un pequeño grupo de datos con dos solo dos individuos, A y B:

| Individual    | Peliculas vistas                             |
| ------------- |:--------------------------------------------:|
| A             | Harry Potter and the Philosopher's Stone     |
| ------------- |:--------------------------------------------:|
| A             | Harry Potter and the Prisioner of Azkaban    |
| ------------- |:--------------------------------------------:|
| B             | Star Wars: Episode IV – A New Hope           |
| ------------- |:--------------------------------------------:|
| A             | Harry Potter and the Order of the Phoenix    |
| ------------- |:--------------------------------------------:|
| B             | The Empire Strikes Back                      |
| ------------- |:--------------------------------------------:|
| B             | Star Wars: Episode VI – Return of the Jedi   |
| ------------- |:--------------------------------------------:|
| A             | Harry Potter and the Deathly Hallows – Part 1|
| ------------- |:--------------------------------------------:|
| B             | Star Wars: Episode I – The Phantom Menace    |


Basados en los datos anteriores, podemos inferir que el **individuo A** es un fan de Harry Potter (quizas tambien es un fan de las peliculas de fantasia), cuando a **B** le gusta las peliculas de Star Wars (posiblemente la ciencia ficcion tambien). Las respuesta a preguntas como **al individuo A le gustaria** "Harry pother and the chamber of secrets" o "Percy jackson & the Olympians: The Lightning Thief" ? o **podria el individuo B querer ver** “Star Wars: The Force Awakens” or “Star Trek”? son predicciones que esperamos que la maquina pueda hacer. Luego, cuando una nueva pelicula este disponible, nuestro algoritmo podria predecir a cual de los dos individuos o ambos podria gustarle o no.

Como tu probablemente ya te habras dado cuenta, el exito del **aprendizaje supervizado** depende de la calidad y el tamaño del conjunto de entrenamiento. Cuando mas grande y mas preciso es, seran mejores las predicciones y clasificaciones grupales que la maquina podra realizar cuando se le proporcione datos para analizar en el futuro.


## Unsupervised Learning
