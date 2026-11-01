# Buscador de letras com Streamlit

App web simples que busca a letra de uma música a partir do nome da banda e da música, consumindo a API pública [lyrics.ovh](https://lyricsovh.docs.apiary.io/).

Foi meu primeiro projeto consumindo uma API REST com Python: requisição HTTP com `requests`, leitura da resposta JSON, tratamento do caso "não encontrado" e uma interface em Streamlit.

## Como funciona

1. O usuário informa a banda e a música.
2. O app chama `GET https://api.lyrics.ovh/v1/{banda}/{musica}`.
3. Se a API responder `200`, a letra aparece na tela; caso contrário, o app mostra uma mensagem de erro.

| Arquivo | Conteúdo |
| --- | --- |
| [`app.py`](app.py) | Interface em Streamlit e função `buscar_letra`. |
| [`testes.ipynb`](testes.ipynb) | Testes exploratórios da API no Jupyter. |
| [`pyproject.toml`](pyproject.toml) | Dependências, gerenciadas com Poetry. |

## Como rodar

Requer Python 3.13 e [Poetry](https://python-poetry.org/).

```bash
poetry install
poetry run streamlit run app.py
```

O app abre no navegador em `http://localhost:8501`.

## Tecnologias

Python · requests · Streamlit · Poetry · Jupyter
