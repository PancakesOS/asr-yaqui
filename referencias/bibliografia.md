# Bibliografía anotada

Última actualización: 2026-11-11. Formato APA 7. Las entradas con **[P]** son lectura prioritaria. Las marcadas *por verificar* necesitan confirmarse contra la fuente original.

Hallazgo central de la búsqueda (corregido el 2026-11-16): **no se encontró ningún trabajo académico centrado en ASR para el yaqui**, pero el modelo masivo **Omnilingual ASR de Meta (noviembre de 2025) incluye al yaqui** (`yaq_Latn`, nivel de recursos bajo). No hay evaluación pública de ese modelo sobre grabaciones de documentación del yaqui. El mayo (`mfy_Latn`), lengua cahita muy cercana, aparece con nivel de recursos medio.

---

## 0. Lo más reciente (2025-2026)

**Omnilingual ASR team, Keren, G., et al. (2025).** *Omnilingual ASR: Open-source multilingual speech recognition for 1600+ languages* [Preprint]. arXiv. https://arxiv.org/abs/2511.09690. Anuncio: [Meta AI](https://ai.meta.com/blog/omnilingual-asr-advancing-automatic-speech-recognition/) **[P]**
- Más de 1,600 lenguas, entre ellas el yaqui. Modelos de 300M a 7B parámetros, licencia Apache 2.0. Variante que transcribe lenguas no vistas con unos cuantos ejemplos de audio y texto (aprendizaje en contexto).
- Es la línea base obligada de la tesis. Pendiente: averiguar de dónde salieron sus datos de yaqui y en qué ortografía.

**Chambers, S., Woodrose Schwartz, S., Kelley, M., y Woodrose Schwartz, L. (2026).** Addressing domain mismatch in ASR for Akuzipik language documentation. En *Proceedings of ComputEL-9* (pp. 93-103). https://aclanthology.org/2026.computel-1.10/ **[P]**
- MMS funciona con habla leída parecida a sus datos (lecturas bíblicas), pero falla con habla espontánea. Ajustarlo con una hora de datos mejora mucho. Es justo el riesgo con los audios de documentación del yaqui.

**Bhandari, V., Kumar, T., y Mulhern, K. (2026).** Voices from the margins: Modeling linguistic diversity in spontaneous speech for low-resource languages. En *Proceedings of ComputEL-9* (pp. 37-54). https://aclanthology.org/2026.computel-1.5/
- Ajuste fino en 21 lenguas con habla espontánea: ningún modelo gana en todas, y un modelo de lenguaje de n-gramas reduce el error hasta 27.3%.

**Liang, S., Lapierre, M., y Levow, G.-A. (2026).** Bottlenecks of in-context learning for fieldwork ASR: A case-study of Panãra. En *Proceedings of ComputEL-9* (pp. 157-166). https://aclanthology.org/2026.computel-1.17/
- Prueba el aprendizaje en contexto (el modo sin reentrenar de Omnilingual) con grabaciones de campo. Los diacríticos y la forma de escribirlos son el principal cuello de botella.

**Liebl, J. E., Chambers, S., Kelley, M., y Walther, G. (2026).** Aspects of selecting the right ASR training languages for under-resourced languages. En *Proceedings of ComputEL-9*. https://aclanthology.org/2026.computel-1.16/
- Entrenar con lenguas parecidas ayuda, aunque el tipo de parecido que más importa cambia según la lengua. Sugiere probar a usar datos del mayo para el yaqui.

**Gessler, L., Anastasopoulos, A., et al. (2026).** The missing middle: Language documentation needs better infrastructure, not better models. En *Proceedings of ComputEL-9*. https://aclanthology.org/2026.computel-1.15/
- Artículo de posición: lo que falta en documentación no son modelos mejores, sino herramientas que los integren al trabajo diario. Respalda el componente de aplicación de la tesis.

---

## 1. El yaqui: lengua, ortografía y textos (español)

Estas obras no son de ASR, pero definen la fonología, la ortografía y las posibles fuentes de texto para un modelo de lenguaje.

**Estrada Fernández, Z. (2009).** *Yaqui de Sonora* (Archivo de Lenguas Indígenas de México, 29). El Colegio de México. ISBN 978-607-462-041-2. [Repositorio Colmex](https://repositorio.colmex.mx/downloads/s1784p69f?locale=en) **[P]**
- Fonología con vocales dobles, consonantes geminadas, alófonos y entonación, más un texto analizado y léxico. Base para justificar cómo se tratan la longitud vocálica y el saltillo en las transcripciones.

**Estrada Fernández, Z., Carlón, A., Buitimea, C., Gurrola, H., y Castillo, M. (2004).** *Diccionario yaqui-español y textos: Obra de preservación lingüística*. Universidad de Sonora; Plaza y Valdés. *Coautores por verificar.*
- 405 páginas, diccionario bilingüe y colección de textos. Fuente de vocabulario y de texto escrito en la ortografía de la Dra. Estrada.
- Una reseña en *Language in Society* (2006) señala que Estrada escribe *b* y *j* donde otros autores escriben *v* y *h*. Esa variación ortográfica afecta directamente el vocabulario de salida del modelo.

**Estrada Fernández, Z., Silva Encinas, M. C., Buitimea Valenzuela, C., y Bejípone Cruz, M. (2021).** *Jiak noki lutu'uria into tenkui etejoi. Historias sobre la cultura y sueños en lengua yaqui*. Universidad de Sonora. ISBN 978-607-518-454-8. [Libros Unison](https://libros.unison.mx/index.php/unison/catalog/download/185/305/1200?inline=1)
- Narraciones con versión ortográfica, glosa interlineal y traducción. Posible fuente de texto para un modelo de lenguaje y ejemplo del formato de anotación que usa el equipo.

**Estrada Fernández, Z., y Bejípone Cruz, M. (2011).** Ori: partícula discursiva en yaqui como patrón de uso gramatical. *Lingüística, 25*, 150-166. [PDF](https://mundoalfal.org/sites/default/files/revista/25_linguistica_150_166.pdf)
- Describe una partícula que expresa duda o pausa. Relevante para el habla espontánea: el modelo tendrá que transcribir rellenos y pausas que el texto escrito suele omitir.

**Guerrero, L.** Don Fermín, una historia de vida yaqui. *Tlalocan*. [Artículo](https://revistas-filologicas.unam.mx/tlalocan/index.php/tl/article/view/490). *Año y volumen por verificar.*
- Texto oral yaqui transcrito, con reseña de los textos publicados en *Tlalocan*. Útil para ubicar otras fuentes de texto.

**Dedrick, J. M., y Casad, E. H. (1999).** *Sonora Yaqui language structures*. University of Arizona Press.

**Shaul, D. L. (1999).** *Yoeme-English, English-Yoeme standard dictionary*. Hippocrene Books.
- Ortografía de Arizona. Útil para documentar la variación entre convenciones.

---

## 2. ASR para lenguas indígenas en México y en español

**Cruz, H. (2021).** Las tecnologías de reconocimiento automático de voz y su incorporación a los métodos de transcripción de lenguas indígenas. *Anales de Antropología, 55*(2). https://doi.org/10.22201/iia.24486221e.2021.77857 *Volumen por verificar.* **[P]**
- La referencia en español más cercana a tu tema. Discute cómo integrar el ASR a la transcripción de lenguas indígenas mexicanas y señala que los hablantes alfabetizados en español tienen dificultad para escribir tonos y saltillos. Buen apoyo para la introducción y la justificación.

**Coto-Solano, R., y Flores Solórzano, S. (2016).** Alineación forzada sin entrenamiento para la anotación automática de corpus orales de las lenguas indígenas de Costa Rica. *Káñina, Revista de Artes y Letras, 40*(extraordinario), 175-199. [PDF](https://revistas.ucr.ac.cr/index.php/kanina/article/download/30234/30212/86577)
- Alineación forzada para bribri, cabécar y malecu. Referencia en español para la etapa de alineación.

**Tesis de identificación automática de lenguas indígenas** (*autores y años por verificar*):
- INAOE: *Un método para la identificación automática del lenguaje hablado*, con pruebas en náhuatl y zoque. [PDF](https://inaoe.repositorioinstitucional.mx/jspui/bitstream/1009/646/1/ReyesHAL.pdf)
- UNAM, Maestría en Ingeniería: López García, B. J., *Sistema de identificación de lenguas indígenas para la indexación de audio* (náhuatl, mixteco, maya y ñañú). [PDF](https://ru.dgb.unam.mx/server/api/core/bitstreams/e28f3e31-f0a1-4363-9e91-b7595ecea6b2/content)
- TecNM Ciudad Madero: *Reconocimiento de habla en palabras aisladas en lenguas indígenas de San Luis Potosí*. [PDF](https://rinacional.tecnm.mx/bitstream/TecNM/3085/1/G06071568_donacion_tesis_bib.pdf)
- TecNM Ciudad Madero: *Corpus de las lenguas indígenas tének, náhuatl* (y otras). [PDF](https://rinacional.tecnm.mx/bitstream/TecNM/3069/1/G06070532_donacion_tesis_bib.pdf)
- Estos trabajos usan métodos anteriores al aprendizaje profundo. Sirven para mostrar la línea mexicana previa y que la construcción de corpus de habla en México sigue siendo escasa.

**Inteligencia artificial para el análisis de la pronunciación de lenguas indígenas.** *Contactos*, UAM Iztapalapa. [PDF](https://contactos.izt.uam.mx/index.php/contactos/article/download/348/186/). *Autores y año por verificar.*
- Divulgación sobre retos del análisis de audio en lenguas indígenas mexicanas (caso del otomí de Ixtenco, sin alfabeto establecido).

**Shi, J., Amith, J. D., Castillo García, R., Guadalupe Sierra, E., Duh, K., y Watanabe, S. (2021).** Leveraging end-to-end ASR for endangered language documentation: An empirical study on Yoloxóchitl Mixtec. En *Proceedings of EACL 2021* (pp. 1134-1145). https://doi.org/10.18653/v1/2021.eacl-main.96 **[P]**
- Mixteco de Yoloxóchitl con 100 h transcritas, receta reproducible en ESPnet y propuesta de que transcriptores novatos corrijan la salida del modelo. Muy cercano a tu aplicación de creación de corpus.

**Amith, J. D., Shi, J., y Castillo García, R. (2021).** End-to-end automatic speech recognition: Its impact on the workflow in documenting Yoloxóchitl Mixtec. En *Proceedings of the First AmericasNLP Workshop* (pp. 64-80). https://doi.org/10.18653/v1/2021.americasnlp-1.8
- Evalúa el ASR por el esfuerzo humano que ahorra, no solo por WER o CER.

**Pugh, R., Sreedhar, V., y Tyers, F. (2024).** Wav2pos: Exploring syntactic analysis from audio for Highland Puebla Nahuatl. En *Proceedings of AmericasNLP 2024*. https://aclanthology.org/2024.americasnlp-1.13
- Ajuste de Wav2Vec2 para náhuatl (lengua yuto-nahua, como el yaqui) con datos de OpenSLR.

**Tesis sobre totonaco (2024).** Universidad de Alberta. [ERA](https://era.library.ualberta.ca/items/aa797047-a121-4b2b-8d48-625eb5996ef0). *Autor por verificar.*
- Totonaco de Coatepec y Upper Necaxa: MMS dio los mejores resultados y la salida sirvió como plantilla para la corrección manual.

---

## 3. ASR para lenguas indígenas del continente

**Mainzinger, J., y Levow, G.-A. (2024).** Fine-tuning ASR models for very low-resource languages: A study on Mvskoke. En *Proceedings of ACL 2024 (Student Research Workshop)* (pp. 170-176). https://doi.org/10.18653/v1/2024.acl-srw.16. Tesis de maestría asociada: [UW](https://digital.lib.washington.edu/researchworks/items/8364eacd-2d41-4597-b7e5-d715b38aa639) **[P]**
- El caso más parecido al tuyo. Compara XLSR-53, MMS-300M y MMS-1B con 10, 60, 120 y 243 minutos de datos, y adaptadores contra ajuste completo.

**Romero, M., Gómez-Canaval, S., y Torre, I. G. (2024).** Automatic speech recognition advancements for Indigenous languages of the Americas. *Applied Sciences, 14*(15), 6497. https://doi.org/10.3390/app14156497 **[P]**
- Ganadores de AmericasNLP 2022 con XLS-R. CER de 12.14 (quechua) a 36.59 (kotiria); la congelación de capas y el dropout pesan más que el número de épocas.

**Ebrahimi, A., Mager, M., Wiemerslage, A., et al. (2023).** Findings of the Second AmericasNLP Competition on Speech-to-Text Translation. *PMLR, 220*, 217-232. [PDF](https://proceedings.mlr.press/v220/ebrahimi23a/ebrahimi23a.pdf) **[P]**
- Justifica usar CER como métrica principal cuando los límites de palabra no están estandarizados.

**Coto-Solano, R., Kim, T. W., Jones, A., y Loáiciga, S. (2024).** Multilingual models for ASR in Chibchan languages. En *Proceedings of NAACL 2024*. https://aclanthology.org/2024.naacl-long.471 **[P]**
- Compara Wav2Vec2, Whisper, MMS y WavLM con 143 minutos (bribri) y 54 minutos (cabécar).

**Coto-Solano, R. (2021).** Explicit tone transcription improves ASR performance in extremely low-resource languages: A case study in Bribri. En *Proceedings of AmericasNLP 2021*. https://doi.org/10.18653/v1/2021.americasnlp-1.20
- La forma de escribir los tonos cambia el desempeño. Respalda definir la convención ortográfica antes de entrenar.

**Coto-Solano, R., Browning, M., Corrado, T., y Nicholas, S. A. (2026).** Voice activation detection for transcription of Indigenous languages. En *Proceedings of ComputEL 2026*. https://aclanthology.org/2026.computel-1.19/
- Compara detectores de voz como primer paso del flujo de transcripción.

**Prud'hommeaux, E., Jimerson, R., Hatcher, R., y Michelson, K. (2021).** Automatic speech recognition for supporting endangered language documentation. *Language Documentation & Conservation, 15*. http://hdl.handle.net/10125/74666 **[P]**
- Mide con cronómetro la transcripción con y sin ASR (séneca), hecha por lingüistas y miembros de la comunidad.

**Jimerson, R., Simha, K., Ptucha, R., y Prud'hommeaux, E. (2018).** Improving ASR output for endangered language documentation. En *Proceedings of SLTU 2018* (pp. 187-191). https://doi.org/10.21437/SLTU.2018-39
- Aumento de datos acústico y de texto con 155 minutos de séneca.

**Liang, S., y Levow, G.-A. (2025).** *Breaking the transcription bottleneck: Fine-tuning ASR models for extremely low-resource fieldwork languages* [Preprint]. arXiv. https://arxiv.org/abs/2506.17459
- Ajuste fino con habla espontánea y ruidosa de trabajo de campo, no habla leída.

**Kriukova et al. (2026).** Choosing an ASR model for Dënë Sųłıné: Navigating polysynthesis and unstandardized orthography. En *Proceedings of ComputEL 2026* (pp. 15-25). https://aclanthology.org/2026.computel-1.3/ *Autores por completar.*
- Contraejemplo: aquí Whisper superó a Wav2Vec2. Justifica probar ambas familias de modelos.

**Foley, B., Arnold, J., Coto-Solano, R., et al. (2018).** Building speech recognition systems for language documentation: The CoEDL Endangered Language Pipeline and Inference System (Elpis). En *Proceedings of SLTU 2018*. https://doi.org/10.21437/SLTU.2018-43
- Herramienta para que documentalistas sin experiencia en cómputo entrenen modelos (16 lenguas). Antecedente directo de tu aplicación: su meta no es automatizar todo, sino un flujo de trabajo práctico con corrección humana.

---

## 4. Modelos de voz preentrenados y modelos ligeros

**Pratap, V., Tjandra, A., Shi, B., et al. (2024).** Scaling speech technology to 1,000+ languages. *Journal of Machine Learning Research, 25*(97), 1-52. https://www.jmlr.org/papers/v25/23-1318.html **[P]**
- MMS: ASR para 1,107 lenguas, menos de la mitad del WER de Whisper en 54 lenguas de FLEURS. Incluye un algoritmo de alineación forzada disponible en TorchAudio.

**Babu, A., Wang, C., Tjandra, A., et al. (2022).** XLS-R: Self-supervised cross-lingual speech representation learning at scale. En *Proceedings of Interspeech 2022*. *Páginas y DOI por verificar.*

**Baevski, A., Zhou, H., Mohamed, A., y Auli, M. (2020).** wav2vec 2.0: A framework for self-supervised learning of speech representations. *Advances in Neural Information Processing Systems, 33*.

**Radford, A., Kim, J. W., Xu, T., Brockman, G., McLeavey, C., y Sutskever, I. (2023).** Robust speech recognition via large-scale weak supervision. En *Proceedings of ICML 2023*. PMLR.

**Seamless Communication, Barrault, L., et al. (2023).** *Seamless: Multilingual expressive and streaming speech translation* [Preprint]. arXiv. https://arxiv.org/abs/2312.05187
- Origen de W2V-BERT 2.0. Según la [guía de Hugging Face](https://huggingface.co/blog/fine-tune-w2v2-bert), iguala a Whisper large-v3 en mongol siendo de 10 a 30 veces más rápido.

**Gandhi, S., von Platen, P., y Rush, A. M. (2023).** *Distil-Whisper: Robust knowledge distillation via large-scale pseudo labelling* [Preprint]. arXiv. https://arxiv.org/abs/2311.00430
- Destilación: un modelo 5.8 veces más rápido con 51% menos parámetros, a 1% de WER del original. Referencia para la parte de "modelo ligero".

---

## 5. Ética y gobernanza de datos indígenas

**Bird, S. (2020).** Decolonising speech and language technology. En *Proceedings of COLING 2020* (pp. 3504-3519). https://doi.org/10.18653/v1/2020.coling-main.313
- Crítica a tratar las lenguas indígenas como datos disponibles. Fundamenta el procesamiento local y el papel de los lingüistas y la comunidad.

**Carroll, S. R., Garba, I., Figueroa-Rodríguez, O. L., et al. (2020).** The CARE principles for Indigenous data governance. *Data Science Journal, 19*(1), 43. https://doi.org/10.5334/dsj-2020-043
- Principios CARE (beneficio colectivo, autoridad para controlar, responsabilidad y ética), complementarios a FAIR. Encaja con la sección de gestión ética de datos que pide el reporte técnico.

---

## Pendientes de búsqueda

- Repositorio de tesis de la Maestría en Lingüística de la Unison (por ejemplo, Silva Encinas, 2004) y trabajos del grupo de la Dra. Estrada sobre fonética del yaqui.
- Trabajos de 2025-2026 en AmericasNLP y ComputEL sobre lenguas yuto-nahuas.
- Literatura sobre cuantización e inferencia local en Apple Silicon (whisper.cpp, MLX).
