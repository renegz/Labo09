1. Permite escribir codigo asincrono por medio de hilos secundarios  de manera secuencial, se diferencia de un hilo tradicional en que podemos controlar cuando la coroutine se suspende y cuando se reanuda.

2. La importancia de suspend es que como puede suspender una coroutine, este no obstruye el hilo principal y asi que no bloquea la interfaz del usuario mientras se realiza la coroutine; Para implementarlo se coloca la palabra "suspend" antes de la declaracion de la funcion.

3. Con dispatcher podemos determinar a la coroutine en que hilo se ejecutará, para escoger uno adecuado depende de la utilidad de la coroutine, segun eso se puede ejecutar en el dispatcher main que es el hilo UI, el dispatcher IO para operaciones Input/Output de red o archivos, default para tareas de computacion intensivas o crear uno personalizado para casos mas especificos.

4. Se utilizan para iniciar una coroutine que produce un resultado asincrono, se diferencia del launch ya que el launch no retorna un resultado y se ejecuta en segundo plano, mientras que async devuelve un objeto Deferred y se obtiene el resultado mediante la funcion await() y permite la ejecucion de multiples tareas asincronas y luego poder combinar los resultados.
