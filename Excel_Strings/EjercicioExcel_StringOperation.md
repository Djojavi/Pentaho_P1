## Descripción

Esta transformación lee un archivo **Excel (.xlsx)** con datos de clientes que se encuentran desordenados, por ejemplo con espacios sobrantes y uso incorrecto de mayúsculas y minúsculas.  
Mediante la transformación **String Operations**, los datos se limpian y normalizan, generando un nuevo campo con el nombre corregido.  
Finalmente, el resultado se exporta a un nuevo archivo **Excel** para comparar el valor original con el valor transformado.

<img width="1464" height="666" alt="Screenshot 2026-04-21 142307" src="https://github.com/user-attachments/assets/d9ed7119-5975-4e72-89a7-2174d87a20e8" />

## Paso 1: Cargar datos

En este paso se realiza la lectura del archivo de entrada en formato **Excel (.xlsx)** mediante el componente **Microsoft Excel Input**.  
Aquí se selecciona el archivo, la hoja correspondiente y el campo que contiene los datos a procesar.  
En este caso, el campo utilizado fue **`cliente_raw`**, que contiene nombres con errores de formato.

<img width="1079" height="627" alt="Screenshot 2026-04-21 083847" src="https://github.com/user-attachments/assets/e59aaae3-4b07-4e82-bb4c-93ba744f0d11" />

## Paso 2: String Operations

En este paso se realiza la limpieza y normalización del campo de texto.  
Se tomó como entrada el campo **`cliente_raw`** y se generó un nuevo campo llamado **`cliente_limpio`**.

La configuración aplicada fue:

- **Trim type = both**: elimina los espacios al inicio y al final
- **Lower/Upper = none**: no convierte todo el texto completamente
- **InitCap = yes**: coloca la primera letra de cada palabra en mayúscula

De esta forma, un valor como:

`"   jUAN pErez   "`  

se transforma en:

`"Juan Perez"`

<img width="1267" height="441" alt="Screenshot 2026-04-21 095647" src="https://github.com/user-attachments/assets/60a8f066-5cdf-4821-a583-e338a5fa176e" />

## Paso 3: Output

Aquí se realiza la exportación del resultado a un archivo **.xlsx** utilizando el componente **Microsoft Excel Writer**.  
Se incluyen tanto el campo original **`cliente_raw`** como el nuevo campo **`cliente_limpio`**, para poder observar la diferencia entre el dato antes y después de la transformación.

<img width="920" height="784" alt="Screenshot 2026-04-21 142143" src="https://github.com/user-attachments/assets/cab1e201-a5b8-4a7f-84f6-5042b31b3c46" />
<img width="1013" height="837" alt="Screenshot 2026-04-21 142252" src="https://github.com/user-attachments/assets/ae941287-40a8-4f71-b9bd-0c35e034bfdf" />


## Paso 4: Resultado

Finalmente, se obtiene un archivo Excel con los datos transformados.  
En este resultado se puede verificar que los nombres fueron limpiados correctamente, eliminando espacios sobrantes y normalizando su formato de escritura.

Ejemplo:

- **cliente_raw:** `"   jUAN pErez   "`
- **cliente_limpio:** `"Juan Perez"`

<img width="1225" height="525" alt="Screenshot 2026-04-21 142331" src="https://github.com/user-attachments/assets/631e1024-7a6e-4c7c-89de-32a55407539d" />
