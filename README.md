## **Preparing your requirements**

To view the documentation locally, first install the requirements on your environment by running the following on your terminal:

```bash
pip install -r docs/requirements.txt
```

It is recommended that you create a virutal environment to install your dependencies. If you have conda and have activated a virtual environment, do the following instead in your conda environment (to use your conda's pip):

```bash
python -m pip install -r docs/requirements.txt
```

Then, host the documentation locally with:

```bash
mkdocs serve
```

You should be able to navigate to the documentation on [https://127.0.0.1:8000/](https://127.0.0.1:8000/).
