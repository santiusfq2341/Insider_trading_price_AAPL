Objetivo general: 

Determinar el impacto de las transacciones de compra y venta de acciones 
realizadas por CEO, miembros de la junta directiva, directores ejecutivos y 
empleados de las compañías que cotizan en la bolsa de valores de Nueva York en el 
precio de las acciones de APPLE desde el año 2015 hasta la fecha de elaboración 
del presente proyecto (27 de marzo 2025). 
1.2 Contexto  
El sentimiento del mercado de valores de Nueva York - Estados Unidos, se refleja en 
índices como el S&P 500 y el DOWJ 30. A lo largo de los años, estos índices han 
sido influenciados por eventos como guerras, situaciones políticas, avances 
tecnológicos, cambio climático, en otras palabras, situaciones externas. Sin 
embargo, un factor a considerar dentro del comportamiento de las acciones es el 
“insider trading”. 
El insider trading se refiere a las transacciones de compra o venta de acciones 
realizadas por altos ejecutivos y empleados de las compañías que cotizan en el 
mercado bursátil. Estas personas tienen la ventaja de acceder a información antes 
de que se haga pública, lo que les permitiría obtener ganancias. 
La SEC (Securities and Exchange Commission) regula el mercado bursátil en 
Estados Unidos y penaliza estas prácticas, asegurando la transparencia y equidad 
en el mercado bursátil. Este ente regulador dicta que por cada compra o venta de 
acciones por parte de los empleados de esa compañía se deben llenar los 
formularios Form 4 o Form 144; esto depende de la forma en la que se negocien las 
acciones. 
1.3 Valor añadido 
En este sentido, he optado por este tema porque no he encontrado estudios que 
correlacionen el insider trading con el precio de las acciones. Con el desarrollo de 
este proyecto, quiero crear una especie de alerta ante los movimientos de acciones 
por parte de los directivos y considerar ese indicador para futuras compras o ventas 
de acciones de mi portafolio. 
2. DATA UNDERSTANDING 
2.1 Fuente de información 
La información viene de 2 fuentes: 
• API de Yahoo Finance: Vale mencionar que no es una API oficial de Yahoo 
Finance, ya que la compañía antes mencionada descontinuó su API en 2017. Llegué 
a esta API por medio de github y la persona que lo publica es un desarrollador 
bastante reconocido y posee calificaciones positivas por lo que decido usar este 
recurso.1 Con esta API se extraen los precios históricos de las acciones del mercado 
bursátil de Estados Unidos. Su frecuencia de actualización es diaria. 
• OpenInsider.com2: esta página recopila todos los formularios llenados por los altos 
ejecutivos de compañías que cotizan en bolsa de valores, extraído de la página de la 
SEC y los consolida en una tabla con un formato tabular (archivo plano). Su 
frecuencia de actualización es diaria. 
2.2 Breve explicación de variables 
Las variables que serán clave al momento de desarrollar mi tema son las siguientes: 
Precios de cotización de acciones extraído con API de Yahoo Finance: 
• Date: fecha que tuvo lugar esa cotización de la acción. 
• Open: es el precio al momento de que el mercado haya comenzado a operar a las 
9:30 AM – Hora Estados Unidos. 
• Close: precio al cierre del día de operaciones, culmina a las 16:00 – Hora Estados 
Unidos. 
• High: es el valor máximo que alcanzó esa cotización en ese día 
• Low: es el valor mínimo que alcanzó esa cotización en ese día 
Datos extraídos de OpenInsider.com 
• Filling date: es la fecha de presentación del formulario ante la SEC 
• Trade date: fecha en la que se realizó la negociación de las acciones 
• Insider name: nombre de la persona que trabaja dentro de la compañía que cotiza 
en bolsa de valores 
• Title: Cargo que ocupa 
• Trade type: la forma en la que se negoció esa transacción, como por ejemplo: sale, 
sale + oe, purchase, entre otras.  
• Price: precio al que se negoció esa acción 
• Qty: cantidad de acciones que se negoció 
• Owned: cantidad de acciones que posee esa persona luego de realizar la 
transacción 
• Delta owned: porcentaje de variación con relación a las acciones que posee esa 
persona después de la transacción. 

1Enlace del API de Yahoo Finance: https://github.com/ranaroussi/yfinance 
2Enlace de OpenInsider.com: http://openinsider.com/ 
