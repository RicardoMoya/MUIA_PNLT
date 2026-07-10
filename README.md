# MUIA_PNLT — Procesamiento del Lenguaje Natural

Repositorio de materiales didácticos de la asignatura **Procesamiento del Lenguaje Natural** del Máster Universitario en Inteligencia Artificial (MUIA) de U-tad.

---

## Contenido

| Notebook | Descripción |
|---|---|
| `01_instalacion_y_prueba_spacy.ipynb` | Verificación del entorno y primera prueba de spaCy |
| `02_primer_ejemplo_spacy.ipynb` | Pipeline básico de spaCy sobre una frase de ejemplo |
| `03_normalizacion_texto_caso_practico.ipynb` | Caso práctico de normalización textual paso a paso |
| `04_actividad_practica_normalizacion.ipynb` | Actividad práctica: construcción de un pipeline de normalización |
| `05_BoW_Tfidf.ipynb` | Vectorización de texto: Bag of Words y TF-IDF con scikit-learn y Gensim |
| `06_metricas_clasificacion.ipynb` | Métricas de evaluación para modelos de clasificación: Accuracy, Precision, Recall, F-Score y ROC-AUC |
| `07_clasificacion_textos_ejemplo.ipynb` | Pipeline completo de clasificación de textos: normalización, BoW, entrenamiento y evaluación de cuatro clasificadores |
| `08_inferencia_modelo_clasificacion_textos.ipynb` | Inferencia sobre un texto nuevo con el vectorizador y el modelo exportados en el notebook 07 |
| `09_actividad_practica_clasificacion_textos.ipynb` | Actividad práctica: pipeline de clasificación de textos sobre un dataset de soporte telco |
| `10_LSI_ejemplo_basico.ipynb` | Latent Semantic Index/Analysis (LSI): teoría y ejemplo básico con Gensim |
| `11_LDA_ejemplo_basico.ipynb` | Latent Dirichlet Allocation (LDA): teoría y ejemplo básico con Gensim |
| `12_LDA_Topic_Modeling_ejemplo_noticias.ipynb` | Topic Modeling con LDA sobre un corpus de noticias: selección del número óptimo de temas mediante coherencia |
| `13_Ejemplo_embeddings_preentrenados.ipynb` | Embeddings preentrenados (NNLM) con TensorFlow Hub: vectorización de palabras y similitud semántica |
| `14_busqueda_semantica_embeddings.ipynb` | Búsqueda semántica con embeddings preentrenados: normalización ligera, comparación de modelos de 50 y 128 dimensiones |

---

## Instalación del entorno

> **Requisito previo:** todos los comandos deben ejecutarse desde la carpeta raíz del repositorio. Si acabas de clonar el proyecto, navega hasta ella antes de continuar:
> ```bash
> cd MUIA_PNLT
> ```

Los pasos siguientes utilizan [**uv**](https://github.com/astral-sh/uv), una herramienta moderna y rápida para gestionar entornos e instalar dependencias en Python.

### 1. Instalar uv

**macOS / Linux:**
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows (PowerShell):**
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### 2. Crear el entorno virtual

Desde la raíz del repositorio:

```bash
uv venv .venv --python 3.11
```

### 3. Activar el entorno

**macOS / Linux:**
```bash
source .venv/bin/activate
```

**Windows:**
```powershell
.venv\Scripts\activate
```

### 4. Instalar las dependencias

```bash
uv pip install -r requirements.txt
```

### 5. Descargar los modelos de spaCy

```bash
python -m spacy download es_core_news_sm
python -m spacy download en_core_web_sm
```

### 6. Registrar el entorno como kernel de Jupyter

```bash
python -m ipykernel install --user --name .venv --display-name "Python (PNLT)"
```

### 7. Abrir Jupyter Notebook

```bash
jupyter notebook
```

Si da algún error en Windows, abrir el Notebook con el siguiente comando:

```bash
python -m jupyter notebook
```

Al crear o abrir un notebook, selecciona el kernel **Python (PNLT)** para asegurarte de que el entorno con spaCy está activo.

---

## Requisitos

- Python 3.11
- uv >= 0.4

Las dependencias Python están declaradas en [`requirements.txt`](requirements.txt).
