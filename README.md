# cardiovascular-risk-prediction-datarobot
Aplicación web desarrollada en Python y Streamlit que permite estimar el riesgo de enfermedad cardiovascular mediante un modelo de Machine Learning desplegado en DataRobot.
# **🫀 Predicción de Riesgo Cardiovascular con DataRobot**

Aplicación web desarrollada en **Python** y **Streamlit** que permite estimar el riesgo de enfermedad cardiovascular utilizando un modelo de **Machine Learning desplegado en DataRobot**.

🫀 Cardiovascular Risk Prediction with DataRobot

Aplicación web desarrollada en Python y Streamlit que permite estimar el riesgo de enfermedad cardiovascular mediante un modelo de Machine Learning desplegado en DataRobot.

El sistema captura variables clínicas del paciente, calcula automáticamente el Índice de Masa Corporal (IMC) y genera una predicción en tiempo real del riesgo cardiovascular.

📋 Tabla de Contenido
📖 Descripción
🏗️ Arquitectura
🔄 Flujo de Predicción
✨ Características
🚀 Tecnologías
📁 Estructura del Proyecto
⚙️ Instalación
🔐 Configuración
▶️ Ejecución
📊 Variables del Modelo
📈 Resultados
🔮 Futuras Mejoras
👩‍💻 Autor
📖 Descripción

La aplicación permite ingresar datos clínicos de un paciente, calcular automáticamente indicadores como el IMC y enviar la información a un modelo de DataRobot para obtener una predicción del riesgo cardiovascular.

Variables analizadas:

Edad
Género
Estatura
Peso
IMC
Presión sistólica
Presión diastólica
Colesterol
Glucosa
Consumo de tabaco
Consumo de alcohol
Actividad física
🏗️ Arquitectura
🧠 Diagrama de Arquitectura

📌 (Recomendado: usar imagen exportada)

![Arquitectura del sistema](docs/diagrams/arquitectura.png)
🧩 Versión alternativa (Mermaid GitHub)
flowchart LR
    U[Usuario] --> A[Streamlit UI - app.py]
    A --> C[CSV Temporal]
    A --> P[predict.py]
    P --> D[DataRobot Deployment]
    D --> P
    P --> A
    A --> U
🔄 Flujo de Predicción
📌 Diagrama del proceso
![Flujo de predicción](docs/diagrams/flujo.png)
🧩 Versión Mermaid (recomendada para GitHub)
flowchart TD
    A[Capturar datos clínicos]
    B[Calcular IMC]
    C{Datos válidos?}
    D[Crear CSV temporal]
    E[Enviar a DataRobot]
    F[Obtener resultado]
    G[Mostrar probabilidad y clasificación]
    H[Mostrar error]

    A --> B --> C
    C -->|Sí| D --> E --> F --> G
    C -->|No| H
✨ Características
✅ Interfaz amigable con Streamlit
🧮 Cálculo automático de IMC
🔎 Validación de datos clínicos
🤖 Integración con DataRobot API
⚡ Predicción en tiempo real
📊 Visualización de probabilidad de riesgo
🧹 Manejo de archivos temporales
🧱 Arquitectura desacoplada
🚀 Tecnologías
🐍 Lenguaje principal
Python
🎈 Desarrollo web
Streamlit
📊 Procesamiento de datos
Pandas
🤖 Inteligencia Artificial
DataRobot
Machine Learning
📄 Formato de datos
CSV
📁 Estructura del Proyecto
cardiovascular-risk-app/
│
├── app.py
├── predict.py
├── requirements.txt
├── README.md
│
└── .streamlit/
    └── secrets.toml
⚙️ Instalación
1️⃣ Clonar repositorio
git clone https://github.com/usuario/cardiovascular-risk-app.git
cd cardiovascular-risk-app
2️⃣ Crear entorno virtual
python -m venv venv

Activar:

Windows:

venv\Scripts\activate

Mac/Linux:

source venv/bin/activate
3️⃣ Instalar dependencias
pip install -r requirements.txt
🔐 Configuración

Crear archivo:

.streamlit/secrets.toml

Contenido:

DATAROBOT_API_KEY="TU_API_KEY"
DATAROBOT_DEPLOYMENT_ID="TU_DEPLOYMENT_ID"
DATAROBOT_HOST="https://app.datarobot.com"
▶️ Ejecución
streamlit run app.py
📊 Variables del Modelo
Variable	Tipo
genero	Numérica
edad_anios	Numérica
estatura_cm	Numérica
peso_kg	Numérica
indice_masa_corporal	Numérica
presion_sistolica	Numérica
presion_diastolica	Numérica
colesterol	Categórica
glucosa	Categórica
fuma	Binaria
consume_alcohol	Binaria
actividad_fisica	Binaria
📈 Resultados

La aplicación retorna:

📊 Probabilidad de riesgo cardiovascular
🧠 Clasificación (alto / bajo riesgo)
📄 Respuesta del modelo DataRobot
Ejemplo:
Probabilidad: 84.35%
Resultado: Alto riesgo cardiovascular
🔮 Futuras Mejoras
📊 Dashboard analítico avanzado
🧾 Historial de pacientes
🗄️ Integración con base de datos
🔐 Autenticación de usuarios
🐳 Dockerización del proyecto
☁️ Despliegue en la nube
🧠 Explainable AI (XAI)
🌐 DataRobot

🔗 https://app.datarobot.com/homepage/main

👩‍💻 Autor

Lilliana Uribe
Proyecto académico enfocado en Machine Learning, Analítica Predictiva y despliegue de modelos con DataRobot y Streamlit.

🚀 Si quieres siguiente nivel

Puedo ayudarte a convertir esto en:

README tipo empresa (IBM / Google style)
versión con banner + logo + portada visual
README optimizado para portafolio LinkedIn
o repositorio listo para entrevista técnica

Solo dime 👍

crea el documento para descargar .md
Analizado
# Create README.md file content

content = """# 🫀 Cardiovascular Risk Prediction with DataRobot

Aplicación web desarrollada en **Python y Streamlit** que permite estimar el riesgo de enfermedad cardiovascular mediante un modelo de **Machine Learning desplegado en DataRobot**.

El sistema captura variables clínicas del paciente, calcula automáticamente el **Índice de Masa Corporal (IMC)** y genera una predicción en tiempo real del riesgo cardiovascular.

---

# 📋 Tabla de Contenido

- 📖 Descripción
- 🏗️ Arquitectura
- 🔄 Flujo de Predicción
- ✨ Características
- 🚀 Tecnologías
- 📁 Estructura del Proyecto
- ⚙️ Instalación
- 🔐 Configuración
- ▶️ Ejecución
- 📊 Variables del Modelo
- 📈 Resultados
- 🔮 Futuras Mejoras
- 👩‍💻 Autor

---

# 📖 Descripción

La aplicación permite ingresar datos clínicos de un paciente, calcular automáticamente indicadores como el IMC y enviar la información a un modelo de DataRobot para obtener una predicción del riesgo cardiovascular.

Variables analizadas:
- Edad
- Género
- Estatura
- Peso
- IMC
- Presión sistólica
- Presión diastólica
- Colesterol
- Glucosa
- Consumo de tabaco
- Consumo de alcohol
- Actividad física

---

# 🏗️ Arquitectura

## 🧠 Diagrama de Arquitectura

```mermaid
flowchart LR
    U[Usuario] --> A[Streamlit UI - app.py]
    A --> C[CSV Temporal]
    A --> P[predict.py]
    P --> D[DataRobot Deployment]
    D --> P
    P --> A
    A --> U
🔄 Flujo de Predicción
✨ Características
Interfaz amigable con Streamlit
Cálculo automático de IMC
Validación de datos clínicos
Integración con DataRobot API
Predicción en tiempo real
Visualización de resultados
Manejo de archivos temporales
Arquitectura desacoplada
🚀 Tecnologías
Python
Streamlit
Pandas
DataRobot
Machine Learning
CSV
📁 Estructura del Proyecto

cardiovascular-risk-app/
│
├── app.py
├── predict.py
├── requirements.txt
├── README.md
│
└── .streamlit/
└── secrets.toml

⚙️ Instalación

git clone https://github.com/usuario/cardiovascular-risk-app.git
cd cardiovascular-risk-app

python -m venv venv

venv\Scripts\activate # Windows
source venv/bin/activate # Mac/Linux

pip install -r requirements.txt

🔐 Configuración

Crear archivo:
.streamlit/secrets.toml

DATAROBOT_API_KEY="TU_API_KEY"
DATAROBOT_DEPLOYMENT_ID="TU_DEPLOYMENT_ID"
DATAROBOT_HOST="https://app.datarobot.com"

▶️ Ejecución

streamlit run app.py

📊 Variables del Modelo
genero
edad_anios
estatura_cm
peso_kg
indice_masa_corporal
presion_sistolica
presion_diastolica
colesterol
glucosa
fuma
consume_alcohol
actividad_fisica
📈 Resultados
Probabilidad de riesgo cardiovascular
Clasificación del riesgo
Respuesta del modelo

Ejemplo:
Probabilidad: 84.35%
Resultado: Alto riesgo cardiovascular

🔮 Futuras Mejoras
Dashboard analítico
Historial de pacientes
Base de datos
Autenticación
Dockerización
Despliegue en la nube
Explainable AI
👩‍💻 Autor

Lilliana Uribe
Proyecto académico de Machine Learning y DataRobot
"""

