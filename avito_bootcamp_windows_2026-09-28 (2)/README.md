# Запуск решения

Архив содержит ноутбук, исходные данные, зависимости, описание подхода и
готовый `submission.csv`. После распаковки оставьте папку `data/` рядом с
`solution.ipynb`. Параметры модели и списки признаков находятся в ноутбуке.

## Windows 10/11

Нужен Python 3.12, 64 бит. Откройте PowerShell **в распакованной папке** и
выполните команды по порядку:

```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m notebook
```

В открывшемся Jupyter выберите `solution.ipynb` и запустите **Run All Cells**.
Ноутбук создаст `result/submission.csv`. На случай, если обучение сейчас не
нужно, готовый файл сдачи уже лежит в корне архива: `submission.csv`.

## macOS и Linux

Из распакованной папки:

```sh
python3.12 -m venv .venv
.venv/bin/python -m pip install -r requirements.txt
.venv/bin/python -m notebook
```

Ноутбук использует относительные пути через `pathlib`. Он не импортирует
проектные `.py` и не обращается к внешним API. Проверенный запуск выполнен
на Python 3.12.14. Версии библиотек закреплены в `requirements.txt`.
