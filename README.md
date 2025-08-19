# alura_second_proyect
Análisis de Evasión de Clientes (Churn) - Telecom X
Autor: Miguel Angel Camarillo Castañeda
Fecha: 18/08/2025

📌 Descripción del Proyecto
Este proyecto fue desarrollado como parte de mi trabajo final/práctica para el curso de [Nombre del Curso]. El objetivo era analizar los datos de clientes de Telecom X para entender por qué algunos cancelan su servicio (lo que se llama "Churn") y proponer soluciones para reducir esta evasión.

🔍 Contexto del Problema
Telecom X es una compañía de telecomunicaciones que está perdiendo muchos clientes. Mi trabajo consistió en:
Analizar los datos históricos de clientes.
Identificar patrones en los que se van.
Proponer ideas para retenerlos.
Los datos incluyen información como:
Cuánto tiempo llevan los clientes (antigüedad).
Qué tipo de contrato tienen.
Cuánto pagan mensualmente.

💻 Qué Hice
1. Limpieza de Datos
Descargué los datos desde una API en formato JSON.
Arreglé valores faltantes (por ejemplo, en los cargos mensuales).
Convertí respuestas como "Sí/No" a números (1/0) para poder analizarlas.

Código importante:
python
# Rellenar valores vacíos en cargos mensuales
df['Charges.Monthly'] = df['Charges.Monthly'].fillna(df['Charges.Monthly'].median())

2. Análisis Exploratorio
Usé gráficos para entender mejor los datos:
📊 Gráfico de pastel: Mostré que el 26.5% de los clientes abandonan.
📈 Gráficos de caja: Comparé cuánto pagan los clientes que se quedan vs. los que se van.
🛠 Tablas de resumen: Calcularé promedios y medianas para las variables importantes.

3. Hallazgos Principales
Encontré que:
Los clientes nuevos (menos de 1 año) son los que más se van.
Los que tienen contratos mensuales abandonan 3 veces más que los de contratos anuales.
Los que pagan más de $80 al mes tienen mayor riesgo de irse.

📝 Conclusiones
Telecom X podría reducir el Churn si:
✅ Ofrece descuentos a clientes nuevos para que no se vayan.
✅ Incentiva contratos anuales (por ejemplo, regalando un mes gratis).
✅ Mejora el soporte a clientes que pagan mucho pero llevan poco tiempo.

🛠 Cómo Reproducir el Análisis
Clonar el repositorio:
git clone https://github.com/tu-usuario/telecom-churn-analysis.git

Instalar dependencias:
pip install pandas matplotlib seaborn

Ejecutar el notebook:
jupyter notebook notebooks/analysis.ipynb

🙋‍♂️ Dificultades y Aprendizajes
Problema: Al principio no entendía cómo manejar los datos anidados en JSON.
Solución: Aprendí a usar json_normalize() para convertirlos en tabla.
Problema: Los gráficos no se veían bien.
Solución: Descubrí que debía usar sns.set(style="whitegrid").

Lo más valioso que aprendí:
📌 Cómo transformar datos reales para encontrar patrones útiles.
📌 Que visualizar datos hace más fácil explicar los resultados.

¡Gracias por revisar mi proyecto! 😊

Nota: Este proyecto fue desarrollado con fines educativos. Los datos son ficticios o anonimizados.
