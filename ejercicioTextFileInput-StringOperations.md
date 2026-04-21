# Text file input - String operations - Excel Output    
*Autor:* Nayeli Leiva
## Descripción 
Esta transformación lee un archivo .txt con datos de clientes que se encuentran desordenados, ya sea con desorden en los caracteres, espacios sobrantes, con la tranformación los limpia y normaliza usando String Operations y lo exporta en un archivo Excel.

<img width="921" height="868" alt="Image" src="https://github.com/user-attachments/assets/f20ecf40-dd97-4ebf-9746-702fef7905ac" />

## Paso 1: Cargar Datos

Lectura del archivo de texto plano con Datos de los clientes guardados en un .txt, en este caso se elige el formato CSV file input, por que a pesar de ser texto plano, este se encuentra delimitado por ;

<img width="884" height="552" alt="Image" src="https://github.com/user-attachments/assets/06b93b93-7a8c-4b54-a45e-a46d1236cde4" />

## Paso 2: String Operation

En este paso se realiza la limpieza y normalización de cada campo de texto, por ejemplo en el campo *trim type* se elige both para eliminar los espacios al inicio y final de cada valor, con *Upper and lower case* convierte el texto a minúsculas o mayúsculas respectivamente.
<img width="921" height="252" alt="Image" src="https://github.com/user-attachments/assets/8fcf1af1-5444-47b6-b563-bde89bf70072" />


## Paso 3: Output

Aquí se realiza la exportación del reaultado a un archivo .xlsx, se agregaron las columnas del archivo original y después de la limpieza de datos para observar la diferencia.

<img width="921" height="252" alt="Image" src="https://github.com/user-attachments/assets/92be927d-d240-4f2a-b6be-7579c7f2f3c0" />

<img width="921" height="678" alt="Image" src="https://github.com/user-attachments/assets/6144e7fe-574c-4426-9bd0-2faafb18c5b2" />

## Paso 4: Resultado

Y finalmente obtenemos el resultado al aplicar la transformación

<img width="883" height="473" alt="Image" src="https://github.com/user-attachments/assets/d95d82e6-3136-4b32-95d2-50bc734464b5" />

<img width="921" height="376" alt="Image" src="https://github.com/user-attachments/assets/0afd75d4-84dc-4822-82fd-640a8cbbe49d" />