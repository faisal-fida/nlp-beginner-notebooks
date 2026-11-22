# nlp-classification-text-generation-notebooks

Two small beginner Jupyter notebooks: text classification with scikit-learn and a word-level text generation attempt with TensorFlow.

## Notebooks

- `NLP Classification.ipynb`: classifies 20 hand-written sentences into two labels (0/1). Pipeline: `CountVectorizer`, `TfidfTransformer`, `SGDClassifier`. Splits 80/20, prints accuracy, then predicts one new sentence.
- `NLP QnA.ipynb`: builds a word vocabulary from 10 short machine learning titles and defines a `generate_text` function that samples next words from a model.

## Status

Teaching-level toy examples, not working models.

- Classification: the sentences and the labels are split by two separate `train_test_split` calls without a shared seed, so training texts and labels do not line up. Accuracy on the tiny set is therefore meaningless (the saved notebook output shows 0.25).
- Text generation: the notebook never defines or trains the RNN `model` it uses, and `generate_text` maps words back with the wrong dictionary direction. Running the last cells fails with a `NameError`. Despite the file name, it does no question answering.

## Tech stack

Python 3, Jupyter, scikit-learn, NumPy, TensorFlow.

## Setup and run

```bash
pip install jupyter scikit-learn numpy tensorflow
jupyter notebook
```

Open a notebook and run the cells top to bottom. No environment variables or data files are needed.

## License

MIT
