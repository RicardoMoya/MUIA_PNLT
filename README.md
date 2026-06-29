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

### 5. Descargar el modelo de español de spaCy

```bash
python -m spacy download es_core_news_sm
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


Al crear o abrir un notebook, selecciona el kernel **Python (NLP)** para asegurarte de que el entorno con spaCy está activo.

---

## Requisitos

- Python 3.11
- uv >= 0.4

Las dependencias Python están declaradas en [`requirements.txt`](requirements.txt).
