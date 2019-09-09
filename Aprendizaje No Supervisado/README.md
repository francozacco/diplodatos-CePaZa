# Practicos de no supervisado.

## Relgas de asociación.

### ¿Como correr la notebook?.
Descargar del sitio https://grouplens.org/datasets/movielens/ el archivo ml-20m.zip. Descomprimirlo y quedarse con los archivos movies.csv y ratings.csv y colocarlos en el mismo directorio que el jupyter-notebook.

Luego corrarer el notebook con jupyter.

### Conclusión.

Nos quedamos con reglas donde el Lift sea mayor a 2.

Seleccionamos Lift como metrica ya que nos ayuda a descartar casos en que la confianza no nos aporta información, 
por ejemplo en casos tales como: conf({Jurassic Park}=>{Star Wars V}) = 0.8 y prob({Star Wars V}) = 0.8. 
Es decir, que se haya visto la pelicula {Star Wars} no esta condicionado de forma alguna con que sepamos que se haya visto la pelicula {Jurassic Park}.

El Lift también tiene una interpretación probabilística. 
Si el Lift es 1, significa que la confianza de la regla es igual al soporte de "{Star Wars}"; en otras palabras significa que "{Jurassic Park}" y "{Star Wars}" son eventos independientes.
  * Debemos recordar que el soporte es la frecuencia relativa del item set.
  * La confianza es la probabilidad empírica de que ocurra el consecuente, dado que ocurrió el antecedente en la regla.
  * Y el Lift refleja el aumento de la probabilidad de que ocurra el consecuente, cuando nos enteramos de que ocurrió el antecedente.
