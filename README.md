# stonks
**EDA Cash request**

![mapa_calor_cash_request](https://github.com/user-attachments/assets/b5fe3792-5714-4c50-acfc-51cc24b010d3)
![image](https://github.com/user-attachments/assets/448e3a73-8879-4316-b4f9-a04e2a3d7ec8)
![desc_cr_1](https://github.com/user-attachments/assets/2e700fa0-8297-4995-89fb-67a10ef72fc3)
![desc_cr_2](https://github.com/user-attachments/assets/948f3bc6-1aab-4942-b879-f20142ba7cab)
![desc_cr_3](https://github.com/user-attachments/assets/4c944197-a9f9-4cf2-b2f0-d39fa386c563)
![desc_cr_4](https://github.com/user-attachments/assets/e88b7362-fd17-40b2-993e-abdab0544706)


**EDA fees**

![mapa_calor_fees](https://github.com/user-attachments/assets/399d231d-be38-47aa-a554-665b2a50f54b)
![Captura de pantalla 2025-02-14 131358](https://github.com/user-attachments/assets/1efed4c5-9626-43bd-8080-df7e6067a2ee)
![desc_fee_1](https://github.com/user-attachments/assets/00a28b96-0f97-4da6-b681-18ce608f6c08)
![desc_fee_2](https://github.com/user-attachments/assets/f83c6bf7-eac6-44a9-af2d-b78bf3ff0a3e)
![desc_fee_3](https://github.com/user-attachments/assets/739ad5b6-dcc0-4cae-8b78-21115deaa780)

**INGENIERIA DE CARACTERISTICAS**











**MODELO DE REGRESIÓN**

Aplicamos una cohorte de nacimiento para agrupar a los usuarios por el mes de su primera solicitud.
Graficamos el monto acumulado por cada cohorte
![image](https://github.com/user-attachments/assets/37135f92-9c4d-433a-bdb6-f1b97e8f124a)

Observamos que a partir del primer mes, la cantidad de solicitudes baja a la maitad, y va bajando lentamente. 
Incluso las cohortes con mayor monto acumulado siguen esta tendencia.
Observamos que los montos del primer mes de cada cohorte es superior al de la cohorte anterior, lo que quiere decir que está ganando popularidad. 
Los meses en los que se dispara debe ser alguna promoción, puede ser alguna de verano ya que coincide estos meses.

Para crear el modelo, cogimos los datos de la segunda cohorte. Realizamos una bísqueda de hiperparámetros
![image](https://github.com/user-attachments/assets/0712b17c-eda4-4330-b48b-42c8f01ab4c1)
Podemos ver que diferentes configuraciones del modelo. Observamos que para grado 6 y alpha 1 el acierto en los datos de entrenamiento es casi perfecta y para 
los datos de prueba tiene un puntaje del 80%. Para saber si el modelo es bueno, hacemos la diferencia del coeficiente de determinación y nos da de resultado 0.199.
Un resultado decente. MAÑANA HACER BOXPLOT PARA ESE MODELO
