Cargador de Modelo Sentence-BERT y Groq
Este repositorio contiene un Jupyter Notebook configurado en Python 3 que se encarga de descargar y cargar un modelo de Procesamiento de Lenguaje Natural (NLP). Basado en la configuración, el código está diseñado para trabajar con modelos de Sentence Transformers, Hugging Face, y requiere integración con la API de Groq.

📖 Descripción
El notebook utiliza la librería de widgets de Jupyter (@jupyter-widgets) para mostrar barras de progreso interactivas mientras se descargan y reconstruyen los pesos del modelo. Durante su ejecución, el script interactúa con los siguientes archivos clave de la arquitectura del modelo:

model.safetensors: El archivo principal que contiene los pesos del modelo, con un tamaño aproximado de 471 MB.

sentence_bert_config.json: Archivo de configuración específico para generar embeddings de oraciones.

config.json y tokenizer_config.json: Archivos de configuración estándar para la tokenización y la estructura del modelo.

modules.json: Define los submódulos utilizados en el pipeline.

🛠️ Requisitos previos
Para asegurar que las funcionalidades, las barras de carga y los modelos operen correctamente, necesitas contar con las siguientes credenciales y librerías en tu entorno de Python 3:

API Key de Groq: Es un requisito indispensable contar con una clave de API de Groq válida para ejecutar los procesos del notebook. Debe estar configurada en tu entorno (por ejemplo, como la variable de entorno GROQ_API_KEY).

jupyter o acceso a Google Colab

ipywidgets (necesario para renderizar FloatProgressModel y HTMLModel en la interfaz)

sentence-transformers

transformers

huggingface_hub

🚀 Uso
Configura tu API Key de Groq en el sistema o plataforma donde ejecutarás el código.

Abre el archivo .ipynb en tu entorno preferido (Jupyter Notebook, JupyterLab o Google Colab).

Ejecuta las celdas de código de forma secuencial.

El output mostrará interfaces interactivas (HBox) con barras de progreso verdes indicando el estado de la descarga (ej. 315MB / 471MB, 30.5kB/s) y la posterior carga de los pesos en memoria.
