# Conversor de Moneda

## Descripción

El **Conversor de Divisas** es una herramienta desarrollada en Java que permite a los usuarios transformar valores entre diferentes monedas utilizando tasas de cambio actualizadas en tiempo real desde una API externa. Está diseñado para ser accesible y práctico, permitiendo el uso de nombres o códigos ISO 4217 para seleccionar las monedas.

## Características

- **Transformación de divisas**: Realiza conversiones de montos basándose en tasas de cambio actualizadas dinámicamente.
- **Compatibilidad con nombres y códigos**: Permite identificar monedas mediante su nombre común o su código ISO.
- **Validación de datos ingresados**: Asegura que las monedas seleccionadas sean válidas y estén disponibles.
- **Actualización en tiempo real**: Conecta con una API externa para garantizar datos actualizados.

## Requisitos

Para ejecutar este proyecto, asegúrate de contar con lo siguiente:

- **Java**: Versión 8 o superior.
- **Dependencias**:
  - [Gson](https://github.com/google/gson): Biblioteca para procesar datos JSON.
- **Conexión a Internet**: Es necesaria para realizar las consultas a la API.

## Instalación

1. Clona el repositorio o descarga los archivos del proyecto:

   ```bash
   git clone https://github.com/Miguel-Ghost/Conversor-de-Monedas.git
2. Asegúrate de que las dependencias estén disponibles en tu proyecto. Si usas un administrador de dependencias como Maven, incluye `Gson` en tu archivo `pom.xml`:

   ```xml
   <dependency>
       <groupId>com.google.code.gson</groupId>
       <artifactId>gson</artifactId>
       <version>2.10.1</version>
   </dependency>
   ```

3. Compila y ejecuta el proyecto con tu entorno de desarrollo favorito o desde la terminal:

   ```bash
   javac Main.java
   java Main
   ```

## Uso

1. Al ejecutar la aplicación, selecciona la opción **Convertir moneda**.
2. Ingresa el nombre o código de la **moneda base** (ejemplo: `USD` o `Dólar estadounidense`).
3. Ingresa el nombre o código de la **moneda destino** (ejemplo: `EUR` o `Euro`).
4. Introduce el monto a convertir.
5. La aplicación mostrará el resultado de la conversión.

## Ejemplo de Ejecución

Moneda origen: USD  
Moneda destino: EUR  
Monto: 150  
Resultado: 138.45 EUR  



## API Utilizada

La API UTILIZADA ES [Exchange Rate API](https://www.exchangerate-api.com/) para obtener las tasas de cambio actualizadas.

## Estructura del Proyecto

- `Main.java`: Clase principal que gestiona el flujo del programa y la interacción con el usuario.
- `ApiCliente.java`: Clase que se conecta a la API y maneja las solicitudes HTTP.
- `TipoCambio.java`: Clase modelo para mapear los datos de respuesta de la API.
- `NombreMoneda.java`: Clase que almacena y maneja una lista de monedas soportadas.
