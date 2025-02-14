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





**COHORTES**

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




**MODELO DE REGRESIÓN**

Aplicamos una cohorte de nacimiento para agrupar a los usuarios por el mes de su primera solicitud.
Graficamos el monto acumulado por cada cohorte
![image](https://github.com/user-attachments/assets/37135f92-9c4d-433a-bdb6-f1b97e8f124a)

Observamos que a partir del primer mes, la cantidad de solicitudes baja a la maitad, y va bajando lentamente. 
Incluso las cohortes con mayor monto acumulado siguen esta tendencia.
Observamos que los montos del primer mes de cada cohorte es superior al de la cohorte anterior, lo que quiere decir que está ganando popularidad. 
Los meses en los que se dispara debe ser alguna promoción, puede ser alguna de verano ya que coincide estos meses.

Para crear el modelo, cogimos los datos de la segunda cohorte. Realizamos una bísqueda de hiperparámetros, GridSearch. Graficamos las combinaciones.
![image](https://github.com/user-attachments/assets/0712b17c-eda4-4330-b48b-42c8f01ab4c1)
Podemos ver que diferentes configuraciones del modelo. Observamos que para grado 6 y alpha 1 el acierto en los datos de entrenamiento es casi perfecta y para 
los datos de prueba tiene un puntaje del 80%. Para saber si el modelo es bueno, hacemos la diferencia del coeficiente de determinación y nos da de resultado 0.199.
Un resultado decente.
Aquí observamos la gráfica para el modelo con grado 6 y alpha 1
![image](https://github.com/user-attachments/assets/fd03a18b-54f1-432f-b815-1b1cf4bc6334)
Si ampliamos el ratio de búsqueda observamos que grado 8 con alpha 100 también da resultados interesantes
![image](https://github.com/user-attachments/assets/133ce743-08ab-4f7f-8aa1-347d5e650a04) 
Utilizando el metodo de la Validación cruzada, podemos observar cual es el mejor grado del polinomio para un alpha.
Aquí vemos que para alpha = 0.001 los meodelos mas estables son entre el grado 7 y 10, donde tienen una mediana alta, pocos outliers y varianza moderada.
![image](https://github.com/user-attachments/assets/d3f0c626-359d-43a9-927c-1c592e1c31fa)
Para alpha=1 se observa que los modelos no acaban de funcionar muy bien, tal vez para grado 6 como vimos antes pero está en zona negativa
![image](https://github.com/user-attachments/assets/b9470bc8-f19d-4be2-9b44-9378e7fcdecf)
Para alphas mas grandes como 100, vemos que los modelos no son muy estables. 
![image](https://github.com/user-attachments/assets/4859c642-70ee-4e4b-8695-398b8a28b694)

Pasamos ahora a los modelos de cohortes semanales, monto acumulado.

Primeros modelos (Datos separados en 40%test):
![image](https://github.com/user-attachments/assets/4c50dc66-044a-416e-a957-522a03a623a4)
![image](https://github.com/user-attachments/assets/d4ddb136-2601-48c6-bb4a-98fb26ec9505)
Mejor resultado 
![image](https://github.com/user-attachments/assets/f76e224b-f30d-4a4b-a594-98c940c16f92)

Vemos la distribución para alpha 0.01. 
![image](https://github.com/user-attachments/assets/33e67d84-2a8f-4684-a958-6d33caac1aa7)

Vemos como actua el modelo en la predicción a semanas futuras
![image](https://github.com/user-attachments/assets/5da1f98d-61b2-4f50-acc5-fa6edafc0a55)
Aquí podemos ver la importancia de los coeficientes 
![image](https://github.com/user-attachments/assets/df880636-9c53-488b-b84b-325ada6dbc84)
Y la importancia absoluta de los coeficientes de ridge.
![image](https://github.com/user-attachments/assets/4cf13244-a227-4c17-a47d-c6f27346c309)







