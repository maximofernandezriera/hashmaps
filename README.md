# ¿Qué es un Hashmap?

## Una aproximación

Imaginad un diccionario inglés-español. Queremos saber qué significa la palabra “fee”. Sabemos que en el diccionario hay muchas entradas y en cada entrada tenemos una palabra en inglés y su correspondiente traducción al español. Buscando por la “f” encontramos que “fee ” significa “tarifa”.

* Un diccionario en Java funciona de un modo similar. 

Contiene una serie de elementos que son las entradas que a su vez están formadas por un par (clave, valor). La clave (key) permite acceder al valor.  

En el ejemplo anterior, la clave sería “fee” y el valor “tarifa”.

* No puede haber claves duplicadas.

## Definición:
Un Hashmap en Java es una estructura de datos que implementa la interfaz Map. Almacena datos en pares clave-valor, donde cada clave es única, y cada clave se asocia exactamente con un valor. En lenguajes como python son llamados diccionarios o mapas.

# Operaciones básicas con Hashmaps

1. **Inserción (`put`)**: Agrega un par clave-valor al mapa. Si la clave ya existe, su valor se actualiza con el nuevo valor proporcionado.

   Ejemplo en Java:
   ```java
   HashMap<String, Integer> map = new HashMap<>();
   map.put("manzana", 5); // Agrega la clave 'manzana' con el valor 5
   map.put("naranja", 3); // Agrega la clave 'naranja' con el valor 3
   ```

2. **Búsqueda (`get`)**: Recupera el valor asociado con una clave específica. Si la clave no existe en el mapa, retorna `null`.

   Ejemplo en Java:
   ```java
   Integer valor = map.get("manzana"); // Devuelve 5
   ```

3. **Eliminación (`remove`)**: Elimina el par clave-valor asociado con una clave específica. Retorna el valor que estaba asociado con la clave, o `null` si la clave no existía.

   Ejemplo en Java:
   ```java
   map.remove("naranja"); // Elimina la clave 'naranja' y su valor asociado
   ```

4. **Contiene la clave (`containsKey`)**: Verifica si el mapa contiene una clave específica. Retorna `true` si la clave existe, de lo contrario `false`.

   Ejemplo en Java:
   ```java
   boolean contiene = map.containsKey("manzana"); // Devuelve true
   ```

5. **Contieneel valor (`containsValue`)**: Verifica si el mapa contiene un valor específico. Retorna `true` si al menos una clave está asociada con ese valor, de lo contrario `false`.

   Ejemplo en Java:
   ```java
   boolean contieneValor = map.containsValue(5); // Devuelve true
   ```

6. **Tamaño (`size`)**: Retorna el número de pares clave-valor en el mapa.

   Ejemplo en Java:
   ```java
   int tamaño = map.size(); // Devuelve el número de pares clave-valor en el mapa
   ```

7. **Iteración**: Los Hashmaps se pueden iterar para procesar cada par clave-valor. Esto se puede hacer a través de las claves, los valores, o ambos.

   Ejemplo en Java:
   ```java
   for (Map.Entry<String, Integer> entrada : map.entrySet()) {
       System.out.println("Clave: " + entrada.getKey() + ", Valor: " + entrada.getValue());
   }
   ```
