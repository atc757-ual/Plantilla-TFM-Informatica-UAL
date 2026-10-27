# TFM — Plataforma de carpooling universitario P2P con Gemelos Digitales

Memoria del Trabajo Fin de Máster **«Plataforma de carpooling universitario P2P basada en Gemelos Digitales, *matching* y simulación»**, del Máster en Ingeniería Informática de la Universidad de Almería.

Autor: Alex César Taquila Camasca · Director: Javier Criado Rodríguez · Curso 2026/2027

## Contenido

- Memoria en LaTeX: 21 capítulos y 5 anexos (A–E). Los capítulos 16–20 (implementación, pruebas, resultados, discusión y conclusiones) son por ahora un esqueleto con marcas en rojo («Por desarrollar»).
- 15 figuras, todas dibujadas en TikZ (vectoriales): casos de uso, clases, arquitectura, entidad-relación, secuencias, actividad, estados y Gantt.
- Bibliografía en BibTeX con 88 referencias.

## Estructura

| Ruta | Contenido |
|---|---|
| `main.tex` | Documento principal: paquetes, datos del TFM y orden de los capítulos |
| `contenido1.tex` … `contenido15.tex` | Capítulos 1 a 15 (planteamiento, diseño y planificación) |
| `contenido-implementacion.tex`, `contenido-pruebas.tex`, `contenido-resultados.tex` | Capítulos 16 a 20, por desarrollar |
| `contenido16.tex` | Bibliografía (capítulo 21) |
| `apendices.tex` | Anexos A a E |
| `resumentexto.tex` | Resumen, palabras clave y *abstract* |
| `indicesyrefe.tex`, `contra.tex` | Índices, abreviaturas y contraportada |
| `referencias.bib` | Base bibliográfica |
| `diagramas/` | Figuras TikZ, una por fichero, incluidas con `\input` |
| `Figuras/` | Logotipos institucionales |
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
