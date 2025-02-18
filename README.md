# **STONKS**

## **Introducción**

Este proyecto tiene como objetivo analizar y extraer insights clave a partir de datos relacionados con tarifas (fees) y solicitudes de adelanto de efectivo (cash requests) dentro de Business Payments, una empresa de servicios financieros. A través de este estudio, se busca comprender mejor el comportamiento de los usuarios, evaluar el impacto de diferentes tipos de tarifas y detectar patrones que puedan ayudar en la toma de decisiones estratégicas.

### Conjuntos de Datos

El análisis se basa en dos conjuntos de datos principales:

**1- Solicitudes de Efectivo (Cash Requests)**

Este conjunto de datos documenta todas las operaciones en las que los usuarios piden adelantos de efectivo, facilitando el estudio de patrones de uso y la identificación de posibles riesgos.

- **Total de registros:** 23,970
- **Cantidad de columnas:** 16

**Columnas destacadas:**
- `id`: Código único de la solicitud.
- `amount`: Importe solicitado.
- `status`: Estado de la solicitud (`approved`, `pending`, `rejected`).
- `user_id`: ID del usuario que realizó la solicitud.
- `reimbursement_date`: Fecha prevista para el reembolso.
- `transfer_type`: Categoría de transferencia.

---

**2- Tarifas (Fees)**

Proporciona detalles sobre las tarifas cobradas a los usuarios por diversos conceptos, como pagos inmediatos, fallos en reembolsos y aplazamientos de pagos.

- **Total de registros:** 21,061
- **Cantidad de columnas:** 13

**Columnas destacadas:**
- `id`: Código único de la tarifa.
- `cash_request_id`: ID de la solicitud de efectivo asociada.
- `type`: Clasificación de la tarifa (`instant_payment`, `split_payment`, `incident`, `postpone`).
- `status`: Estado de la tarifa (`confirmed`, `rejected`, `cancelled`, `accepted`).
- `total_amount`: Importe total.
- `created_at`: Fecha de registro.

---

### **Objetivos**
- Analizar y depurar los datos para asegurar su calidad y coherencia.
- Identificar tendencias de uso y frecuencia de pagos para analizar el comportamiento de los usuarios.
- Implementar análisis de cohortes para estudiar la retención y comportamiento a lo largo del tiempo.
- Desarrollar un modelo de clasificación que anticipe qué usuarios podrían abandonar la plataforma.

### **Herramientas y Tecnologías Usadas**
- **Python:** Procesamiento de datos con `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`.
- **Google Colab:** Ejecución y desarrollo de scripts en la nube.
- **Excel:** Inspección y verificación adicional de datos.


## **EDA Cash request**

![mapa_calor_cash_request](https://github.com/user-attachments/assets/b5fe3792-5714-4c50-acfc-51cc24b010d3)

## **EDA fees**

![mapa_calor_fees](https://github.com/user-attachments/assets/399d231d-be38-47aa-a554-665b2a50f54b)

## **INGENIERIA DE CARACTERISTICAS**

![image](https://github.com/user-attachments/assets/41cefcb4-e537-4b43-98ce-f2c14728a648)

![image](https://github.com/user-attachments/assets/549a4a29-a07f-4ef1-8e20-adb30f45a1a1)

![image](https://github.com/user-attachments/assets/701ac90f-d416-4798-88a4-87c1e2a651ba)

![image](https://github.com/user-attachments/assets/743e008e-e6f2-47cf-8a3c-9d041bf659e7)

![image](https://github.com/user-attachments/assets/eddccfd2-4afe-4737-b4b2-319dd8e094e2)

![image](https://github.com/user-attachments/assets/68ea4fdd-4f25-4202-95f0-38a719cb9e85)

![image](https://github.com/user-attachments/assets/dbf27ee7-07a8-4d06-affe-eb8137255d4a)

![image](https://github.com/user-attachments/assets/4eae388c-9535-4045-a2de-3252acf8ea09)

![image](https://github.com/user-attachments/assets/45be7d40-c85b-49c8-8f6f-593d500feba9)

![image](https://github.com/user-attachments/assets/224f55cd-b7a1-42b6-a0f4-032437ecc702)

![image](https://github.com/user-attachments/assets/bc576e24-e4b6-49af-bcd2-53138e17b244)


### **COHORTES**

Varios Cohortes

Retención clientes

![tasa_retención](https://github.com/user-attachments/assets/750de52f-e7d8-4d7a-a305-bbe4e27d7140)

Abondo clientes

![tasa_abandono](https://github.com/user-attachments/assets/1b6672de-bb2c-4e5a-ad79-4024245bea52)

Retención Solicitudes

![tasa_ret_sol](https://github.com/user-attachments/assets/cb6fcc74-5a30-4d3f-ba56-1e69663631e1)

Abandono Solicitudes

![tasa_abandono_sol](https://github.com/user-attachments/assets/c606d22a-50a1-46af-a85d-4d57769e6586)

Cohorte de top 10 usuarios

Por mes

![top10_users](https://github.com/user-attachments/assets/b2c72370-b26d-4f4a-ba9f-b6990f31a9dc)

Por semana

![Top10_users_w](https://github.com/user-attachments/assets/8d774d84-61c1-4c30-b381-922a7cc2aa6d)


Tasa retención clasficado (bronce,plata,oro) por mes inicial y el amount. Todos los usuarios.

![tasa_bronce](https://github.com/user-attachments/assets/a3231151-cdc8-4e46-a90b-1c8c6a86350e)

![tasa_plata](https://github.com/user-attachments/assets/99b21130-1d5a-4152-80ff-88c05c66cf54)

![tasa_oro](https://github.com/user-attachments/assets/6178af83-104c-48f5-a00b-bb70db420aab)

Mismo cohorte pero el acumulado.

![tasa_acum_bronce](https://github.com/user-attachments/assets/66867ddf-75b8-4dc1-8d35-b60b76e810e7)

![tasa_acum_plata](https://github.com/user-attachments/assets/f4bdb76e-0dba-4903-a648-c29428eea0ea)

![tasa_acum_oro](https://github.com/user-attachments/assets/6305938c-1075-4ca1-95f2-2496c3eb02c2)

Tasa retención clasficado (bronce,plata,oro) por mes inicial y el amount. usuarios activos.

![u_a_bronce](https://github.com/user-attachments/assets/eb94981d-4ea8-4cf6-97f5-6ea6bc3feb11)

![u_a_plata](https://github.com/user-attachments/assets/a0ffa6b9-9a4d-4ad6-b223-d5ff7b9bd13e)

![u_a_oro](https://github.com/user-attachments/assets/f36a57d6-7b82-43d0-978c-aa30e1c4ea1c)

los acumulados de los usuarios activos.

![u_a_acum_bronce](https://github.com/user-attachments/assets/11d4238f-3a39-4b09-ab50-0dd239edc237)

![u_a_acum_plata](https://github.com/user-attachments/assets/bfd569fc-237f-40c3-96df-ca0b36eb4618)

![u_a_acum_oro](https://github.com/user-attachments/assets/e2bb654c-0ac4-45e5-9a5b-7aa259437e50)

Tasa retención clasficado (bronce,plata,oro) por mes inicial y el amount. usuarios eliminados.

![u_d_bronce](https://github.com/user-attachments/assets/b6bd6209-b156-4ef4-93c4-6995e6698953)

![u_d_plata](https://github.com/user-attachments/assets/acb1d29e-3481-438b-9d6c-7c94ad31d3e1)

los acumulados de los usuarios elimindaos.

![u_d_acum_bronce](https://github.com/user-attachments/assets/f0ba6791-2986-4670-aeb9-86677f978c13)

![u_d_acum_plata](https://github.com/user-attachments/assets/5a1c9188-d2fb-494b-a526-b5dae46d451b)




## **MODELO DE REGRESIÓN**

Aplicamos una cohorte de nacimiento para agrupar a los usuarios por el mes de su primera solicitud.
Graficamos el monto acumulado por cada cohorte
![image](https://github.com/user-attachments/assets/37135f92-9c4d-433a-bdb6-f1b97e8f124a)

Observamos que a partir del primer mes, la cantidad de solicitudes baja a la maitad, y va bajando lentamente. 
Incluso las cohortes con mayor monto acumulado siguen esta tendencia.
Observamos que los montos del primer mes de cada cohorte es superior al de la cohorte anterior, lo que quiere decir que está ganando popularidad. 
Los meses en los que se dispara debe ser alguna promoción, puede ser alguna de verano ya que coincide estos meses.

Para crear el modelo, cogimos los datos de la segunda cohorte. Realizamos una búsqueda de hiperparámetros. Graficamos las combinaciones.

![image](https://github.com/user-attachments/assets/15cfa6fb-0b78-4430-b285-ee6f4647b846)
![image](https://github.com/user-attachments/assets/d72596cf-08a0-4f14-81cb-67517f5ab31e)


Podemos ver que diferentes configuraciones del modelo. Observamos que para grado 8 y alpha 100 el acierto en los datos de entrenamiento es casi perfecta y para 
los datos de prueba tiene un puntaje del 95%. Para saber si el modelo es bueno, hacemos la diferencia del coeficiente de determinación.
Aquí observamos la gráfica para el modelo con grado 8 y alpha 100

![image](https://github.com/user-attachments/assets/149fb660-727a-496c-9e81-dbd58d13cad4)
![image](https://github.com/user-attachments/assets/e945e5e8-a4cd-4130-883f-47037ac40b9a)


Utilizando el metodo de la Validación cruzada, podemos observar cual es el mejor grado del polinomio para un alpha.
Siendo alpha 100 el mejor resultado, aplicamos validación cruzada para ver el comportamiento de los diferentes grados del polinomio.

![image](https://github.com/user-attachments/assets/2bc50627-fffd-4114-8510-3819a06ed18d)


Como vemos la diferencia del polinomio es practicamente 0 y la R^2 de interpolación es practicamente 1, lo que signfica que para interpolación va muy bien, pero
para extrapolación no es muy útil ya que tiene sobreajuste.

Observamos que para predecir no son muy buenos.

![image](https://github.com/user-attachments/assets/9551d293-6bf1-4591-b5cd-579d072185c2)



Observamos la importancia de los coeficientes.

![image](https://github.com/user-attachments/assets/10b8ff0a-664f-46c3-b31e-65b2cb0a95eb)

En absolutos

![image](https://github.com/user-attachments/assets/8c7abee0-c450-42c0-ab36-699d016ebdf7)

Hacemos una búsqueda para alpha 1, ya que es el segundo mejor alpha que se encuentra haciendo la búsqueda de parámetros

![image](https://github.com/user-attachments/assets/066772ab-b64e-4daa-a9c7-d9febdffc697)


Pero para predecir continuamos obteniendo valores negativos.

![image](https://github.com/user-attachments/assets/df37b178-05ac-4945-bad0-3f7f1c477e6e)


**Modelo de interpolación cohorte semanales**

Buscamos los mejores parámetros (Datos separados en 20%test):

![image](https://github.com/user-attachments/assets/3648ff59-f9b8-43bd-a94f-edfad6f976c9)

![image](https://github.com/user-attachments/assets/a0ed2bf4-ff9d-4b8e-9e82-b45397772ed5)


Nos indica que el mejor resutlado es 3 con alpha 100:

![image](https://github.com/user-attachments/assets/b5b0b248-16b5-4216-9ef4-3807d854c00b)
![image](https://github.com/user-attachments/assets/2eaec5f9-d19a-455a-88d3-39ff4362a81f)


Observamos la estabilidad del modelo para diferentes grados del polinomio con validación cruzada.

![image](https://github.com/user-attachments/assets/3ec7fc52-8b3e-4428-8c3e-5dca3c259999)

Importancia de los coeficientes

![image](https://github.com/user-attachments/assets/07d29c6e-dac1-4f4d-9171-447181fd5d11)



## CLASIFICADORES

A partir de los usuarios activos clasificados por rango, generamos los modelos clasificadores.


### Árbol de decisión

Asignamos a las variables las caracterísitcas de entraada y los valores a clasificar

![image](https://github.com/user-attachments/assets/616271fc-96a2-40f9-9b0b-5c4749b19939)

Y generamos el modelo:
![image](https://github.com/user-attachments/assets/0d3ad31d-7e3d-47e1-bcd7-3bcd221cce1e)

Métricas

![image](https://github.com/user-attachments/assets/8b13291b-ad5c-4302-be26-ef21c8064c4b)

"Curva" AUROC

![image](https://github.com/user-attachments/assets/af838961-131b-48e9-ab70-7008f2f98158)

"Curvas" de aprendizaje

![image](https://github.com/user-attachments/assets/a839116f-c8d8-45b1-a048-054521d3b5ff)

Se observa que el maximo de número de datos conjuntos necesarios han sido 5000.



### KNN

Buscamos el mejor numero de vecinos para el modelo KNN:

![image](https://github.com/user-attachments/assets/70f79919-1d68-490b-a202-f55438e73b2c)


Observamos las metricas y vemos que son practicamente perfectas.

![image](https://github.com/user-attachments/assets/7f9482e8-b9ac-4b5a-83e0-53bf79ce3daf)


Comparación de modelos

![image](https://github.com/user-attachments/assets/53a41672-e5c0-4b66-80b7-faca6c3b3ac3)




