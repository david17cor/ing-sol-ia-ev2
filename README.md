Cargador de Modelo Sentence-BERT y Groq
Este repositorio contiene un Jupyter Notebook configurado en Python 3 que se encarga de descargar y cargar un modelo de Procesamiento de Lenguaje Natural (NLP). Según su configuración, el código está diseñado para trabajar con modelos de Sentence Transformers, Hugging Face y requiere integración con la API de Groq.
📖 Descripción
El notebook utiliza la librería de widgets de Jupyter (@jupyter-widgets) para mostrar barras de progreso interactivas mientras se descargan y cargan los pesos del modelo.

Durante su ejecución, el script interactúa con los siguientes archivos clave de la arquitectura del modelo:
- model.safetensors: archivo principal que contiene los pesos del modelo, con un tamaño aproximado de 471 MB.
- sentence_bert_config.json: archivo de configuración específico para generar embeddings de oraciones.
- config.json y tokenizer_config.json: archivos de configuración estándar para la tokenización y la estructura del modelo.
- modules.json: define los submódulos utilizados en el pipeline.
🛠️ Requisitos previos
Para que las funcionalidades, las barras de progreso y los modelos operen correctamente, necesitas contar con las siguientes credenciales y librerías en tu entorno de Python 3.
Credenciales
- API Key de Groq: se requiere una clave de API de Groq válida para ejecutar los procesos del notebook. Configúrala en tu entorno, por ejemplo, mediante la variable de entorno GROQ_API_KEY.
Entorno y librerías
- Jupyter Notebook, JupyterLab o Google Colab.
- ipywidgets (necesario para renderizar componentes interactivos como FloatProgressModel y HTMLModel).
- sentence-transformers
- transformers
- huggingface_hub
🚀 Uso
1. Configura tu API Key de Groq en el sistema o plataforma donde ejecutarás el código.
2. Abre el archivo .ipynb en tu entorno preferido: Jupyter Notebook, JupyterLab o Google Colab.
3. Ejecuta las celdas de código de forma secuencial.
4. Observa las salidas del notebook para revisar el progreso de la descarga y la carga de los pesos del modelo.
Durante la ejecución, la salida puede mostrar interfaces interactivas (HBox) con barras de progreso verdes que indican el estado de la descarga, por ejemplo, 315 MB / 471 MB, junto con información de velocidad, como 30.5 kB/s, y el proceso posterior de carga de los pesos en memoria.
📦 Archivos del modelo
Archivo	Descripción
model.safetensors	Contiene los pesos del modelo.
sentence_bert_config.json	Configuración de Sentence-BERT para generar embeddings de oraciones.
config.json	Configuración general de la arquitectura del modelo.
tokenizer_config.json	Configuración del tokenizador.
modules.json	Define los módulos que componen el pipeline.


📝 Notas
- Asegúrate de mantener tu clave de Groq privada. No la incluyas directamente en el notebook ni la subas al repositorio.
- La disponibilidad y visualización de las barras de progreso puede variar según el entorno de ejecución.
- El tamaño de los archivos y la velocidad de descarga pueden variar.
