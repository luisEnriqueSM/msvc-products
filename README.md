# msvc-products


# Comandos Docker para levantar el contenedor de msvc-products


```bash
# Limpiar, generar Jar file y omitir tests
.\mvnw clean package -DskipTests

# Construir imagen
docker build -t msvc-products:v1 .

# Correr contenedor
docker run -d -P --name msvc-products --network springcloud msvc-products:v1