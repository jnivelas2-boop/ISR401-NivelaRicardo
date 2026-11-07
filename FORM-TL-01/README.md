# ISR401-NivelaRicardo

Repositorio personal de **Ingeniería de Requerimientos (ISR-401)**, 4.º nivel, paralelo B, SPA 2026–2027.
Estudiante: **Nivela Saavedra José Ricardo**.

Universidad Técnica Estatal de Quevedo.
Docente: Gleiston Cicerón Guerrero Ulloa, PhD.

## Contenido

| **Carpeta** | **Actividad** | **Archivo principal** | **PDF compilado** |
|---|---|---|---|
| `FORM-TL-01/` | Taller de clasificación y cuantificación de requisitos (formativa) | `main.tex` | `main.pdf` |

Caso de estudio: **Plataforma de gestión de citas médicas del Policlínico Ribera del Quevedo**.
El documento incluye la clasificación de 20 enunciados, la cuantificación de cinco requisitos de calidad vagos y la tabla de discusión de discrepancias con Jostin Vélez.

Estructura de `FORM-TL-01/`:

```text
FORM-TL-01/
├── main.tex          documento principal
├── referencias.bib   referencias bibliográficas (estilo IEEE)
├── main.pdf          PDF compilado
└── README.md         descripción e instrucciones de compilación
```

## Cómo compilar en Overleaf

Configuración del proyecto:

| **Opción de Overleaf (Menú)** | **Valor** |
|---|---|
| Compiler | **pdfLaTeX** |
| Main document | **main.tex** |

Este documento usa la clase **`article`**, el compilador **pdfLaTeX**, el gestor **BibTeX** y el estilo bibliográfico **`IEEEtran.bst`**.
Sus paquetes son `inputenc`, `fontenc`, `geometry`, `booktabs`, `longtable`, `array`, `hyperref` y `cite`.
Para compilar se necesitan solamente **`main.tex` y `referencias.bib`**; el documento no utiliza imágenes ni archivos de secciones externos.

### Pasos

1. Crear un proyecto vacío en Overleaf.
2. Subir los archivos `main.tex` y `referencias.bib` de esta carpeta. Ambos deben quedar en la raíz del proyecto. Si el proyecto contiene un `main.tex` de ejemplo, sustituirlo por el del taller.
3. En la configuración, seleccionar **pdfLaTeX** como compilador y **main.tex** como documento principal.
4. Pulsar **Recompilar**. La bibliografía se procesa con BibTeX a partir de `referencias.bib`.
5. Descargar el PDF generado.

No hace falta subir el PDF existente, los archivos auxiliares de compilación ni la carpeta `tmp/`.

### Si algo falla

- **No se encuentra `referencias.bib`:** comprobar que esté en la misma carpeta que `main.tex` y conserve exactamente ese nombre.
- **Las referencias aparecen como `[?]`:** recompilar; si persiste, usar **Recompile from scratch** en las opciones de recompilación.
- **No se encuentra `IEEEtran.bst` en una instalación local:** instalar el paquete `IEEEtran` desde el gestor de paquetes de la distribución LaTeX.

## Cómo compilar localmente

Con TeX Live o MiKTeX instalado, ejecutar desde la raíz del repositorio:

```bash
cd FORM-TL-01
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Si ya estás dentro de `FORM-TL-01`, omitir el primer comando.
El resultado es `FORM-TL-01/main.pdf`.

### Verificación realizada

Se probó una compilación local desde cero con copias únicamente de `main.tex` y `referencias.bib`, usando la secuencia anterior. Se generó un PDF de cinco páginas, sin citas ni referencias cruzadas pendientes. Esta comprobación se realizó con MiKTeX; no se ejecutó una prueba dentro de Overleaf.
