# Audi-RS

Página Web para Visualizar Coches [Audi RS](https://www.audi.nl/nl/r-rs/rs-modellen/)

Una aplicación diseñada para los entusiastas de los coches Audi RS. Este sistema permite explorar diferentes modelos, ver detalles y obtener información relevante de cada vehículo.

![rs6](https://github.com/user-attachments/assets/ba26a378-5d50-48ea-b36e-4c9756839456)

### Tabla de Datos Modelos Principales

|Modelo    | Año | Potencia | Precio |
|----------|-----|-------|-----------|
|Audi RS3  | 2023| 400cv | $60,000 |
|Audi RS5  | 2022| 450cv | $75,000 |
|Audi RS7  | 2023| 600cv | $120,000 |

## Funcionalidades Principales

- **Exploración de Modelos**:
  - Visualizar una lista completa de modelos Audi RS.
  - Filtrar por año, potencia, o precio.
- **Información Detallada**:
  - Mostrar especificaciones técnicas, imágenes y precios de cada coche.
- **Interfaz Intuitiva**:
  - Diseño moderno y responsivo para una experiencia de usuario óptima.

## Tecnologías Utilizadas

 - PHP
  
 - MySQL
  
 - HTML y CSS
  
 - JavaScript

### Ejemplo de Código en PHP

```
<?php

$conn = new mysqli("localhost", "usuario", "contraseña", "audi_rs_db");
if ($conn->connect_error) {
    die("Conexión fallida: " . $conn->connect_error);
}

$sql = "SELECT * FROM coches";
$result = $conn->query($sql);

if ($result->num_rows > 0) {
    while($row = $result->fetch_assoc()) {
        echo "<h3>" . $row["modelo"] . "</h3><p>Precio: $" . $row["precio"] . "</p>";
    }
} else {
    echo "No se encontraron coches.";
}
$conn->close();
?>
```
Con este proyecto, esperamos ofrecer una herramienta completa para los amantes de los coches Audi RS.
