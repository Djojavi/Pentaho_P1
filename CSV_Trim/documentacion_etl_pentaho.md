# 📊 Documentación de Transformación ETL en Pentaho  
## Limpieza de datos desde CSV mediante operaciones de texto

---

## 🔹 1. Descripción general

La presente transformación tiene como finalidad la **ingesta y limpieza de datos provenientes de un archivo CSV**, aplicando operaciones específicas sobre cadenas de texto para mejorar la calidad de la información.

El enfoque principal se centra en la **normalización del campo `correo`**, eliminando inconsistencias como espacios innecesarios que afectan su validez.

---

## 🔹 2. Estructura del proceso

El flujo de transformación está compuesto por una secuencia lineal de pasos que permiten:

- Leer datos desde un archivo plano
- Aplicar transformaciones de limpieza
- Preparar los datos para su uso posterior

---

## 🖼️ Espacio para imagen – Vista general del flujo  
*(Insertar aquí una captura del canvas de Pentaho mostrando toda la transformación conectada)*

---

## 🔹 3. Fuente de datos

### CSV file input

Este paso se encarga de la **lectura del archivo CSV**, interpretando su estructura y asignando tipos de datos a cada campo.

**Características:**
- Lectura secuencial del archivo
- Separación por delimitador (coma)
- Definición explícita de campos

**Campos utilizados:**
- `nombre` (String)
- `correo` (String)

---

## 🖼️ Espacio para imagen – Configuración de CSV Input  
*(Insertar captura de la configuración del step “CSV file input”)*

---

## 🔹 4. Transformaciones de datos

### 4.1 String Operations (TRIM)

Este paso realiza la **eliminación de espacios en blanco al inicio y al final del campo `correo`**, evitando inconsistencias comunes en datos provenientes de entrada manual o sistemas externos.

**Función principal:**
- Normalización básica de texto

---

## 🖼️ Espacio para imagen – Configuración de String Operations  
*(Insertar captura del step con opción TRIM activada)*

---

### 4.2 Replace in String (REPLACE)

Permite la **sustitución de caracteres dentro de una cadena**, en este caso eliminando espacios internos que afectan la estructura del correo electrónico.

**Función principal:**
- Limpieza interna del texto
- Corrección de formato

---

## 🖼️ Espacio para imagen – Configuración de Replace in String  
*(Insertar captura del step mostrando el reemplazo de espacios)*

---

## 🔹 5. Flujo de ejecución

La transformación sigue un flujo secuencial donde cada paso procesa la salida del anterior:

```
CSV file input
   ↓
String Operations (TRIM)
   ↓
Replace in String (eliminación de espacios)
```

---

## 🖼️ Espacio para imagen – Ejecución del flujo  
*(Insertar captura del preview o ejecución en Pentaho con filas procesadas)*

---

## 🔹 6. Resultado del proceso

Como resultado de las transformaciones aplicadas, los datos presentan:

- Eliminación de espacios innecesarios
- Correos electrónicos correctamente formateados
- Mayor consistencia en el dataset

---

## 🔹 7. Consideraciones

- El orden de las transformaciones es crítico para garantizar resultados correctos  
- El proceso es modular y permite la incorporación de nuevas reglas de limpieza  
- Este tipo de transformación es común en etapas iniciales de procesos ETL  

---

## 🔹 8. Observaciones finales

La limpieza de datos mediante operaciones sobre cadenas es un paso fundamental dentro de cualquier flujo de integración de datos, ya que impacta directamente en la calidad del análisis posterior.

Esta implementación representa una base sólida para la construcción de procesos ETL más complejos.
