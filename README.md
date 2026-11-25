# ASR para el yaqui: bitácora del trabajo terminal

Repositorio-bitácora del trabajo terminal de la Maestría en Ciencia de Datos (Universidad de Sonora), modalidad **reporte técnico**.

**Título provisional:** Reconocimiento automático del habla para lenguas originarias de Sonora: transcripción de audio con modelos ligeros para uso comunitario.

**Objetivo general:** pasar de un audio en yaqui (*Yoem Noki*) a su transcripción escrita, con un modelo ligero que funcione de forma local y apoye la creación de corpus junto con los lingüistas.

## Estructura

| Carpeta | Contenido |
| --- | --- |
| `bitacora/` | Una entrada por sesión de trabajo: qué se hizo, qué se encontró, qué sigue. |
| `referencias/` | Bibliografía anotada (`bibliografia.md`) y archivo BibTeX (`referencias.bib`). Solo metadatos y enlaces, no PDF con derechos de autor. |
| `estado-del-arte/` | Borradores del estado del arte. |
| `docs/` | Documentos del programa (seminarios, directrices) y minutas de reuniones. |
| `notebooks/` | Exploraciones en Jupyter. |
| `src/` | Código del proyecto (Python). |
| `data/` | **No se versiona.** Ver `data/README.md`. |

## Manejo de datos

Los audios y transcripciones pertenecen a la comunidad yaqui y al equipo de la Dra. Zarina Estrada Fernández.

- Ningún audio, transcripción ni glosa se sube a este repositorio ni a servicios externos.
- Todo el procesamiento se hace de forma local o en la supercomputadora de la universidad.
- El repositorio debe mantenerse **privado** mientras no se acuerde otra cosa con los lingüistas y con la Universidad del Pueblo Yaqui.

## Entorno

El entorno se gestiona con [`uv`](https://docs.astral.sh/uv/).

```bash
uv sync            # instala dependencias
uv run jupyter lab # abre los notebooks
```

## Cómo usar la bitácora

1. Al terminar cada sesión, copia `bitacora/plantilla.md` a `bitacora/AAAA-MM-DD.md` y llénala.
2. Cada referencia nueva se agrega a `referencias/referencias.bib` y, con una nota breve, a `referencias/bibliografia.md`.
3. Haz *commit* al final de la sesión con un mensaje descriptivo (por ejemplo, `bitacora: lectura de Mainzinger y Levow 2024`).

## Estado actual

- [x] Bibliografía inicial en inglés y español.
- [x] Propuesta de estructura del estado del arte.
- [ ] Acceso a los audios de la Dra. Estrada.
- [ ] Redacción del estado del arte.
