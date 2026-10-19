# TFM — Plataforma de carpooling universitario P2P con Gemelos Digitales

Memoria del Trabajo Fin de Máster **«Diseño de una plataforma de carpooling universitario P2P basada en Gemelos Digitales, *matching* y simulación»**, del Máster en Ingeniería Informática de la Universidad de Almería.

Autor: Alex César Taquila Camasca · Director: Javier Criado Rodríguez · Curso 2026/2027

## Contenido

- Memoria completa en LaTeX: 16 capítulos y 6 anexos (A–F).
- 8 figuras: las de arquitectura, secuencias y actividad están dibujadas en TikZ (vectoriales); el DCU y el DCL son imágenes.
- Bibliografía en BibTeX con 81 referencias, clasificadas según ISO/IEC 25010:2011.

## Estructura

| Ruta | Contenido |
|---|---|
| `main.tex` | Documento principal: paquetes, datos del TFM y orden de los capítulos |
| `contenido1.tex` … `contenido16.tex` | Los 16 capítulos de la memoria |
| `apendices.tex` | Anexos A a F |
| `resumentexto.tex` | Resumen, palabras clave y *abstract* |
| `indicesyrefe.tex`, `contra.tex` | Índices, abreviaturas y contraportada |
| `referencias.bib` | Base bibliográfica |
| `diagramas/` | Figuras TikZ, una por fichero, incluidas con `\input` |
| `Figuras/` | Imágenes (DCU, DCL) y logotipos institucionales |
| `Codigo/` | Reservado para el código del prototipo |
| `UAL.sty`, `codigo.sty` | Estilo de la plantilla de la UAL |

## Compilar

```bash
latexmk -pdf main.tex
```

O el ciclo manual:

```bash
pdflatex main.tex && bibtex main && pdflatex main.tex && pdflatex main.tex
```

El resultado es `main.pdf`. Requiere una distribución TeX Live o MiKTeX con `titlesec`, `pgfgantt` y `tikz` (incluidos en las instalaciones completas).

## Notas

- El PDF **no se versiona** (está en `.gitignore`): se regenera compilando.
- Proyecto basado en la plantilla [Plantilla-TFM-Informatica-UAL](https://github.com/savinspm/Plantilla-TFM-Informatica-UAL), que se conserva como remoto `upstream`.
