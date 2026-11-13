# ConsentIA

Consentimiento informado e instrucciones en medicina estética. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/consentia/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24187235.svg)](https://doi.org/10.5281/zenodo.24187235)

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

Tercera app del [Kit EstéticIA](https://fborrasumh.github.io/kitesteticia/): el consentimiento informado de cada técnica y las instrucciones antes y después del tratamiento.

- **Lee la ficha de [AnamnesIA](https://fborrasumh.github.io/anamnesia/)** (formato `kitesteticia-paciente/1`): identificador, edad, técnicas y antecedentes, sin volver a preguntar. Si AnamnesIA marcó «no tratar ahora» para una técnica, lo recuerda con su motivo.
- **Riesgos personales**: los antecedentes que importan (anticoagulantes, herpes, queloides, fototipo alto, enfermedad autoinmune, relleno previo, isotretinoína…) se convierten en riesgos explicados para cada técnica. Sin ficha, el médico confirma que ha revisado las circunstancias personales.
- **Diez técnicas**, con qué es, qué esperar, lo que ocurre casi siempre, riesgos frecuentes, riesgos poco frecuentes pero graves, contraindicaciones y alternativas. Producto, lote y zona por técnica.
- **En el idioma del paciente** (español, inglés o portugués), independiente del idioma de la pantalla.
- **Apartados de la Ley 41/2002** (arts. 8 y 10) comprobados uno a uno, firma del representante legal si el paciente es menor, revocación y autorización de fotografías separada (historia, docencia, redes).
- **Legibilidad** del documento con el índice INFLESZ en español, el de Flesch en inglés y el de Flesch adaptado por Martins en portugués.
- **Dos documentos**: el consentimiento para firmar y las instrucciones para casa con los signos de alarma y el teléfono de la consulta. Word e impresión.

No usa IA y no hace ninguna llamada de red. Interfaz en español, inglés y portugués.

## Privacidad

Todo se guarda en el navegador. Nada sale hacia ningún servidor. La app trabaja con un identificador; el nombre y el documento de identidad se escriben a mano en el papel.

## Límites

Los textos los ha redactado el equipo autor a partir de fichas técnicas, instrucciones de uso y literatura habitual: son una base que cada consulta revisa con sus productos y su asesoría legal. El documento escrito no sustituye a la explicación verbal. La comprobación de la ley verifica que los apartados están, no su suficiencia jurídica, y no es asesoramiento legal. La legibilidad es una medida aproximada.

## Pruebas

`node tests/test_nucleo.js` (textos en tres idiomas, ficha, riesgos personales, documentos, comprobación legal y legibilidad) y `python3 tests/smoke.py` (lee una ficha descargada de verdad de AnamnesIA; recorrido completo en Chromium, tres idiomas, persistencia, accesibilidad WCAG 2.2 AA, CSP y móvil).

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Elena Caride Miana (Dra. Caride Medicina Estética & Antiaging).

Tercera app del Kit EstéticIA, diseñado para el alumnado del Máster de Formación Permanente en Medicina Estética Integral y Antienvejecimiento (UMH).

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Elena Caride Miana [0000-0002-7620-4857](https://orcid.org/0000-0002-7620-4857)

## Cómo citar

Borrás Rocher, F. y Caride Miana, E. (2026). *ConsentIA* (v1.0.0) [Software]. DOI: [10.5281/zenodo.24187235](https://doi.org/10.5281/zenodo.24187235)

## Licencia

MIT. Véase [LICENSE](LICENSE).
