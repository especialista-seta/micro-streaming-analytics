Micro streaming analytics

Se trata de implementar una pequeña aplicación con Spring Boot que lea de forma periódica mensajes JSON de una cola RabbitMQ y genere información estadística descriptiva sobre los valores encontrados: media, mediana, moda, desviación típica, cuartiles, valor máximo y valor mínimo.

Los mensajes JSON de la cola de entrada han de tener el formato definido para la ingesta de datos IoT en la API sur de OpenGate. La naturaleza del dato simulado recolectado se deja a elección del programador, pero ha de ser numérico.

El resultado del cálculo estadístico se volcará, en formato JSON a definir por el programador, a una base de datos MongoDB. El documento JSON deberá tener marca de tiempo y los datos estadísticos definidos anteriormente.

Se deberá utilizar Docker y docker-compose para arrancar toda la solución: aplicación Java micro-streaming-analytics, RabbitMQ, MongoDB.