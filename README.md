# cardiovascular-risk-prediction-datarobot
Aplicación web desarrollada en Python y Streamlit que permite estimar el riesgo de enfermedad cardiovascular mediante un modelo de Machine Learning desplegado en DataRobot.
# **🫀 Predicción de Riesgo Cardiovascular con DataRobot**

Aplicación web desarrollada en **Python** y **Streamlit** que permite estimar el riesgo de enfermedad cardiovascular utilizando un modelo de **Machine Learning desplegado en DataRobot**.

---

# **📋 Tabla de Contenido**

* Descripción  
* Arquitectura  
* Características  
* Tecnologías  
* Estructura del Proyecto  
* Instalación  
* Configuración  
* Ejecución  
* Variables del Modelo  
* Resultados  
* Futuras Mejoras  
* Autor

---

# **📖 Descripción**

La aplicación captura información clínica de un paciente, calcula automáticamente el **Índice de Masa Corporal (IMC)** y envía los datos a un modelo desplegado en **DataRobot** para generar una predicción de riesgo cardiovascular.

## **Variables Analizadas**

* Edad  
* Género  
* Estatura  
* Peso  
* Índice de Masa Corporal (IMC)  
* Presión Sistólica  
* Presión Diastólica  
* Colesterol  
* Glucosa  
* Consumo de Tabaco  
* Consumo de Alcohol  
* Actividad Física

---

# **🏗️ Arquitectura**

## **Diagrama de Arquitectura (PlantUML)**

@startuml

skinparam componentStyle rectangle

actor Usuario

rectangle "Streamlit UI\\n(app.py)" as APP  
rectangle "Prediction Service\\n(predict.py)" as PRED  
database "CSV Temporal" as CSV  
cloud "DataRobot Deployment" as DR

Usuario \--\> APP : Ingresa datos clínicos

APP \--\> CSV : Genera CSV  
APP \--\> PRED : Ejecuta proceso

PRED \--\> DR : Solicita predicción  
DR \--\> PRED : Resultado

PRED \--\> APP : Probabilidad y clasificación

APP \--\> Usuario : Mostrar resultado

@enduml  
---

## **Flujo de Predicción**

@startuml

start

:Capturar datos clínicos;

:Calcular IMC;

:Validar presión arterial;

if (Datos válidos?) then (Sí)

:Crear CSV temporal;

:Ejecutar predict.py;

:Enviar datos a DataRobot;

:Obtener resultado;

:Mostrar probabilidad;

:Mostrar clasificación;

else (No)

:Mostrar error;

endif

stop

@enduml  
---

# **✨ Características**

* ✅ Interfaz amigable desarrollada con Streamlit.  
* ✅ Cálculo automático del IMC.  
* ✅ Validación de datos clínicos.  
* ✅ Integración con DataRobot.  
* ✅ Predicción en tiempo real.  
* ✅ Visualización de probabilidades.  
* ✅ Gestión automática de archivos temporales.  
* ✅ Arquitectura desacoplada entre interfaz y servicio de predicción.

---

# **🚀 Tecnologías**

### **🐍 Lenguaje Principal**

### **🎈 Desarrollo Web**

### **📊 Procesamiento de Datos**

### **🤖 Inteligencia Artificial**

### **📄 Formato de Datos**

\# 🚀 Tecnologías

\#\# 🐍 Lenguaje Principal

\<p align="left"\>  
  \<img src="https://skillicons.dev/icons?i=python" height="60" alt="Python"/\>  
\</p\>

\!\[Python\](https://img.shields.io/badge/Python-3776AB?style=for-the-badge\&logo=python\&logoColor=white)

\---

\#\# 🎈 Desarrollo Web

\<p align="left"\>  
  \<img src="https://skillicons.dev/icons?i=streamlit" height="60" alt="Streamlit"/\>  
\</p\>

\!\[Streamlit\](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge\&logo=streamlit\&logoColor=white)

\---

\#\# 📊 Procesamiento de Datos

\<p align="left"\>  
  \<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" height="60" alt="Pandas"/\>  
\</p\>

\!\[Pandas\](https://img.shields.io/badge/Pandas-150458?style=for-the-badge\&logo=pandas\&logoColor=white)

\---

\#\# 🤖 Inteligencia Artificial

\<p align="left"\>  
  \<img src="https://cdn.simpleicons.org/datarobot" height="60" alt="DataRobot"/\>  
\</p\>

\!\[DataRobot\](https://img.shields.io/badge/DataRobot-Batch\_Predictions-orange?style=for-the-badge)

\!\[Machine Learning\](https://img.shields.io/badge/Machine\_Learning-Predictive\_Model-green?style=for-the-badge)

\---

\#\# 📄 Formato de Datos

\<p align="left"\>  
  \<img src="https://cdn-icons-png.flaticon.com/512/6133/6133884.png" height="60" alt="CSV"/\>  
\</p\>

\!\[CSV\](https://img.shields.io/badge/CSV-Input\_Output\_Data-lightgrey?style=for-the-badge)

\---

\#\# 🏆 Stack Tecnológico

\<p align="center"\>  
  \<img src="https://skillicons.dev/icons?i=python,streamlit" /\>  
\</p\>

\<p align="center"\>  
  \<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge\&logo=pandas\&logoColor=white"/\>  
  \<img src="https://img.shields.io/badge/DataRobot-FF6F00?style=for-the-badge"/\>  
  \<img src="https://img.shields.io/badge/Machine\_Learning-AI-success?style=for-the-badge"/\>  
  \<img src="https://img.shields.io/badge/CSV-Data\_File-lightgrey?style=for-the-badge"/\>  
\</p\>

---

# **📁 Estructura del Proyecto**

cardiovascular-risk-app/  
│  
├── app.py  
├── predict.py  
├── requirements.txt  
├── README.md  
│  
└── .streamlit/  
    └── secrets.toml

## **Estructura UML**

@startmindmap

\* Cardiovascular Risk App  
\*\* app.py  
\*\*\* Interfaz Streamlit  
\*\*\* Captura Datos  
\*\*\* Cálculo IMC  
\*\*\* Validaciones

\*\* predict.py  
\*\*\* Batch Prediction API  
\*\*\* Comunicación DataRobot  
\*\*\* Descarga Resultados

\*\* requirements.txt

\*\* README.md

\*\* .streamlit  
\*\*\* secrets.toml

@endmindmap  
---

# **⚙️ Instalación**

## **1\. Clonar el repositorio**

git clone https://github.com/usuario/cardiovascular-risk-app.git  
cd cardiovascular-risk-app

## **2\. Crear entorno virtual**

python \-m venv venv

### **Windows**

venv\\Scripts\\activate

### **Linux / Mac**

source venv/bin/activate

## **3\. Instalar dependencias**

pip install \-r requirements.txt  
---

# **🔐 Configuración**

Crear el archivo:

.streamlit/secrets.toml

Contenido:

DATAROBOT\_API\_KEY="TU\_API\_KEY"  
DATAROBOT\_DEPLOYMENT\_ID="TU\_DEPLOYMENT\_ID"  
DATAROBOT\_HOST="https://app.datarobot.com"  
---

# **▶️ Ejecución**

streamlit run app.py  
---

# **📊 Variables del Modelo**

| Variable | Tipo |
| ----- | ----- |
| genero | Numérica |
| edad\_anios | Numérica |
| estatura\_cm | Numérica |
| peso\_kg | Numérica |
| indice\_masa\_corporal | Numérica |
| presion\_sistolica | Numérica |
| presion\_diastolica | Numérica |
| colesterol | Categórica |
| glucosa | Categórica |
| fuma | Binaria |
| consume\_alcohol | Binaria |
| actividad\_fisica | Binaria |

---

# **📈 Resultado**

La aplicación devuelve:

* Probabilidad de enfermedad cardiovascular.  
* Clasificación binaria del riesgo.  
* Respuesta completa del modelo desplegado.

### **Ejemplo**

Probabilidad: 84.35%

Predicción:  
Posible enfermedad cardiovascular  
---

# **🔮 Futuras Mejoras**

* Dashboard de analítica avanzada.  
* Historial de pacientes.  
* Integración con bases de datos.  
* Autenticación de usuarios.  
* Dockerización de la aplicación.  
* Despliegue en la nube.  
* Explicabilidad del modelo (Explainable AI).

---

# **🌐 DataRobot**

[https://app.datarobot.com/homepage/main](https://app.datarobot.com/homepage/main)

---

# **👩‍💻 Autor**

**Lilliana Uribe**

Proyecto académico enfocado en Machine Learning, Analítica Predictiva y despliegue de modelos utilizando DataRobot y Streamlit.

