# Plantilla LaTeX para trabajos recepcionales de la UJAT-DACyTI

Plantilla en formato APA 7ma. edición basada en los **LINEAMIENTOS PARA LA ELABORACIÓN DE LA TESIS DE LICENCIATURA, ESPECIALIDAD, MAESTRÍA Y DOCTORADO** de la UJAT: https://archivos.ujat.mx/2024/abogado-general/17-5/2-WEB-LINEAMIENTOS-PARA-LA-ELABORACION-DE-LA-TESIS-DE-LICENCIATURA-ESPECIALIDAD-MAESTRIA-Y-DOCTORADO-28112023.pdf.

## Archivos

- `tesis.tex`: documento principal (portada, índices, capítulos, referencias).
- `referencias.bib` — base de datos bibliográfica de ejemplo.
- `tesis.pdf` — versión ya compilada.

## Requisitos previos

Esta plantilla necesita tres paquetes de TeX Live que no vienen en instalaciones por defecto:

| Paquete                 | Contiene                                |
|-------------------------|-----------------------------------------|
| `texlive-lang-spanish`  | `babel` en español (`spanish.ldf`)      |
| `texlive-bibtex-extra`  | el paquete y estilo `apacite`           |
| `texlive-latex-extra`   | `titlesec`, `enumitem`, `fancyhdr`, etc.|

Si usas Ubuntu como yo, simplemente instala los paquetes necesarios desde la terminal así:

```bash
sudo apt-get install texlive-lang-spanish texlive-bibtex-extra texlive-latex-extra
```

## Pasos para la compilación

```bash
pdflatex tesis
bibtex   tesis
pdflatex tesis
pdflatex tesis
```

Las dos últimas ejecuciones de `pdflatex` son necesarias para configurar la numeración cruzada, el índice y la lista de referencias. Te recomiendo utilizar TeXstudio (https://texstudio.sourceforge.net) porque solamente necesitas presionar el botón de Play ▶ una sola vez y TeXstudio realiza los 3 pasos de la compilación por tí.

## Adapta la plantilla

En color <mark>amarillo</mark> se muestran los datos que debes editar. Vamos por partes:

1. **Datos del trabajo**: agrega tu grado, nombre, estudiante, director del trabajo y la fecha.
1. **Contenido de los capítulos**: reemplaza los textos entre corchetes `[ ]` con tu propia información.
1. **Referencias**: agrega tus fuentes a `referencias.bib` y cítalas con `\cite{clave}` para la cita clásica entre paréntesis o `\citeA{clave}` para la cita narrativa en formato "Autor (Año)".
1. Disfruta tu tesis en formato científico sin necesidad de usar M$ Word.

> Plantilla creada con ❤️ por Oscar Chávez-Bosquez utilizando exclusivamente software libre.