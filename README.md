# Predicción de ocupación de aulas con sensores (sin visión)

Este repositorio contiene:
- `main.tex`: paper en LaTeX (11pt, carta, márgenes 1", interlineado 1.1, sin sangría).
- `referencias.bib`: bibliografía en estilo numérico (biblatex).
- `train.py`: script de entrenamiento/evaluación con scikit-learn.
- Datos esperados: CSV del dataset UCI/Kaggle (ver enlaces en el paper).

## Cómo compilar el PDF
- En Overleaf: crear proyecto y subir `main.tex` y `referencias.bib` (compilador XeLaTeX o pdfLaTeX + biber).
- Local: `pdflatex main.tex && biber main && pdflatex main.tex && pdflatex main.tex`

## Cómo entrenar
```bash
pip install -r requirements.txt  # opcional
python train.py --csv data/datatraining.txt data/datatest.txt data/datatest2.txt --sep ","
```
