# Propuesta de estado del arte

Borrador de estructura con los argumentos principales de cada sección. Las citas remiten a `../referencias/bibliografia.md`.

**Pregunta guía:** ¿qué se sabe sobre transcribir automáticamente lenguas indígenas con muy pocos datos, y qué falta para hacerlo en yaqui?

---

## 1. Introducción y alcance

- Problema: el "cuello de botella de la transcripción". Transcribir una hora de grabación puede tomar decenas de horas de especialista (Shi et al., 2021).
- Alcance: trabajos de 2018 en adelante, con énfasis en lenguas de América y en modelos multilingües preentrenados.
- Método de búsqueda: fuentes consultadas, cadenas en inglés y español, criterios de inclusión.

## 2. El yaqui como objeto de estudio

- Lengua yuto-nahua (rama taracahita, grupo cahita), hablada en Sonora y Arizona.
- Rasgos que importan para el ASR: vocales largas y cortas que distinguen significado, consonantes geminadas, saltillo, acento tonal y morfología aglutinante (Estrada Fernández, 2009; Dedrick y Casad, 1999).
- Ortografía no unificada: *b/v* y *j/h* según el autor (Estrada et al., 2004; Shaul, 1999). El modelo aprenderá la convención que se elija.
- Recursos existentes: diccionarios, gramáticas y textos glosados. No hay trabajos académicos de ASR centrados en el yaqui, pero **Omnilingual ASR (Meta, 2025) incluye al yaqui** con nivel de recursos bajo, sin evaluación pública sobre grabaciones de documentación.

## 3. Fundamentos del reconocimiento automático del habla

- Del enfoque clásico (modelos ocultos de Markov) a los modelos de extremo a extremo.
- Dos familias: CTC (wav2vec 2.0, XLS-R, MMS, W2V-BERT) y codificador-decodificador (Whisper).
- Métricas: WER y CER. En lenguas con límites de palabra poco estandarizados se prefiere CER (Ebrahimi et al., 2023).

## 4. Modelos multilingües preentrenados

- Tabla comparativa: datos de preentrenamiento, número de parámetros, lenguas cubiertas, licencia y forma de ajuste.
- MMS con adaptadores es eficiente con pocos datos (Pratap et al., 2024; Mainzinger y Levow, 2024).
- Whisper sin ajuste falla en lenguas que no vio, pero ajustado puede ganar en algunos casos (Kriukova et al., 2026). Conviene probar ambas familias.

## 5. ASR para lenguas indígenas y de bajos recursos

- México: mixteco de Yoloxóchitl (Shi et al., 2021), náhuatl (Pugh et al., 2024), totonaco (Universidad de Alberta, 2024), y la discusión en español de Cruz (2021).
- Continente: mvskoke, bribri, cabécar, séneca, dënë sųłıné y las cinco lenguas de AmericasNLP 2022.
- Tabla síntesis: lengua, horas de datos, modelo, métrica y resultado. Lectura esperada: con 1 a 4 horas ya se obtienen modelos útiles como borrador para corrección humana.

## 6. Preparación del corpus

- Normalización de audio, detección de voz (Coto-Solano et al., 2026), segmentación y alineación forzada (Coto-Solano y Flores Solórzano, 2016; Pratap et al., 2024).
- Partición por hablante para no sobreestimar el desempeño.
- Habla espontánea frente a habla leída (Liang y Levow, 2025).

## 7. Modelos ligeros y ejecución local

- Adaptadores, destilación (Gandhi et al., 2023) y cuantización.
- Por qué local: privacidad de los datos de la comunidad y uso sin conexión.

## 8. El ASR dentro del flujo de documentación

- El objetivo no es automatizar todo, sino producir un borrador que el especialista corrige (Foley et al., 2018; Amith et al., 2021).
- Evaluación extrínseca: tiempo ahorrado por transcripción (Prud'hommeaux et al., 2021).

## 9. Ética y gobernanza de datos

- Principios CARE (Carroll et al., 2020) y enfoque descolonizador (Bird, 2020).
- Implicaciones para este proyecto: procesamiento local, autoridad de los lingüistas sobre el corpus y acuerdos con la Universidad del Pueblo Yaqui.

## 10. Brechas y posicionamiento de la tesis

- El único ASR que cubre el yaqui es un modelo masivo (Omnilingual ASR) que nadie ha evaluado con habla espontánea de documentación, y no existe un corpus de habla yaqui alineado y documentado.
- Hay poca evidencia sobre lenguas yuto-nahuas del norte de México.
- Falta comparar MMS, XLS-R, W2V-BERT y Whisper sobre grabaciones de documentación reales, con evaluación de los lingüistas.
- Aporte de la tesis: corpus alineado, comparación de modelos, modelo ligero y herramienta de transcripción asistida.
